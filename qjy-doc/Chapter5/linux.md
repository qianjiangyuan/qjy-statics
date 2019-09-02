# 5.2: linux操作

本节介绍一些常用操作，介绍常用参数，具体可以查看linux的相关[资料](<https://www.runoob.com/linux/linux-command-manual.html>)。

#### 查看

```
# 文件系统的磁盘空间占用情况，通常可以查看挂载情况
df -h
```



#### 查找

​	一般用grep，用法也比较多

```
grep -r xxxxxx /usr/WebPortal 
grep -rnw . -e FAMILY_TOKEN
```



挂载

```
# 查看设备
fdisk -l

# 把设备sde1挂载成/mnt/目录
sudo mount /dev/sde1 /mnt/dlwsdata4

# 把storage下的某个目录挂载到/tmp/目录
sudo mount zjlab-storage:/mnt/dlwsdata /tmp/zjlab-storage
```



#### 安装

ubuntu环境下用apt-get

```
apt-get update
apt-get install -y xxxx
```



#### 获取

wget，参数如下

- -O，指定下载目录
- -q， 增加参数

```
wget url
```



#### 解压

1. tar

tar是用来建立，还原备份文件的工具程序，参数如下:

- -x  -x或--extract或--get 从备份文件中还原文件。 
- -z  -z或--gzip或--ungzip 通过gzip指令处理备份文件。
- -f  -f<备份文件>或--file=<备份文件> 指定备份文件。
- -C<目的目录>或--directory=<目的目录> 切换到指定的目录。
- 所以， -xzf是用来表示解压

```2
tar -xzf /tmp/java.tar.gz -C ${JAVA_HOME}
```

1. unzip

- -j 不处理压缩文件中原有的目录路径。
- -o 不必先询问用户，unzip执行后覆盖原有文件。
- -d<目录> 指定文件解压缩后所要存储的目录

```
unzip -jo -d ${JAVA_HOME}/jre/lib/security /tmp/jce_policy.zip
```



#### 基本操作

mkdir， 建目录

chmod， 改权限

rm，删除

cd，进入目录

ls，查看文件

ln，软连接



