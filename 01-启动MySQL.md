# 启动MySQL

## 启动和停止

启动： net stop mysql80
停止： net start mysql80

> `mysql80` 是安装MySQL的时候填写的 `Windows 服务名`

## 连接数据库

1. 用MySQL自带的命令行工具登录

打开工具之后直接输入密码登录。

2. 用系统自带的命令行工具登录（cmd）

`mysql [-h 127.0.0.1] [-P 3306] -u root -p`
