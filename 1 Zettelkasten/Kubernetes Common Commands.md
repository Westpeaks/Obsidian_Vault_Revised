### Cluster & Context
```bash
kubectl cluster-info                    # cluster endpoint info
kubectl config get-contexts             # list available contexts
kubectl config use-context <name>       # switch context
kubectl config current-context          # show active context
kubectl get nodes                       # list nodes
kubectl describe node <name>            # node details/capacity
```

### Getting Info
```bash
kubectl get pods                        # pods in current namespace
kubectl get pods -A                     # pods across all namespaces
kubectl get pods -o wide                # pods with node/IP info
kubectl get all                         # pods, services, deployments, etc.
kubectl get <resource> -n <namespace>   # scope to a namespace
kubectl describe pod <name>             # detailed pod info + events
kubectl get events --sort-by='.lastTimestamp'  # recent cluster events
```

### Logs & Debugging
```bash
kubectl logs <pod>                      # logs from a pod
kubectl logs -f <pod>                   # follow/stream logs
kubectl logs <pod> -c <container>       # logs from specific container
kubectl logs <pod> --previous           # logs from crashed container
kubectl exec -it <pod> -- /bin/sh       # shell into a pod
kubectl exec -it <pod> -c <container> -- bash  # into specific container
kubectl top pods                        # resource usage (needs metrics-server)
kubectl top nodes                       # node resource usage
```

### Creating & Applying
```bash
kubectl apply -f file.yaml              # create/update from manifest
kubectl apply -f ./dir/                 # apply all manifests in a dir
kubectl create -f file.yaml             # create only (errors if exists)
kubectl delete -f file.yaml             # delete resources in manifest
kubectl diff -f file.yaml               # preview changes before apply
```

### Editing & Scaling
```bash
kubectl edit deployment <name>          # live-edit a resource
kubectl scale deployment <name> --replicas=3
kubectl rollout restart deployment <name>
kubectl rollout status deployment <name>
kubectl rollout undo deployment <name>  # rollback last change
kubectl rollout history deployment <name>
kubectl set image deployment/<name> <container>=<image>:<tag>
```

### Deleting
```bash
kubectl delete pod <name>
kubectl delete deployment <name>
kubectl delete namespace <name>
kubectl delete pods --field-selector=status.phase=Failed  # clean up failed pods
```

### Namespaces
```bash
kubectl get namespaces
kubectl create namespace <name>
kubectl config set-context --current --namespace=<name>  # default ns for context
```

### Services & Networking
```bash
kubectl get svc                         # list services
kubectl port-forward svc/<name> 8080:80 # local port -> service port
kubectl port-forward pod/<name> 8080:80 # local port -> pod port
kubectl get endpoints                   # verify service routes to pods
```

### ConfigMaps & Secrets
```bash
kubectl create configmap <name> --from-file=config.txt
kubectl create secret generic <name> --from-literal=key=value
kubectl get secret <name> -o jsonpath='{.data.key}' | base64 -d
```

### Handy flags/shortcuts
```bash
kubectl get po,svc,deploy               # comma-sep multiple resource types
kubectl get pod <name> -o yaml          # full resource definition
kubectl explain <resource>.<field>      # docs for a field, e.g. pod.spec.containers
watch kubectl get pods                  # auto-refresh view
kubectl api-resources                   # list all resource types
```

A few worth aliasing if you're on the CLI a lot: `k` for `kubectl`, and `kgp`/`kgs`/`kdp` for get pods/get svc/describe pod — saves a ton of typing over time. Since you're running your own cluster at home, `k9s` is also worth a look if you don't already have it — it's a terminal UI that wraps a lot of this (logs, exec, resource browsing) into one dashboard instead of juggling separate commands.

## Links:

[[Kubernetes Basics]]

20260722