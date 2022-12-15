# Projects/Environments
This directory contains all of your `argocd-autopilot` projects. Projects provide a way to logically group applications and easily control things such as defaults and restrictions.As part of the Universal Directory Structure, it is equivalent to `environments` which defines security rules, code generator (e.g. ApplicationSet) for deployment code (e.g. applications.argoproj.io), and destinations (aka Clusters)

### Creating a new project/environment
To create a new project run:
```bash
export GIT_TOKEN=<YOUR_TOKEN>
export GIT_REPO=<REPO_URL>

argocd-autopilot project create <PROJECT_NAME>
```

### Creating a new project on different cluster
You can create a project that deploys applications to a different cluster, instead of the cluster where Argo-CD is installed. To do that run:
```bash
export GIT_TOKEN=<YOUR_TOKEN>
export GIT_REPO=<REPO_URL>

argocd-autopilot project create <PROJECT_NAME> --dest-kube-context <CONTEXT_NAME>
```
Now all applications in this project that do not explicitly specify a different `--dest-server` will be created on the project's destination server.
