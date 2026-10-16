# task-manager-config

Kubernetes configuration (GitOps) for the Task Manager API.

## Environments
| Folder | Namespace |
|---|---|
| `staging/` | `staging` |

## One-time setup (secrets are NOT stored in Git)
kubectl create namespace staging
kubectl create secret generic task-manager-api-secrets -n staging --from-literal=JWT_SECRET=<a-long-random-secret>

## Deploy manually
kubectl apply -k staging/