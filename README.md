# 快速搭建php环境
<b></b>

### setup0
更换国内镜像源
```
vim /etc/docker/daemon.json



{
    "registry-mirrors":["https://docker.mirrors.ustc.edu.cn"]
}



```

### setup1
在项目目录下

```
git clone https://github.com/liburdi/docker-php.git
mv docker-php/* ./
```

### setup2

```
vim docker/nginx/default.conf
```


### setup3

```
 docker-compose up
```
