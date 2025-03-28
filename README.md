## openmiddleware
开放中间件

## 云原生中间件，让中间件运维更简单

基于operator-sdk开发的常用中间件operator,简化中间件部署、运维、备份、监控。
## 目前已支持的中间件如下：
微服务治理中间件:
zookeeper
消息队列中间件:
kafka


## 开发流程

operator-sdk init --domain openmiddleware.com --repo github.com/openmiddleware/xxx-operator

operator-sdk create api --group db --version v1alpha1 --kind xxxCluster --resource --controller

