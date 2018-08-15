- 安装命令
我们把registry的数据挂在/opt/data下面
```
docker pull registry
docker run -d -p 5000:5000 -v /data/registry:/var/lib/registry registry
```
- 客户端连接registry的时候需要
添加一个文件/etc/docker/daemon.json，内容如下
```
echo '{ "insecure-registries":["registry.jr.glodon.com:5000"] }'>> /etc/docker/daemon.json

```



在各个机器都配的dns或者hosts指向这台机器