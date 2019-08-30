# k8s-app-dep-env-php-and-java-demo

k8s 部署 java和php dome

###1.首先先部署harbor 环境
###2.在配置好mvn和jdk环境
###3.在docker 配置里面添加
###/etc/docker/daemon.json
###{
###"insecure-registry":["harborIP"]
###}
###重启docker
### mvn clean package
### docker build .  harborIP/project/java:v1
### docker login  harborIP 输入账号以及密码
### docker push harborIP/project/java:v1
