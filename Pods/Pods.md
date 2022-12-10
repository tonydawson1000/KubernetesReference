# Pods

## Description
### ["Pods are the smallest deployable units of computing that you can create and manage in Kubernetes."](https://kubernetes.io/docs/concepts/workloads/pods/)

---
## Sample Pod Manifest.
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
  labels:
    app: nginx
    tier: frontend
spec:
  containers:
  - name: nginx
    image: nginx
```

---
## Cheat Sheet

| Command | Description |
|---|---|
| Pod Help | |
| `kubectl explain pod` | Display Pod info |
| `kubectl run --help` | Display Pod help |
| Readonly Commands | |
| `kubectl get pods` | List all Pods |
| `kubectl get pod <podname>` | List single Pod |
| `kubectl get pods -o wide` | List detailed info about Pods |
| `kubectl get pod <podname> -o wide` | List detailed info about a Pod |
| `kubectl describe pod <podname>` | List full details about a a Pod |
| Create Manifest Command | |
| `kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-nginx.yaml` | Generate a sample Pod Manifest Definition file  |
| Apply Manifest | |
| `kubectl apply -f pod-nginx.yaml` | Send the Manifest to Kubernetes API |
| DELETE Pod(s) | |
| `kubectl delete pod <podname> <podname2> <podname3>` | Deletes one or more Pods |