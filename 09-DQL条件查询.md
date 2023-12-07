# DQL 条件查询 (where)

## 语法

- `select` 字段列表 `from` 表名 `where` 条件列表

![比较运算符](/images/比较运算符.png)

![逻辑运算符](/images/逻辑运算符.png)


## 示例

-- 条件查询

-- 1. 查询年龄等于 88 的员工

    select * from emp where age = 88;

-- 2. 查询年龄小于 20 的员工信息

    select * from emp where age < 20;

-- 3. 查询年龄小于等于 20 的员工信息

    select * from emp where age <= 20;

-- 4. 查询 没有身份证号 的员工信息

    select * from emp where idcard is null;

-- 5. 查询 有身份证号 的员工信息

    select * from emp where idcard is not null;

-- 6. 查询年龄不等于 88 的员工信息

    select * from emp where age != 88;

    select * from emp where age <> 88;

-- 7. 查询年龄在15岁（包含）到 20岁（包含）之间的员工信息

    select * from emp where age >= 15 && age <= 20;

    select * from emp where age >= 15 and age <= 20;

    select * from emp where age between 15 and 20;


-- 8. 查询性别为 女 且年龄小于 25岁的员工信息

    select * from emp where gender = '女' && age < 25;

-- 9. 查询奈年龄等于18 或者 20 或者 40 的员工信息

    select * from emp where age = 18 || age = 20 || age = 40;

    select * from emp where age = 18 or age = 20 or age = 40;

    select * from emp where age in(18,20,40);


-- 10. 查询姓名为两个字的员工信息

    select * from emp where name like '__';

-- 11. 查询身份证号最后一位X的员工信息

    select * from emp where idcard like '%X';
