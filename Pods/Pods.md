# Pods

## Description
### ["Pods are the smallest deployable units of computing that you can create and manage in Kubernetes."](https://kubernetes.io/docs/concepts/workloads/pods/)

---
## Cheat Sheet

| Command | Description |
|---|---|
| Readonly Commands | |
| `kubectl get pods` | List all Pods |
| `kubectl get pods -o wide` | List detailed info about Pods |
| Create Manifest Command | |
| `kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-nginx.yaml` | Generate a sample Pod Manifest Definition file  |
| Apply Manifest | |
| `kubectl apply -f pod-nginx.yaml` | Send the Manifest to Kubernetes API |