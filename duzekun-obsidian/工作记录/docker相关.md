# 报错信息

## case 1
```
docker login --username=wangyuan@cambricon.com docker-user.gotgo.cc:30080
Password: 
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.40/auth: dial unix /var/run/docker.sock: connect: permission denied
```
原因：没有docker权限

