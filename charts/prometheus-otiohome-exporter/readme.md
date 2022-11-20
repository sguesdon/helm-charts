# prometheus-otiohome-exporter

# add repository

```sh
helm repo add sguesdon 'https://raw.githubusercontent.com/sguesdon/helm-charts/gh-pages/'
```

# prepare install

create your own configuration

```yaml
otio:
  host: xxxxxxxxx
  profile:
    place_id: xxxxxxx
  auth:
    host: xxxxxxx
    client_id: xxxxxxx
    access_token: xxxxxxxxxx
    refresh_token: xxxxxxxxxxxx
replicaCount: 1
```

# install

```sh
helm upgrade \
  --install \
  --namespace=monitoring \
  --create-namespace \
  --values ./my-custom-config.yaml \
  prometheus-otiohome-exporter sguesdon/prometheus-otiohome-exporter
```
