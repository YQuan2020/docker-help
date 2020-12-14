## build 测试

### 查看image内容(默认 更换image)

#### 1. 最常见的方式是创建容器，然后金融容器的 bash 查看镜像内容
````
docker run -it --entrypoint sh nginx:latest #更换image
````


#### 2. tar包
````
docker save nginx:latest > nginx.tar
tar -xvf nginx.tar
````


#### 3. 快速启动一个容器，查看内容，然后退出并删除容器
````
docker run --rm nginx:latest ls -alR
````


#### 4. 通过[dive](https://github.com/wagoodman/dive "Title") 命令方面查看
````
dive nginx:latest
````