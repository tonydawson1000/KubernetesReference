# ReplicaSets

## Description
### ["A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods."](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/)

---
## Cheat Sheet

| Command | Description |
|---|---|
| Readonly Commands | |
| `kubectl get replicasets` | List all ReplicaSets |
| `kubectl get replicasets -o wide` | List detailed info about Pods |
| Create Manifest Command | |
| `kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-nginx.yaml` | Generate a sample Pod Manifest Definition file  |
| Apply Manifest | |
| `kubectl apply -f pod-nginx.yaml` | Send the Manifest to Kubernetes API |