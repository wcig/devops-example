# Clickhouse example

## 1. Docker

配置参数:
* 8123: HTTP 端口
* 9000: TCP 端口
* ulimit: 指定了最大可以打开的文件数量

运行命令:

```shell
# 不挂载卷
docker run -d \
  --name clickhouse \
  -p 8123:8123 \
  -p 9000:9000 \
  --ulimit nofile=262144:262144 \
  clickhouse/clickhouse-server:24.2-alpine

# 挂载卷
docker run -d \
  --name clickhouse \
  -p 8123:8123 \
  -p 9000:9000 \
  -v /opt/apps/clickhouse/data:/var/lib/clickhouse/ \
  -v /opt/apps/clickhouse/logs:/var/log/clickhouse-server/ \
  --ulimit nofile=262144:262144 \
  clickhouse/clickhouse-server:24.2-alpine
```

## 2. Docker compose

参考文件 docker-compose.yml
