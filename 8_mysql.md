### mysql 安装,选择环境centos7
###### 下载rpm
```
wget http://repo.mysql.com/mysql57-community-release-el7-11.noarch.rpm
```
###### 安装rpm
```
sudo rpm -ivh mysql57-community-release-el7-11.noarch.rpm
```
###### 安装mysql-server
```
yum install -y mysql-community-server
```
###### 编辑my.cnf
```
vim /etc/my.cnf
```
在mysqld下面增加一行skip-grant-tables
###### 重启mysql
```
service mysqld restart
```
###### 登录mysql
```
mysql -u root -p
```
输入机器root账户的密码
###### 执行mysql命令,创建密码为admin的账户，赋予比较大的权限(这里权限以及账户密码可以自行设置,%表示不限制客户端的ip，这里可以限定ip)
 ```
 mysql>create user 'admin'@'%' IDENTIFIED BY 'admin';
     >GRANT ALL on *.* TO 'admin'@'%';
 ```
 上面的语句如果遇到问题可以先执行 flush privileges;
###### 编辑my.cnf
 ```
 vim /etc/my.cnf
 ```
在mysqld下面去除刚刚加的那一行skip-grant-tables
###### 重启mysql
 ```
 service mysqld restart
```
###### mysql可以使用了

