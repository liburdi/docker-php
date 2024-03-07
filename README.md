### setup0
更换国内镜像源
```
vim etc/docker/daemon.json



{
    "registry-mirrors":["https://docker.mirrors.ustc.edu.cn"]
}



```

### setup1

```
 mv docker-php/* project's path
 cd project's path
```

### setup2

```
vim docker/nginx/default.conf
```


### setup3

```
 docker-compose up
```
