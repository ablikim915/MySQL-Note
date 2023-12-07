# DQL 分页查询（limit）

## 语法

`select` 字段列表 `from` 表名 `LIMIT` 起始索引, 查询记录数;


## 注意

- 起始索引从0开始，`起始索引 = (查询页码 - 1) * 每页显示记录数`。
- 分页查询是数据库的`方言`，不同的数据库有不同的实现，`MySQL中是limit`。
- 如果查询的是第一页数据，起始索引可以省略，直接简写为 `limit 10`。


## 示例

-- 分页查询

-- 1. 查询第1页员工数据，每页展示10条记录

    select * from emp limit 0,10;

    select * from emp limit 10;


-- 2. 查询第2页员工数据，每页展示10条记录

    select * from emp limit 10,10;
