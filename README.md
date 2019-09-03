# k8s-app-dep-env-php-and-java-demo

k8s 部署 java和php dome
 
> * 1.首先先部署harbor 环境
> * 2.在配置好mvn和jdk环境
> * 3.在docker 配置里面添加
- /etc/docker/daemon.json
#
 {
"insecure-registries": ["192.168.1.1"]
}
#
 # 重启docker
 # systemctl daemon-reload
 # systemctl restart docker
 # docker login --username=admin 192.168.1.1
  
 - 推送试一下：
  ## docker push 192.168.1.1/project/java:latest
#
- mvn clean package
- docker build .  harborIP/project/java:v1
- docker login  harborIP 输入账号以及密码
- docker push harborIP/project/java:v1
