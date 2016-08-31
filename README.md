# Alpine Linux Etcd3 Docker Container
[![Docker Stars](https://img.shields.io/docker/stars/wolfdeng/etcd-docker.svg)](https://hub.docker.com/r/wolfdeng/etcd-docker/)
[![Docker Pulls](https://img.shields.io/docker/pulls/wolfdeng/etcd-docker.svg)](https://hub.docker.com/r/wolfdeng/etcd-docker/)
[![Image Size](https://img.shields.io/imagelayers/image-size/wolfdeng/etcd-docker/latest.svg)](https://imagelayers.io/?images=wolfdeng/etcd-docker:latest)
[![Image Layers](https://img.shields.io/imagelayers/layers/wolfdeng/etcd-docker/latest.svg)](https://imagelayers.io/?images=wolfdeng/etcd-docker:latest)

利用Alpine Linux打造的小体积的ETCD Docker镜像。

### 使用方式：

获取docker镜像

```
docker pull wolfdeng/etcd-docker
```

获取etcd discovery的链接

```
curl https://discovery.etcd.io/new?size=3
```


启动docker

```
 docker run --name etcd -d -p 2379:2379 -p 2380:2380 -p 4001:4001 -p 7001:7001 -v ~/temp/data0/etcd:/data wolfdeng/etcd-docker --advertise-client-urls http://0.0.0.0:4001 --initial-advertise-peer-urls http://0.0.0.0:7001 --discovery=https://discovery.etcd.io/blahblahblahblahblahblah
```
