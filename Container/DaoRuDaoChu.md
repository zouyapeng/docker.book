# 导入导出

## 导入
```bash
$ sudo docker export [container id or name] > export.tar
```

## 导出
```bash
cat export.tar | sudo docker import - test/ubuntu:v1.0
```