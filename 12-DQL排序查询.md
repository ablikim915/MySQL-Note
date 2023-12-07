# DQL 排序查询 （order by）

## 语法

`select` 字段列表 `from` 表名 `ORDER BY` 字段1 排序方式1, 字段2 排序方式2;


## 排序方式

- ASC：升序（默认值）
- DESC：降序


## 注意

如果是多字段排序，当第一个字段值相同时，才会根据第二个字段进行排序。


## 示例

-- 排序查询

-- 1. 根据年龄，对员工进行升序排序

    select * from emp order by age;


-- 2. 根据入职时间，对员工进行降序排序

    select * from emp order by entrydate desc;


-- 3. 根据年龄,对员工进行升序排序，年龄相同，再按照入职时间进行降序排序

    select * from emp order by age, entrydate desc;
