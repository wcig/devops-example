# Jaeger example

## 1. Docker install

```shell
docker run -d --name jaeger -p 5775:5775/udp -p 16686:16686 -p 14250:14250 -p 14268:14268 jaegertracing/all-in-one:1.48.0
```

## 2. Docker compose install

* [docker-compose.yml](docker-compose.yml)
* [docker-compose-arm64.yml](docker-compose-arm64.yml)
