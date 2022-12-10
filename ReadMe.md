# Kubernetes Reference

```
  _                             _  __     _                          _
 | |                           | |/ /    | |                        | |
 | |     ___  __ _ _ __ _ __   | ' /_   _| |__   ___ _ __ _ __   ___| |_ ___  ___
 | |    / _ \/ _` | '__| '_ \  |  <| | | | '_ \ / _ \ '__| '_ \ / _ \ __/ _ \/ __|
 | |___|  __/ (_| | |  | | | | | . \ |_| | |_) |  __/ |  | | | |  __/ ||  __/\__ \
 |______\___|\__,_|_|  |_| |_| |_|\_\__,_|_.__/ \___|_|  |_| |_|\___|\__\___||___/

```

## Description
A collection of useful docs for working with Kubernetes.

| Resource | Description |
|---|---|
| [Pods](./Pods/Pods.md) | "Pods are the smallest deployable units of computing that you can create and manage in Kubernetes." |
| [ReplicaSets](./ReplicaSets/ReplicaSet.md) | "A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods." |
| [Deployments](./Deployments/Deployment.md) | "A Deployment provides declarative updates for Pods and ReplicaSets." |

---
## Command line tools to interact with Kubernetes.

| Name | Description |
|---|---|
| `kubeadm` | CLI tool that simplifies creation and management of Kubernetes Cluster |
| `kubectl` | CLI tool for interacting with Kubernetes Cluster

---
## YAML Manifests
All Kubernetes YAML Manifest files have the following 4 top-level properties.

```yaml
apiVersion:
kind:
metadata:
spec:
```

# `kubectl edit` ...

---
## Cheat Sheet

| Command | Description |
|---|---|
| `yo mama` | some desc  |
|   |   |
|   |   |