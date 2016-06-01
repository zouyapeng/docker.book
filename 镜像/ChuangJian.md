# 创建(Dockerfile)
# 创建Ubuntu基础镜像
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

