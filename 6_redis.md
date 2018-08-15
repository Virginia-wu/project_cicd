把/data/redis/data的数据挂载到/data
启动命令
```
docker run -p 6379:6379 -v /data/redis/data:/data  -d redis:3.2 redis-server
```