---
title: Docker 容器在 Linux 环境下访问宿主机 IP
date: 2024-01-25 16:59:43
tags:
  - Docker
  - Linux
  - NetWork
---

如果是 Docker Compose 的方式，直接在 docker-compose.yml 文件中添加下面的配置即可。

```yaml
extra_hosts:
  - "host.docker.internal:host-gateway"
```

这样容器内部可以通过域名 `host.docker.internal` 解析出宿主机 IP 地址。
