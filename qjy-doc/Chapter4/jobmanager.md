# 4.6:JobManager

#### 原理介绍

采用了flask的框架，python3的环境。

flask是python的轻量级web框架。

通过 cluster_manger 启动了五个管理任务，分别是job、user、node、joblog、command，一直在对SQL数据库进行间隔为1s的任务轮询，检测到待处理状态的任务，则进行相应的操作。

- user，当检测到有新用户，则在存储节点进行相应的路径预设和权限处理。
- node，返回节点的最新状态，如name，labels, gpu_allocatable,gpu_capacity,gpu_used,InternalIP,pods等信息。
- job, 当检测到有待处理的job时，进行操作。
- joblog，存储日志
- command，当检测到有未执行的command的时候，执行。

tips:

里面涉及节点相关的操作都是通过kubectl去实现的，具体查看k8sUtils的脚本。



#### 对应源码

在/src/ClusterManager下，入口文件为cluster_manger.py，其他五个任务分别对应五个文件。

#### flask文档

[文档](http://docs.jinkan.org/docs/flask/)

