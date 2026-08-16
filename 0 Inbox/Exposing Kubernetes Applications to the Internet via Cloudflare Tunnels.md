
## Configuring tunnel from CLI

- Installing CloudflareD

[https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/create-local-tunnel/](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/create-local-tunnel/ "https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/create-local-tunnel/")

`cloudflared tunnel login`

- This created a cert at /home/*user*/.cloudflared/cert.pem

**cert.pem example**
```
cloudflared tunnel create ldpi



kubectl create secret generic tunnel-credentials \

--from-file=credentials.json=59c97568-9eda-4dbf-9857-b6cf9cf91259.json
```

## Adding to Cloudflare DNS

- Go to Cloudflare DNS, add a new record

- select CNAME

- Enter: 
  
  [59c97568-9eda-4dbf-9857-b6cf9cf91259.cfargotunnel.com](http://59c97568-9eda-4dbf-9857-b6cf9cf91259.cfargotunnel.com "http://59c97568-9eda-4dbf-9857-b6cf9cf91259.cfargotunnel.com")
  
  *Note* this id will change with each new tunnel created. 

## Adding manifests

- First we need a service

```
apiVersion: v1
kind: Service
metadata:
  name: linkding
spec:
  ports:
    - port: 9090
  selector:
    app: linkding
  type: ClusterIP
```

- Now let's configure the tunnel

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: cloudflared
spec:
  selector:
    matchLabels:
      app: cloudflared
  replicas: 2 # You could also consider elastic scaling for this deployment
  template:
    metadata:
      labels:
        app: cloudflared
    spec:
      containers:
      - name: cloudflared
        image: cloudflare/cloudflared:latest
        args:
        - tunnel

        # Points cloudflared to the config file, which configures what
        # cloudflared will actually do. This file is created by a ConfigMap
        # below.
        - --config
        - /etc/cloudflared/config/config.yaml
        - run
        livenessProbe:
          httpGet:
            # Cloudflared has a /ready endpoint which returns 200 if and only if
            # it has an active connection to the edge.
            path: /ready
            port: 2000
          failureThreshold: 1
          initialDelaySeconds: 10
          periodSeconds: 10
        volumeMounts:
        - name: config
          mountPath: /etc/cloudflared/config
          readOnly: true
        # Each tunnel has an associated "credentials file" which authorizes machines
        # to run the tunnel. cloudflared will read this file from its local filesystem,
        # and it'll be stored in a k8s secret.
        - name: creds
          mountPath: /etc/cloudflared/creds
          readOnly: true
      volumes:
      - name: creds
        secret:
          secretName: tunnel-credentials

      # Create a config.yaml file from the ConfigMap below.
      - name: config
        configMap:
          name: cloudflared
          items:
          - key: config.yaml
            path: config.yaml
---
# This ConfigMap is just a way to define the cloudflared config.yaml file in k8s.
# It's useful to define it in k8s, rather than as a stand-alone .yaml file, because
# this lets you use various k8s templating solutions (e.g. Helm charts) to
# parameterize your config, instead of just using string literals.
apiVersion: v1
kind: ConfigMap
metadata:
  name: cloudflared
data:
  config.yaml: |
    # Name of the tunnel you want to run
    
    tunnel: ldpi

    credentials-file: /etc/cloudflared/creds/credentials.json

    # Serves the metrics server under /metrics and the readiness server under /ready
    metrics: 0.0.0.0:2000
    no-autoupdate: true

    ingress:
    - hostname: ldpi.mischavandenburg.net
      service: http://linkding:9090

    # This rule sends traffic to the built-in hello-world HTTP server. This can help debug connectivity
    # issues. If hello.example.com resolves and tunnel.example.com does not, then the problem is
    # in the connection from cloudflared to your local service, not from the internet to cloudflared.
    - hostname: hello.example.com
      service: hello_world
    # This rule matches any traffic which didn't match a previous rule, and responds with HTTP 404.
    - service: http_status:404
```
## Links:

[Older guide](https://developers.cloudflare.com/cloudflare-one/networks/connectors/cloudflare-tunnel/deployment-guides/kubernetes/)

[Older tunnel yaml example](https://github.com/cloudflare/argo-tunnel-examples/blob/master/named-tunnel-k8s/cloudflared.yaml)

[[Deploying an Application via Flux]]

[[Adding Storage to Deployed Container  via Flux]]

20260812