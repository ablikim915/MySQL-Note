# DML修改数据&删除

## 修改数据

```
    update 表名 set 字段名1=值1, 字段名2=值2, ... [where 条件];
```

> 注意：修改语句的条件可以有，也可以没有，`如果没有条件，则会修改整张表的所有数据`。

> 示例：
>
> -- 修改id为 1 的数据，将那么修改为 rambo
> 
> update employee set name = 'rambo' where id = 1;

> -- 修改id为 1 的数据，将name修改为 翠花，gender 修改为 女；
> 
>update employee set name = '翠花', gender = '女' where id = 1;

> -- 将所有员工的入职时间修改为 2008-08-08
> 
> update employee set entrydate = '2008-08-08';


## 删除数据

```
    delete from 表名 [where 条件];
```

> 注意：
>
> delete语句的条件可以有，也可以没有，如果没有条件，则会删除整张表的所有数据。
> 
> delete语句不能删除某一个字段的值（可以用 update）。


> 示例：
> 
> -- 删除 gender为女的员工
> 
> delete from employee where gender = '女';

> -- 删除所有员工
> 
> delete from employee;
