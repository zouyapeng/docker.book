# 启动
## hello world
```bash
$ docker run hello-world
```

## 交互模式
```bash
$ docker run -it ubuntu:14.04 /bin/bash
root@57064404d74b:/#

# -t 分配一个伪终端(pseudo-tty)并绑定到容器的标准输入上
# -i 标准输入保持打开
```