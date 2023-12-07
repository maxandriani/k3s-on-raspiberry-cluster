# Cert Manager

**CERT-MANAGER NUNCA VAI FUNCIONAR EM UM AMBIENTE OFFLINE!!!**

https://cert-manager.io/docs/installation/


helm repo add jetstack https://charts.jetstack.io
helm repo update

kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.12.0/cert-manager.crds.yaml


helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --set installCRDs=true
  # --version v1.12.0 \
  # --set installCRDs=true


helm install cert-manager jetstack/cert-manager  --namespace cert-manager --create-namespace --set installCRDs=true

