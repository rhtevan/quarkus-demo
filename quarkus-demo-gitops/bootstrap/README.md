# Bootstrap
This directory contains the deployment and operation code for bootstrapping gitops tools, in particular, ArgoCD controllers for managing not only itself but also deployment environments and destination clusters. 

### Initialize an Ignition Cluster (A lightweight cluster with gitops tools)
To run:
```bash
export GIT_TOKEN=<YOUR_TOKEN>

# Must include the path to parent directory of 'bootstrap'
# For example: https://github.com/rhtevan/quarkus-demo/quarkus-demo-gitops
export GIT_REPO=<REPO_URL>

argocd-autopilot repo bootstrap --recover
```
> For more details, See Argocd Autopilot: [recovery](https://argocd-autopilot.readthedocs.io/en/stable/Getting-Started/#recovering-argo-cd-from-an-existing-repository), and [installation](https://argocd-autopilot.readthedocs.io/en/stable/Installation-Guide/#linux-and-wsl-using-curl)

