# bitwardenrs-k3s

A kubectl YAML to deploy a BitwardenRS-Server on a Kubernetes Stack

## Post-Installation

You can tune the prod or dev Kustomize Overlay with :
- bitwarden-deployment.yaml : to match your storage driver (in my example I use a NFS driver),
- bitwarden-ingressroute.yaml : to match your FQDN.

## Installation 

```bash
git clone https://github.com/kyzdev/bitwardenrs-k3s
cd bitwardenrs-k3s
kubectl apply -k overlays/prod
```
## Uninstallation

```bash
kubectl delete namespace prod-bitwarden
```