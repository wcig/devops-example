# Apollo example

A simple apollo deployment example by docker compose.

```shell
docker-compose -f docker-compose.yml up
# docker-compose -f docker-compose-arm64.yml up

docker-compose -f docker-compose.yml down
# docker-compose -f docker-compose-arm64.yml down

## notice: docker-compose version >= v2.10.2
docker-compose -v
```
Apollo login url: http://localhost:8070, default account is apollo/admin.

Reference:

* https://www.apolloconfig.com/#/zh/README
* https://github.com/apolloconfig/apollo-quick-start
