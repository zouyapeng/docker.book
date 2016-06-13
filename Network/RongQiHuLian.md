
# 容器互联

容器的连接（linking）系统是除了端口映射外，另一种跟容器中应用交互的方式。

该系统会在源和接收容器之间创建一个隧道，接收容器可以看到源容器指定的信息。

## 自定义容器命名
连接系统依据容器的名称来执行。因此，首先需要自定义一个好记的容器命名。

虽然当创建容器的时候，系统默认会分配一个名字。自定义命名容器有2个好处：

- 自定义的命名，比较好记，比如一个web应用容器我们可以给它起名叫web
- 当要连接其他容器时候，可以作为一个有用的参考点，比如连接web容器到db容器
使用 --name 标记可以为容器自定义命名。
```bash
$ sudo docker run -d -P --name web training/webapp python app.py
```

使用 ```docker ps``` 来验证设定的命名。
```bash
$ sudo docker ps -l
CONTAINER ID  IMAGE                  COMMAND        CREATED       STATUS       PORTS                    NAMES
aed84ee21bde  training/webapp:latest python app.py  12 hours ago  Up 2 seconds 0.0.0.0:49154->5000/tcp  web
```

也可以使用 ```docker inspect``` 来查看容器的名字
```bash
$ sudo docker inspect -f "{{ .Name }}" aed84ee21bde
/web
```
注意：容器的名称是唯一的。如果已经命名了一个叫 web 的容器，当你要再次使用 web 这个名称的时候，需要先用```docker rm``` 来删除之前创建的同名容器。+

在执行 ```docker run``` 的时候如果添加 --rm 标记，则容器在终止后会立刻删除。注意，--rm 和 -d 参数不能同时使用。
## 容器互联

