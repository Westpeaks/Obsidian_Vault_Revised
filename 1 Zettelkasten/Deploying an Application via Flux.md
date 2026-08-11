
Flux uses and GitOps principles to deploy applications to a Kubernetes cluster via YAML configuration files.

Flux has a recommended repository structure, organizing files into separate directories for apps, base configurations, and environment-specific configurations (staging, production).

Example of Flux structure:
```console
├── apps
│   ├── base
│   ├── production 
│   └── staging
├── infrastructure
│   ├── base
│   ├── production 
│   └── staging
└── clusters
    ├── production
    └── staging
```

• This requires the creation of several YAML files:

- apps.yaml: This tells Flux to look at the apps/staging directory

- kustomization.yaml files: Here we define resources and configurations for the application

- namespace.yaml: We create a dedicated namespace for the application

- deployment.yaml: We define the Kubernetes deployment for the application

• Let's understand the path Flux follows to deploy our application:

1. Flux reads the clusters/staging directory

2. Finds and applies the apps.yaml file

3. Looks at the apps/staging directory

4. Finds the kustomization file

5. Applies the resources we defined in the base configuration

• After we commit and push our changes, Flux automatically detects and applies the new configuration without any manual intervention needed.

• We verify our deployment by checking the namespace, pods, and using port-forwarding to access the application.

• This approach gives us version-controlled, declarative management of Kubernetes resources, and we'll see firsthand the benefits of GitOps.

```
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
resources:
  - deployment.yaml
  - namespace.yaml


apiVersion: v1
kind: Namespace
metadata:
  name: linkding
```

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: linkding
spec:
  replicas: 1
  selector:
    matchLabels:
      app: linkding
  template:
    metadata:
      labels:
        app: linkding
    spec:
      containers:
        - name: linkding
          image: sissbruecker/linkding:1.31.0
          ports:
            - containerPort: 9090
```

```bash
kubectl port-forward pod/linkding 8080:9090
```
## Links:

[[About GitOps]]

[Ways of structuring your repositories](https://fluxcd.io/flux/guides/repository-structure/)

20260727