# DDL 数据库、数据字段定义语句

> MySQL数据库的SQL语句不区分大小写，关键字建议使用大写

## DDL- 数据库操作

1. 查询

- 查询所有数据库

`SHOW DATABASES;`

- 查询当前处于哪个数据库

`select database();`


2. 创建

`CREATE DATABASE [IF NOT EXISTS] 数据库名 [DEFAULT CHARSET 字符集] [COLLATE 排序规则];`

> 举例：`create database if not exists test default charset utf8mb4;`

3. 删除

`DROP DATABASE [IF EXISTS] 数据库名;`

> 举例：`drop database if exists test;`

4. 使用

`USE 数据库名;`
