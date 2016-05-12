# Ubuntu 16.04安装
## 准备
Docker requires a 64-bit installation regardless of your Ubuntu version. 

Additionally, your kernel must be 3.10 at minimum. 

The latest 3.10 minor version or a newer maintained version are also acceptable.
### 跟新源
```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates
```

### 添加GPG key
```bash
sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
```

### 检查docker.list
```bash
sudo vim /etc/apt/sources.list.d/docker.list 
```
修改内容：
```bash
deb https://apt.dockerproject.org/repo ubuntu-xenial main
```

### 跟新docker源
```bash
sudo apt-get update
```



