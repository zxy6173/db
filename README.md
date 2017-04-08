# 数据库数据

## 简介

front是测试项目中使用的数据库。

## 导入方法

1. 拉取一个mongodb的镜像。

```
    docker pull mongo
```

2. 启动一个装有mongodb数据库的容器。
    
```
    //将数据文件下载到本地的一个指定目录，再将该目录挂载到运行容器中。
    docker run -d --name mongo -p 27017:27017 -v [本地目录]:/data/db mongo
```
    
3. 进入该容器。

docker exec -it mongo /bin/bash

4. 导入数据。

mongorestore -d front --dir /data/db/front



