# ArgoCD

Continuos Delivery tool for kubernetes.

## Prerequisite

- kubectl
- Kubernetes cluster
- Cluster admin level access
- kubeconfig configured to point to cluster
- Access to a git repository

## Kind

I am using kind to create a kubernetes cluster in Docker.

```powershell
choco install kind -y
```

Create a cluster

```powershell
kind create cluster --name argocd-playground
```

## Installing ArgoCD

Once you have a cluster you can simply install ArgoCD with `kubectl apply`

### Installing ArgoCD cli

```powershell
choco install argocd-cli -y
```

Access the UI by port forwarding and accessing on localhost:8080

```powershell
kubectl port-forward svc/argocd-server -n argocd 8080:443

## Get the password, in bash]
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```
