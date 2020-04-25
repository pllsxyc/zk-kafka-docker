## 部署方法：
### 直接docker-compose -f zk-kafka-docker-compose.yml up -d一整套系统就能全部跑起来，但是这个时候只有一个kafka节点
### 然后执行docker-compose -f zk-kafka-docker-compose.yml scale kafka=3 启动三个kafka节点。
### 一个3节点zookeeper和三节点kafka，一个kafka-manager,一个kafkaoffsetmonitor的容器集群就出来了，作为一个开发环境非常适合。
### kafka-manager和kafkaoffsetmonitor两个镜像我push到个人的docker hub上了，Dockerfile也非常简单。放在这里。

## 注意：
### 把yml文件中的 KAFKA_ADVERTISED_HOST_NAME 参数改成自己的内网地址