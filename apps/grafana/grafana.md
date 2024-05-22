# Grafana example

## 1. Docker install

```shell
docker run -d \
  --name grafana \
  -p 3000:3000 \
  -v ./grafana/provisioning/datasources:/etc/grafana/provisioning/datasources \
  -v ./grafana/provisioning/dashboards:/etc/grafana/provisioning/dashboards \
  -v ./grafana/dashboards:/var/lib/grafana/dashboards \
  grafana/grafana:10.0.2
```

## 2. Docker compose install

* [docker-compose.yml](docker-compose.yml)
