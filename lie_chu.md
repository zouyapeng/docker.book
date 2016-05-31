# 列出

使用docker images显示本地已有的镜像。

```bash
zyp@work:~$ docker images 
REPOSITORY           TAG                 IMAGE ID            CREATED             SIZE
ubuntu               14.04               8f1bd21bd25c        4 days ago          188 MB
zouyapeng/dokuwiki   latest              c9bf1b678f65        2 weeks ago         266.1 MB
```

在列出信息中,可以看到几个字段信息
name | id | code
- | - | -
gitbook | 1 | nodejs
wordpress | 2 | php

REPOSITORY
TAG
IMAGE ID
CREATED
SIZE
来自于哪个仓库,比如	ubuntu
镜像的标记,比如	14.04
它的	 	ID	 	号(唯一)
创建时间
镜像大小