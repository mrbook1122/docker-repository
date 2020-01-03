# yapi部署

## mongodb

1.创建mongo数据卷
> docker volume create mongo

2.启动mongo，指定自己网络

> docker run --name mongo -v mongo:/data/db -d --network my-net mongo

## yapi

1.构建安装镜像
> docker build -t yapi-install .

2.创建卷
> docker volume create yapi

3.初始化
> docker run --rm -v --name yapi-install yapi:/my-yapi --publish 9090:9090 -d --network my-net yapi-install

4.构建yapi
> docker build -t yapi .

5.启动yapi
> docker run --name yapi -v yapi:/my-yapi --publish 5050:3000 --network my-net -d yapi
