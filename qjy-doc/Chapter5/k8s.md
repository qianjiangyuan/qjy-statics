# 5.1: k8s操作

可以在dev machine上进行所有节点的k8s操作。

```
# 查看kube-system的namespace下的pods
./deploy.py kubectl get pods -n kube-system

# 查看pods
./deploy.py kubectl get pods

# 查看daemonsets
./deploy.py kubectl get daemonsets

# 查看nodes
./deploy.py kubectl get nodes

# verbose参数用来打印完成的
./deploy.py --verbose kubectl get nodes

# 查看一个pod
/deploy.py kubectl describe pod collectd-node-agent-2vz68

# 查看一个pod的日志
./deploy.py kubectl log pod collectd-node-agent-2vz68

# 进入一个pod
./deploy.py kubectl exec -ti collectd-node-agent-2vz68 /bin/bash

# k8s启停服务
./deploy.py kubernetes stop jobmanager
./deploy.py kubernetes start jobmanager
```

