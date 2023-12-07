# DQL 分组查询 (group by)


## 语法

`select` 字段列表 `from` 表名 [`where` 条件] `GROUP BY` 分组字段名 [`HAVING` 分组后的过滤条件];


## where与having区别

- 执行时机不同：where是分组之前进行过滤，不满足where条件，不参与分组；而having是分组之后队结果进行过滤。
- 判断条件不同：where不能对聚合函数进行判断，而having可以。

## 注意

- 执行顺序：where > 聚合函数 > having
- 分组之后，查询的字段一般为聚合函数和分组字段，查询其他字段无任何意义。

## 示例

-- 分组查询

-- 1. 根据性别分组，统计男性员工 和 女性员工数量

    select gender, count(*) from emp group by gender;


-- 2. 根据性别分组，统计男性员工 和 女性员工的平均年龄

    select gender, avg(age) from emp group by gender;


-- 3. 查询年龄小于45的员工，并根据工作地址分组，获取员工数量大于等于3的工作地址

    select workaddress, count(*) address_count from emp where age < 45 group by workaddress having address_count >= 3;
