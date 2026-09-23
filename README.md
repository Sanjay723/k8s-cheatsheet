## Cluster Information & Context


```bash
# View local Kind clusters
kind get clusters

# Display cluster endpoint and core service info
kubectl cluster-info

# View kubeconfig file (PowerShell)
cat .\.kube\config

# Set alias for kubectl
alias k="kubectl"

---


### Important Note for Windows PowerShell:
In standard PowerShell on Windows, the Linux-style command `alias k="kubectl"` will give an error. If you are using PowerShell in your terminal[cite: 5, 6], the native PowerShell equivalent is:


```powershell
Set-Alias -Name k -Value kubectl


# List all namespaces
kubectl get ns


# Run a single Nginx pod imperatively
kubectl run nginx --image=nginx

# List pods in current namespace
kubectl get pods

# List pods with IP and node placement details
kubectl get pod nginx -o wide

# List all pods across all namespaces
kubectl get pods -A -o wide

# List pods inside a specific namespace
kubectl get pods -n kube-system

# View detailed pod events and status
kubectl describe pod nginx

# Delete a specific pod
kubectl delete pod nginx

# Delete an individual pod managed by a Deployment/ReplicaSet
kubectl delete pod my-app-57f9cc845b-8pgbv


# Dry run a deployment (client-side validation without applying)
kubectl create deployment my-app --image=nginx --dry-run=client

# Generate deployment YAML definition without applying to cluster
kubectl create deployment my-app --image=nginx --dry-run=client -o yaml

# Create a deployment with specified replica count
kubectl create deployment my-app --image=nginx --replicas=3

# List deployments
kubectl get deploy

# List replica sets
kubectl get replicaset

