# zhdl_erp


## 参考文档
https://gitee.com/jishenghua/JSH_ERP/tree/master

## 部署方法
1. redis、mysql安装步骤忽略，请参考文档。
```shell
docker run --network host -d  -v /opt/mysql/data:/var/lib/mysql -v /opt/mysql/conf/:/etc/mysql -e MYSQL_ROOT_PASSWORD=20210819 -p 3306:3306 --name mysql mysql:5.7.25
```
2. 安装后端程序
```shell
cd jshERP-boot/ && docker run --network host -d -Published 9999:9999 --name backend backend:v1
```
3. 安装前端程序
```shell
cd jshERP-web/ && docker run --network host -d -p 80:80 --name front front:v1
```


