# 4.4: RestfulAPI	

#### 原理介绍

采用了flask的框架，python3的环境。

flask是python的轻量级web框架。

通过 flask_restful 库的 Api, Resource 可以快速生成restful的api。

#### 请求完整路径

完整链路：

1. 浏览器端发起请求，比如https://qjy-proxy01.zhejianglab.com/api/dlws/ListJobs?num=20 。
2. 域名解析，域名-公网ip-内网ip（qjy-proxy01）的节点，在nginx中，进入/的匹配规则，请求转入webui2的服务。
3. 在webui2的服务中，在dlwsController中，进入/api/[controller]的匹配规则，从而去掉了/api/dlws的contextpath，在controller中，拼接得到了restfulapi的url，并进行了访问。
4. 在restfulapi的服务中，接收到了请求，并进行了返回。

图示：

![./images/request.png](..\images\request.png)

#### 对应源码

在/src/RestApi下，主代码都在dlwsrestapi.py内。

#### flask文档

[文档](http://docs.jinkan.org/docs/flask/)

#### API接口整理

和前端功能上的增删改查是一一对应的，具体待整理。

提供的主要Api有以下这些

- 处理前端请求
- 创建Job
- 获得Job列表
- 删除Job
- 获得某个Job的详情
- 获得集群的状态
- 批准Job...

