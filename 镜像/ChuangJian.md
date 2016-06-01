# 创建(Dockerfile)
## 创建Ubuntu基础镜像
```bash
$ sudo debootstrap trusty trusty > /dev/null
$ sudo tar -C trusty -c . | docker import - trusty
```
