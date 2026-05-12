# argocd-declarative
- ArgoCD installation
- Installation of app of apps
- Installation of hello world application
- ArgoCD self management

# Deployment steps:
```bash
helm install argo-cd -n argocd charts/argo-cd/
kubectl get secret -n argocd argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
helm template charts/root-app/ | kubectl apply -f -
```
