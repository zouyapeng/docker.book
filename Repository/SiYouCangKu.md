
# 私有仓库

## 安装
### 容器安装
```bash
# 没有国外服务器的用户建议先使用pull下镜像
$ docker pull registry

$ docker run -d -p 5000:5000 -v /opt/registry:/tmp/registry registry
```
### Packages安装
- Ubuntu
```bash
$ sudo apt-get install -y build-essential python-dev libevent-dev python-pip liblzma-dev
$ sudo pip install docker-registry
```

- Centos
```bash
$ sudo yum install -y python-devel libevent-devel python-pip gcc xz-devel
$ sudo python-pip install docker-registry
```

## 其他更多查考我的wiki
