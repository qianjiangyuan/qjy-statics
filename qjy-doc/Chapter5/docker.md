# 5.3: Docker

#### Dockerfile指令

| 指令          | 功能                                   |
| ------------- | -------------------------------------- |
| FROM          | 基础镜像，相当于base                   |
| FROM …… AS xx | 同FROM，后面使用可以拿xx作为别名       |
| ARG           | 定义变量，ARG xx = 11，后面可以用${xx} |
| ENV           | 定义环境变量                           |
| RUN           | 执行语句                               |
| COPY          | copy进容器内的目录。现有目录下文件     |
| ADD           | 添加进容器，压缩包                     |
| WORKDIR       | 定义工作路径，执行RUN先会进入WORKDIR   |
| ENTRYPOINT    | 镜像入口，Docker run就会执行这个语句   |
| MAINTAINER    | author信息                             |

#### Docker基本操作	

[不做累述](https://www.runoob.com/Docker/Docker-command-manual.html)