# Install Platform Charts

## nginx-ingress

```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update
helm upgrade --install nginx-ingress --namespace --namespace ingress-nginx -f values/nginx-ingress.yaml ingress-nginx/ingress-nginx
```

## cert-manager

```
helm upgrade --install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --version v1.19.2 \
  --set crds.enabled=true \
  -f values/cert-manager.yaml
```
