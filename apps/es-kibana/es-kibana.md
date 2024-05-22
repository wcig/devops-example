# Elasticsearch-Kibana example

## 1. Docker install

```shell
docker network create network-es-kibana

docker run -d --name elasticsearch --net network-es-kibana -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -e "ES_JAVA_OPTS=-Xms512m -Xmx512m" elasticsearch:7.17.13

docker run -d --name kibana --net network-es-kibana -p 5601:5601 kibana:7.17.13
```

## 2. Docker compose install

* [docker-compose.yml](docker-compose.yml)
