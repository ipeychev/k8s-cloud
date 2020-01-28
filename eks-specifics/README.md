# Install

1. Get the config values and store them in a file:

```sh
$ helm show values stable/nginx-ingress > nginx-ingress-config.yaml
```

2. Install via Helm:

```sh
$ helm install dxp -f nginx-ingress-config.yaml stable/nginx-ingress
```

# Upgrade

After changing config values or when there is a new version:

1. Upgrade via Helm

# Uninstall

1. Uninstall via Helm

```sh
$ helm uninstall dxp
```