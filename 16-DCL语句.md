# DCL 语句

## DCL 介绍

DCL英文全称是`Data Control Language`(数据控制语言),用来管理数据库`用户`、控制数据库的`访问权限`。

<br>

## DCL 管理用户

### 1. 查询用户

`USE` mysql;

`SELECT` * `FROM` user;


### 2. 创建用户

`CREATE USER` '用户名'`@`'主机名' `IDENTIFIED BY` '密码'; 

### 3. 修改用户密码

`ALTER USER` '用户名'`@`'主机名' `IDENTIFIED WITH` mysql_native_password `BY` '新密码'; 


### 4. 删除用户

`DROP USER` '用户名'`@`'主机名';


<br> 

## 注意

- 主机名可使用 % 通配。
- 这类SQL开发人员操作的比较少，主要是DBA（Database Administrator 数据库管理员）使用。 


<br>

## 示例

-- 创建用户 itcast， 只能在当前主技localhost访问，密码123456

    create user 'itcast'@'localhost' identified by '123456';
<br><br>

-- 创建用户 pedro，可以在任意主机访问该数据库，密码123456；

    create user 'pedro'@'%' identified by '123456';
<br><br>


-- 修改用户 pedro 的访问密码为 1234；

    alter user 'pedro'@'%' identified with mysql_native_password by '1234';
<br><br>


-- 删除itcast@localhost用户

    drop user 'itcast'@'localhost';
