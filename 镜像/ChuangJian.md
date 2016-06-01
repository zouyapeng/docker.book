# 创建
## 创建Ubuntu基础镜像
```bash
$ sudo [debootstrap](https://wiki.debian.org/Debootstrap) trusty trusty > /dev/null
$ sudo tar -C trusty -c . | docker import - trusty
sha256:2c2a1ef844faf88c0fd6e188ad68e08e42ab7732071c2a41a23e287af1efdde1
$ docker run trusty cat /etc/lsb-release
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=14.04
DISTRIB_CODENAME=trusty
DISTRIB_DESCRIPTION="Ubuntu 14.04 LTS"
```

在Docker GitHub仓库里还有创建其他基础镜像的脚本的例子:

- [BusyBox](https://github.com/docker/docker/blob/master/contrib/mkimage-busybox.sh)
- CentOS / Scientific Linux CERN (SLC) on [Debian/Ubuntu](https://github.com/docker/docker/blob/master/contrib/mkimage-rinse.sh) or on [CentOS/RHEL/SLC/etc](https://github.com/docker/docker/blob/master/contrib/mkimage-yum.sh).
- [Debian / Ubuntu](https://github.com/docker/docker/blob/master/contrib/mkimage-debootstrap.sh)



## 使用Dockerfile创建镜像


```dockerfile
FROM trusty:latest

MAINTAINER Zouyapeng<zyp19901009@163.com>

ENV \
  TEST_ENV1=123456 \
  TEST_ENV2=true \
  TEST_ENV3=/var/log

RUN apt-get update && apt-get install -y \
  apache2 \
  php5
  
COPY requirements.txt /tmp/
COPY . /tmp/
ADD http://example.com/big.tar.xz /

VOLUME ["/etc/custom-config", "/var/log"]

EXPOSE 80 162/udp 10051 10052
```

