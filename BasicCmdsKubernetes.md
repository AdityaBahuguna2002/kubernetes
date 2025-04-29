# Basic Kubernetes Commands

## Cluster Information
```bash
# Check cluster information
kubectl cluster-info
```
```bash
# View nodes in the cluster
kubectl get nodes
```

## Pods
```bash
# List all pods in the current namespace
kubectl get pods
```
```bash
# List all pods in all namespaces
kubectl get pods --all-namespaces
```
```bash
# Describe a specific pod
kubectl describe pod <pod-name>
```
# ex -kubectl describe pod frontend-deployment-755744d6d9-k4bt4

```bash
# Delete a pod
kubectl delete pod <pod-name>
```

## Deployments
```bash
# List all deployments
kubectl get deployments
```
```bash
# Create a deployment
kubectl create deployment <deployment-name> --image=<image-name>
```

```bash
# Scale a deployment
kubectl scale deployment <deployment-name> --replicas=<number>
```

```bash
# Delete a deployment
kubectl delete deployment <deployment-name>
```

## Services
```bash
# List all services
kubectl get services
```

```bash
# Expose a deployment as a service
kubectl expose deployment <deployment-name> --type=<service-type> --port=<port>
```

```bash
# Delete a service
kubectl delete service <service-name>
```

## Namespaces
```bash
# List all namespaces
kubectl get namespaces
```

```bash
# Create a namespace
kubectl create namespace <namespace-name>
```

```bash
# Delete a namespace
kubectl delete namespace <namespace-name>
```

## Logs
```bash
# View logs of a pod
kubectl logs <pod-name>
```

```bash
# Stream logs of a pod
kubectl logs -f <pod-name>
```

## ConfigMaps and Secrets
```bash
# List all ConfigMaps
kubectl get configmaps
```

```bash
# List all Secrets
kubectl get secrets
```

## Apply and Delete Resources
```bash
# Apply a configuration file
kubectl apply -f <file-name>.yaml
```
```bash
# Delete resources defined in a file
kubectl delete -f <file-name>.yaml
```

## Debugging
```bash
# Execute a command in a running pod
kubectl exec -it <pod-name> -- <command>
```
```bash
# Start a shell session in a pod
kubectl exec -it <pod-name> -- /bin/bash
```

## Other Useful Commands
```bash
# Get resource usage (requires metrics-server)
kubectl top nodes
kubectl top pods
```
```bash
# Get events in the cluster
kubectl get events
```
