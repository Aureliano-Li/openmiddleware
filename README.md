## openmiddleware
开放中间件

## 云原生中间件，让中间件运维更简单

基于operator-sdk开发的常用中间件operator,简化中间件部署、运维、备份、监控。
## 目前已支持的中间件如下：
微服务治理中间件: Microservice Middleware,msm  
zookeeper
nacos
apollo

消息队列中间件:Message Queue,mq  
kafka
rocketmq
pulsar

存储：Storage,stg  
minio
bookkeeper

数据库：Database,db  
mysql
postgresql


## 开发流程

operator-sdk init --domain openmiddleware.com --repo github.com/openmiddleware/xxx-operator

operator-sdk create api --group db --version v1alpha1 --kind xxxCluster --resource --controller

## 中间件operator开发基本逻辑
1. pod都是会重启的，因此不能依赖非pvc的存储
2. 配置文件有两种处理方式，一是每次启动pod时，使用初始化容器通过脚本生成；二是将配置文件保存到pvc里。
3. 通过sts启动的pod，每个pod配置都是一样的，包括镜像、命令、环境变量


