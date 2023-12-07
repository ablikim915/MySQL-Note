# DML数据操作语言

`DML` 英文全称是 Data Manipulation Language(`数据操作语言`)，用来对数据库中表的数据记录进行`增删改`操作

- 添加数据（insert）
- 修改数据（update）
- 删除数据（delete）


## 添加数据 - insert

1. 给指定字段添加数据

```
    insert into 表名 (字段名1, 字段名2, ...) values (值1, 值2, ...);
```

> 示例： insert into employee (id, workno, name, gender, age, idcard, entrydate) VALUES (1,'1','Itcast','男', 12, '123456789123456789', '2011-11-22');



2. 给全部字段添加数据

```
    insert into 表名 values (值1, 值2, ...);
```

> 示例：insert into employee values (2, '22', 'monkey', '男', 16, '123456789123456781', '2018-06-13')


3. 批量添加数据

```
    insert into 表名 (字段名1, 字段名2, ...) values (值1, 值2, ...), (值1, 值2, ...), (值1, 值2, ...);
```
```
    insert into 表名 values (值1, 值2, ...), (值1, 值2, ...), (值1, 值2, ...);
```

> 示例：insert into employee values (3, '33', '成龙', '男', 66, '123452389123456781', '1999-06-12'), (4, '44', '喵喵', '女', 17, '123452389124356781', '2023-06-12');
