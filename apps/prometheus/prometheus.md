# Prometheus example

## 1. Docker install

```shell
docker volume create prometheus_data

docker run -d \
  --name prometheus \
  -p 9090:9090 \
  -v ./config.yml:/etc/prometheus/prometheus.yml \
  -v prometheus_data:/prometheus \
  prom/prometheus:v2.45.0
```

## 2. Docker compose install

* [docker-compose.yml](docker-compose.yml)
