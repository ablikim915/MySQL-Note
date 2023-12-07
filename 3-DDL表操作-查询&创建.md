# DDL 查询

> 前提是，先用 `use` 指令进入的数据库里，再用此指令。

1. 查询当前数据库所有表

`show tables;`

2. 查询表结构

`desc 表名`

3. 查询指定表的建表语句

`show create table 表名`


# DDL 创建


1. 创建表

        create table 表名(
            字段1 字段1类型 [comment 字段1注释],
            字段2 字段2类型 [comment 字段2注释],
            字段3 字段3类型 [comment 字段3注释],
            
            ...
            字段n 字段n类型 [comment 字段n注释]
        ) [comment 表注释]

> 注意：[...]位可选参数，最后一个字段后面没有逗号
