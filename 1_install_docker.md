#### docker安装(centos7)
``` 
yum install -y yum-utils
yum-config-manager     --add-repo     https://download.docker.com/linux/centos/docker-ce.repo
yum install -y docker-ce.x86_64
service docker start
``` 