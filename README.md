## 方法1：自已建register:会缓存镜像，需要硬盘大
ref :https://github.com/dqzboy/Docker-Proxy?tab=readme-ov-file


```
cd docker

# 启动全部容器
docker compose up -d

# 启动指定的容器,例如: Docker Hub Registry Proxy
docker compose up -d dockerhub

# 查看容器日志
docker logs -f [容器ID或名称]
```



##方法2：使用cloudfalre的worker服务，反代理

https://github.com/ciiiii/cloudflare-docker-proxy 

参考：https://github.com/ciiiii/cloudflare-docker-proxy/issues/126

直接使用src/index.js的脚本新建一个worker 配好域名即可。