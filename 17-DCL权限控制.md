# DCL 权限控制

## 权限类型

MySQL中定义了很多种权限，但是常用的就一下几种：

![DCL权限](/images/DCL权限.png)

<br>

## 权限控制

### 1. 查询权限
`SHOW GRANTS FOR` '用户名'`@`'主机名';


### 2. 授予权限
`GRANT` 权限列表 `ON` 数据库名.表名 `TO` '用户名'`@`'主机名';


### 3. 撤销权限
`REVOKE` 权限列表 `ON` 数据库名.表名 `FROM` '用户名'`@`'主机名';


<br>

## 注意
- 多个权限之间，使用逗号分隔。
- 授权时，数据库名和表名可以使用*进行通配，代表所有。

<br>

## 示例

-- 查询权限

    show grants for 'pedro'@'%';

<br>

-- 授予权限

    grant all on itcast.* to 'pedro'@'%';

<br>

-- 撤销权限

    revoke all on itcast.* from 'pedro'@'%';
