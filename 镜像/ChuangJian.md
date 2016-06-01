# 创建(Dockerfile)
## 创建Ubuntu基础镜像
```bash
$ sudo [debootstrap](https://wiki.debian.org/Debootstrap) trusty trusty > /dev/null
$ sudo tar -C trusty -c . | docker import - trusty

$ docker run raring cat /etc/lsb-release
```

