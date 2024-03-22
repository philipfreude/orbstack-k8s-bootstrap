# Orbstack K8s Bootstrap

```bash
helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
helm repo update
helm upgrade --install \
  --namespace kube-system \
  --values ./metrics-server-values.yaml \
  metrics-server \
  metrics-server/metrics-server
```

```bash
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update
helm upgrade --install \
  --namespace ingress-nginx \
  --create-namespace \
  --values ./ingress-nginx-values.yaml \
  ingress-nginx \
  ingress-nginx/ingress-nginx
```
