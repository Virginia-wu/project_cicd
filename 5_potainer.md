把potainer的数据挂载到/opt/portainer
启动命令
```
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v /data/portainer:/potainerdata portainer/portainer
```
选local,密码admin123