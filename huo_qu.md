# 获取

可以使用docker pull 命令来从仓库获取所需要的镜像。

下面的例子将从Docker Hub仓库下载一个Ubuntu 14.04操作系统的镜像。

```bash

```
该命令实际上相当于
```bash
$ sudo docker pull docker.io/ubuntu:14.04
```
即从官方仓库注册服务器获取镜像。

14.04为镜像的tag。

有时候官方仓库注册服务器下载较慢，甚至不能下载,这时可以从其他仓库下载或者翻墙。
