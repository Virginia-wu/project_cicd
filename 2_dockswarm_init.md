#### 在其中一台机器作为master
``` 
docker swarm init
``` 
####在另外一台机器连接
类似如下命令，具体token init的时候会生成
```
docker swarm join --token SWMTKN-1-0aqsmj0e4fbbu6pxsbq3kkd4g5lm11k4iytcwxa5bs7ip9f09c-bvh4krfbt2yvytymcmaigb7y6 172.16.248.192:2377

```
这个命令可以在docker swarm init的时候查看到,连接的时候有可能会报grpc的异常，这时候检查下防火墙，关闭防火墙
或者防火墙对swarm的端口的限制关闭可以解决问题，关闭防火墙的命令
```
systemctl stop firewalld.service
systemctl disable firewalld.service

```