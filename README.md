# 使用kubernetes部署单节点mysql
##注意：该项目主要是通过使用kubernetes部署单节点mysql.
###1,mysql镜像步骤如下：
####docker  build  -t 171518784/mysql  .
####2,生成镜像171518784/mysql，并上传至dockerhub ，使用命令：
####  docker push 171518784/mysql
####3,创建pod命令：
#### kubectl  create  -f mysql-rc.yaml
#### kubectl  create  -f mysql-service.yaml
#### 不需要再创建mysql.yaml,该pod类型已经写在replicationController中。
####4,使用命令kubectl get svc查看pod运行的状况。
####5,进入pod查看mysql运行状态，命令：
#### kubectl exec -ti  podName /bin/bash
#### 执行命令：mysql -u root -p mysql

