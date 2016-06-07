
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
$ sudo apt-get install -y build-essential python-dev libevent-dev python-pip liblzma-dev
$ sudo pip install docker-registry

- Centos
$ sudo yum install -y python-devel libevent-devel python-pip gcc xz-devel

### 源码安装

## 上传
## 下载
## 搜索