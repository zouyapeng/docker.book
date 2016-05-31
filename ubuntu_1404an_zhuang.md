# Ubuntu 14.04安装
## 准备
- Docker需要64位的操作系统
- Linux kernel 版本不得低于3.10

### 跟新源
```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates
```

### 添加GPG key
```bash
$ sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
```

### 检查docker.list
```bash
$ sudo vim /etc/apt/sources.list.d/docker.list 
```
修改内容：
```bash
# Ubuntu 16.04安装
## 准备
- Docker需要64位的操作系统
- Linux kernel 版本不得低于3.10

### 跟新源
```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates
```

### 添加GPG key
```bash
$ sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
```

### 检查docker.list
```bash
$ sudo vim /etc/apt/sources.list.d/docker.list 
```
修改内容：
```bash
# Ubuntu 16.04安装
## 准备
- Docker需要64位的操作系统
- Linux kernel 版本不得低于3.10

### 跟新源
```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates
```

### 添加GPG key
```bash
$ sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
```

### 检查docker.list
```bash
$ sudo vim /etc/apt/sources.list.d/docker.list 
```
修改内容：
```bash

```

### 跟新docker源
```bash
$ sudo apt-get update
```

## 安装
- 安装docker
```bash
$ sudo apt-get install docker-engine
```

- 启动服务
```bash
$ sudo service docker start
```

- 测试
```bash
$ sudo docker run hello-world
```



```

### 跟新docker源
```bash
$ sudo apt-get update
```

## 安装
- 安装docker
```bash
$ sudo apt-get install docker-engine
```

- 启动服务
```bash
$ sudo service docker start
```

- 测试
```bash
$ sudo docker run hello-world
```



```

### 跟新docker源
```bash
$ sudo apt-get update
```

## 安装
- 安装docker
```bash
$ sudo apt-get install docker-engine
```

- 启动服务
```bash
$ sudo service docker start
```

- 测试
```bash
$ sudo docker run hello-world
```




