# ReplicaSets

## Description
### ["A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods."](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/)

---
## Sample ReplicaSet Manifest.
```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: nginx-rs
  labels:
    app: myapp
    tier: frontend
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp
      tier: frontend
  template:
    metadata:
      name: nginx-pod
      labels:
        app: myapp
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
| ReplicaSet Help | |
| `kubectl explain replicaset` | Display ReplicaSet info |
| `kubectl create replicaset --help` | Display ReplicaSet help |
| Readonly Commands | |
| `kubectl get replicasets` | List all ReplicaSets |
| `kubectl get replicaset <replicasetname>` | List single ReplicaSet |
| `kubectl get replicasets -o wide` | List detailed info about ReplicaSets |
| `kubectl get replicaset <replicasetname> -o wide` | List detailed info about a ReplicaSet |
| `kubectl describe replicaset <replicasetname>` | List full details about a ReplicaSet |
| Create Manifest Command | |
| `kubectl ??? --dry-run=client -o yaml > rs-myapp.yaml` | Generate a sample ReplicaSet Manifest Definition file  |
| Apply Manifest | |
| `kubectl apply -f rs-myapp.yaml` | Send the Manifest to Kubernetes API |
| Scale ReplicaSet | |
| `kubectl apply -f rs-myapp.yaml` | Update (`replicas: 6`) and send the Manifest to Kubernetes API |
| `kubectl scale --replicas=6 -f rs-myapp.yaml` | Scale based on original yaml manifest |
| `kubectl scale replicaset <replicasetname> --replicas=6` | Scale based on name |
| `kubectl edit replicaset <replicasetname>` | Edit (and save) the yaml manifest directly within Kubernetes |
| DELETE ReplicaSet  | |
| `kubectl delete replicaset <replicasetname>` | Deletes the ReplicaSet (and all associated Pod(s)) |