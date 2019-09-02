# 4.3: webUI

#### 原理介绍

采用了asp.net core2.0的框架，在前端实现上使用了angularJS，jQuery，bootstrap来进行了功能和样式的完善。

asp.net core2.0是MVC的结构，View层进行视图的渲染，Controller层进行逻辑的控制，Model层更像是interface，定义了几个模型的字段，来规范http请求接口的输入输出。

前端模块实现功能：

1. 认证授权
2. 账户管理：增（首次登录自动增为用户）、查（列表查看）、改（权限调整）。
3. 任务管理：增（submit），删（kill），查（列表和单个job查看）、改（approve）。
4. 集群管理：查（查看集群各节点状态）
5. 一些可视化查看

tips:

- WebPortal，也指webUI的模块，webportal是asp.net core中的一个专有名词

#### 对应源码

在/src/WebUI2下，webui和webui2都是前端代码，区别是一个用asp.net core1.0，一个是asp.net core2.0，目前平台使用的是webui2.

#### asp.net core文档

[官网中文文档](https://docs.microsoft.com/zh-cn/aspnet/core/getting-started/?view=aspnetcore-2.2&tabs=windows)

