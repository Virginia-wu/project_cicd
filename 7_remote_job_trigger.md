http访问
http://{USER}:{API_TOKEN}@{JENKINS_URL}/job/{JOB}/build?token={AUTHENTICATION_TOKEN}
就可以
USER是远程jenkins的用户名
API_TOKEN远程jenkins用户对应的API_TOKEN
JOB是远程jenkins job的名字
AUTHENTICATION_TOKEN是远程jenkins job配置的job token

