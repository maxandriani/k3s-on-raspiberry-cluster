# MetalLB

helm repo add metallb https://metallb.github.io/metallb
helm install metallb metallb/metallb

helm install metallb metallb/metallb -f values.yaml

## Install

Elevate namespace with does annotations

``` yaml
labels:
    pod-security.kubernetes.io/enforce: privileged
    pod-security.kubernetes.io/audit: privileged
    pod-security.kubernetes.io/warn: privileged
```

