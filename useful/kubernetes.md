# Handy Kubernetes checks

## Curl from inside K8s

Run this:

```powershell
kubectl run mycurlpod --image=curlimages/curl -i --tty -- sh
```

You should now get a command prompt and be able to run `curl` commands from within the cluster you installed this onto.

If you exit and want to reattach then just do this:

```powershell
kubectl attach mycurlpod -c mycurlpod -i -t
```

## Find POD

```powershell
$POD = @(kubectl get pod -l app.kubernetes.io/name=pod-name -n elekta-platform-elements -o jsonpath="{.items[0].metadata.name}")
```