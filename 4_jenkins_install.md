jenkins

拉取镜像
```
docker pull jenkins:2.60.3
```
创建目录
```
mkdir /data/jenkins_home
chmod 777 /data/jenkins_home
```
启动jenkins
```
docker run -d -u root -p 7080:8080 -p 50000:50000 \
--env JAVA_OPTS="-Dpermissive-script-security.enabled=true -Xmx400m" \
-v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/usr/bin/docker:ro \
-v /usr/lib64/libltdl.so.7:/usr/lib/x86_64-linux-gnu/libltdl.so.7  \
-v /data/jenkins_home:/var/jenkins_home -e JAVA_OPTS=-Duser.timezone=Asia/Shanghai jenkins:2.60.3
```
到/data/jenkins_home/secrets目录下，查看密码
```
cat /data/jenkins_home/secrets/initialAdminPassword
```
用这个密码登录jeckins
设置密码用户均为admin
安装推荐的插件，另外再安装maven插件


