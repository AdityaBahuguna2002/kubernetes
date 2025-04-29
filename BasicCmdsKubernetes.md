# Basic Kubernetes Commands

## Cluster Information
```bash
# Check cluster information
kubectl cluster-info

# View nodes in the cluster
kubectl get nodes
```

## Pods
```bash
# List all pods in the current namespace
kubectl get pods

# List all pods in all namespaces
kubectl get pods --all-namespaces

# Describe a specific pod
kubectl describe pod <pod-name>

# ex -kubectl describe pod frontend-deployment-755744d6d9-k4bt4

# Delete a pod
kubectl delete pod <pod-name>
```

## Deployments
```bash
# List all deployments
kubectl get deployments

# Create a deployment
kubectl create deployment <deployment-name> --image=<image-name>

# Scale a deployment
kubectl scale deployment <deployment-name> --replicas=<number>

# Delete a deployment
kubectl delete deployment <deployment-name>
```

## Services
```bash
# List all services
kubectl get services

# Expose a deployment as a service
kubectl expose deployment <deployment-name> --type=<service-type> --port=<port>

# Delete a service
kubectl delete service <service-name>
```

## Namespaces
```bash
# List all namespaces
kubectl get namespaces

# Create a namespace
kubectl create namespace <namespace-name>

# Delete a namespace
kubectl delete namespace <namespace-name>
```

## Logs
```bash
# View logs of a pod
kubectl logs <pod-name>

# Stream logs of a pod
kubectl logs -f <pod-name>
```

## ConfigMaps and Secrets
```bash
# List all ConfigMaps
kubectl get configmaps

# List all Secrets
kubectl get secrets
```

## Apply and Delete Resources
```bash
# Apply a configuration file
kubectl apply -f <file-name>.yaml

# Delete resources defined in a file
kubectl delete -f <file-name>.yaml
```

## Debugging
```bash
# Execute a command in a running pod
kubectl exec -it <pod-name> -- <command>

# Start a shell session in a pod
kubectl exec -it <pod-name> -- /bin/bash
```

## Other Useful Commands
```bash
# Get resource usage (requires metrics-server)
kubectl top nodes
kubectl top pods

# Get events in the cluster
kubectl get events
```