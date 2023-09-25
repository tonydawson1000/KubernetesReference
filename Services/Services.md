# Services

## Description
### ["A Service is a method for exposing a network application that is running as one or more Pods in your cluster."](https://kubernetes.io/docs/concepts/services-networking/service/)

## Imperative :(
Used to 'expose' OBJECTS (Pods/Deployments) as a Service

    kubectl expose <pod/deployment> --port=<host port> --target-port=<container port>

    e.g.

    kubectl expose pod mynginx --port=80 --target-port=8080

---

#### Verify details of Service
Use `get` or `describe` to find details

    kubectl get/describe service <servicename>

    e.g.

    kubectl get service mynginx

    or 

    kubectl describe service mynginx

---

## Declaritive :)
Have kubectl generate (`--dryrun`) a Service Manifest (yaml) file, then apply

    kubectl expose pod <podname> --port=80 --target-port=8080 --dry-run=client -o yaml > mynginx-service-to-pod.yaml
    
    or
    
    kubectl expose deployment <deploymentname> --port=80 --target-port=8080 --dry-run=client -o yaml > mynginx-service-to-deployment.yaml

    kubectl apply -f mynginx-service.yaml

---