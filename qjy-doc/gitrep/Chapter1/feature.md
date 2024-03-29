# 1.3：平台特点

使用我们的钱江源平台，你可以：

- 进行多种框架的深度学习训练

- 开箱即用，免去安装环境和依赖的繁琐

- 使用平台共享目录下的数据集，免去下数据集的时间

- 使用平台用户分享的一些结果和经验

- 使用平台提供的GPU共享资源

- 为开源项目添砖加瓦

  

### 特点

#### 1.开箱即用同时也支持用户自定义部署

通过Docker容器及微服务架构方便AI工程师开箱即用或根据用户需求自定义快速部署计算环境（通过下载官方发布的Docker容器如tensorflow可以达到秒级部署的效果）

比如钱江源平台中的tensorflow Docker里包括有:

- 所有的tensorflow所需的二进制包，如curl、libpng、libzmq、zip等

- Python(带有pip工具，jypyer、numpy、scipy、sklean...)

- 专用的cuda库

  

#### 2.尽可能好的利用节点的计算资源

通过kubernetes管理服务器集群可以帮助AI科学家更好地利用硬件资源：科学家们只需要提供计算资源需求描述，钱江源平台将根据这些需求描述和每个节点上的可用资源寻找最合适的节点来提供服务。而科学家们不必了解自己的计算是在哪个服务器上运行。利用kubernetes合理的调度算法可以确保整个集群的各个节点的硬件资源都得到尽可能好的利用。

多租户使用时，通过job来管理每个租户的开发环境，当计算任务完成时或者用户自定义kill job后， 本次Job的所申请的GPU等资源都将交还给集群，方便二次使用。

#### 3.健康检查和自修复

随着集群大小的增加，计算机组件将需要频繁处理出现故障的情况，QianJiangYuan平台提供了[](https://qjy-proxy01.zhejianglab.com/grafana)插件方便科学家及开发人员对节点的GPU等基础设施进行实时健康检查，当节点出现故障时，集群会优先自动将计算任务调度到其他节点继续运行而不用人工手动处理，保证了计算任务的安全性。