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

---

## Kubernetes Dashboard

Deploy the [Kubernetes Dashboard](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)

Configure [Access to the Dashboard](https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md)

Get a Login Token by running the following

```
kubectl get secret admin-user -n kubernetes-dashboard -o jsonpath={".data.token"} | base64 -d
```

## kubectl logs
#### Used to show the Logs from within the Container/Pod
```
kubectl logs <podname>
```

## kubectl exec
#### Used to execute a process inside a Container/Pod
```
kubectl exec -it <podname> -- <processname>`

e.g.

kubectl exec -it nginx -- /bin/sh

or

kubectl exec --stdin --tty nginx -- /bin/bash
```
---


---
## Cheat Sheet

| Command | Description |
|---|---|
| `yo mama` | some desc  |
|   |   |
|   |   |