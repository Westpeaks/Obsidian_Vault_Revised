# Adding storage to Kubernetes Container

- To add storage via FluxCD, you must create a storage.yaml file cluster directory under `
  `*Path-of-cluser-directory*/apps/base/*app-directory*`
	- In the example the app is LinkDing so `*Path-of-cluser-directory*/apps/base/linkding`

`k exec -it linkding-7bffb6cdb9-h7mnm -- python manage.py createsuperuser --username=mischa --email=mischa@example.com`

```
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: linkding-data-pvc
spec:
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 1Gi
```

- After the storage is declared, it must be added to the kustomization.yaml for Flux to deploy the configured storage to the app container. 
	- First, under specs in the deployment.yaml file the storage is declared in the container config.
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

          volumeMounts: #here is where the volume will mount
            - name: linkding-data
              mountPath: /etc/linkding/data
      volumes: #here is where it is named
        - name: linkding-data
          persistentVolumeClaim:
            claimName: linkding-data-pvc #this points to the name in the storage.yaml file
	  ```
- Then the storage.yaml file must be listed in the kustomization.yaml in the app directory (Ex.`*Path-of-cluser-directory*/apps/base/linkding`)
  ```
  apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
resources:
  - deployment.yaml
  - namespace.yaml
  - storage.yaml
  - service.yaml
  ```
  - Once this is complete, push the changes to GitHub and Flux will deploy the storage.
## Links:

[[Deploying an Application via Flux]]


20260811