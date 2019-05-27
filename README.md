# docker-fastdfs

# 基于 Docker 安装 FastDFS

> https://www.funtl.com/zh/apache-dubbo-codeing/FastDFS-%E5%AE%89%E8%A3%85.html



# 开启端口
`22122` ，`23000`

# 启动容器
```shell
docker-compose up -d
```
# 测试上传
## 交互式进入容器
```shell
docker exec -it fastdfs /bin/bash
```
## 测试文件上传
```shell
/usr/bin/fdfs_upload_file /etc/fdfs/client.conf /usr/local/src/fastdfs-5.11/INSTALL
```
## 服务器反馈上传地址
```shell
group1/M00/00/00/wKhLi1oHVMCAT2vrAAAeSwu9TgM3976771
```
## 测试 Nginx 访问
```shell
http://192.168.75.128:8888/group1/M00/00/00/wKhLi1oHVMCAT2vrAAAeSwu9TgM3976771
```