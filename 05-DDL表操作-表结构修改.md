# DDL 表结构修改

## 添加字段

语法：

```
alter table 表名 add 字段名 类型(长度) [comment 注释] [约束];
```


> 举例： alter table emp add nickname varchar(20) comment '昵称';


## 修改字段

- 修改数据类型
    
```
    alter table 表名 modify 字段名 新数据类型(长度);
```

> 举例：alter table emp modify nickname char(20);

- 修改字段名和字段类型

```
    alter table 表名 change 旧字段名 新字段名 类型(长度) [comment 注释] [约束];
```

> 举例：alter table emp change nickname username varchar(30) comment '用户名';


## 删除字段

```
    alter table 表名 drop 字段名;
```

> 举例：alter table emp drop username;


## 修改表名

```
    alter table 表名 rename to 新表名;
```

> 举例：alter table emp rename to employee;


## 删除表

- 删除表

```
    drop table [if exists] 表名;
```

> 举例：drop table if exists tb_user;

- 删除指定表，并重新创建该表;

```
    truncate table 表名;
```

> 举例：truncate table employee;

> 注意：在删除表时，表中的全部数据也会被删除掉。
