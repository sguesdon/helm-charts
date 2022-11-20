# prometheus-otiohome-exporter

[Latest release](https://img.shields.io/badge/dynamic/json.svg?label=Latest%20release&url=https://sguesdon.github.io/helm-charts/index.json&query=$[%27prometheus-otiohome-exporter%27].latest&logo=helm&logoColor=white)

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
