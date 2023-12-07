# DDL 表操作 数据类型


> 参照 [《MySQL数据类型》](https://www.runoob.com/mysql/mysql-data-types.html)


## 数值类型

MySQL 支持所有标准 SQL 数值数据类型。

这些类型包括严格数值数据类型(INTEGER、SMALLINT、DECIMAL 和 NUMERIC)，以及近似数值数据类型(FLOAT、REAL 和 DOUBLE PRECISION)。

关键字INT是INTEGER的同义词，关键字DEC是DECIMAL的同义词。

BIT数据类型保存位字段值，并且支持 MyISAM、MEMORY、InnoDB 和 BDB表。

作为 SQL 标准的扩展，MySQL 也支持整数类型 TINYINT、MEDIUMINT 和 BIGINT。下面的表显示了需要的每个整数类型的存储和范围。

![MySQL数值类型](/images/MySQL%E6%95%B0%E5%80%BC%E7%B1%BB%E5%9E%8B.png)


### 单精度和双精度浮点数

单精度是这样的格式，1位符号，8位指数，23位小数。

![单精度浮点数](/images/%E5%8D%95%E7%B2%BE%E5%BA%A6%E6%B5%AE%E7%82%B9%E6%95%B0.png)

双精度是1位符号，11位指数，52位小数。

![双精度浮点数](/images/%E5%8F%8C%E7%B2%BE%E5%BA%A6%E6%B5%AE%E7%82%B9%E6%95%B0.png)



## 字符串类型

![MySQL字符串类型](/images/MySQL%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%B1%BB%E5%9E%8B.png)


> 注意：char(n) 和 varchar(n) 中括号中 n 代表字符的个数，并不代表字节个数，比如 CHAR(30) 就可以存储 30 个字符。

> CHAR 和 VARCHAR 类型类似，但它们保存和检索的方式不同。它们的最大长度和是否尾部空格被保留等方面也不同。在存储或检索过程中不进行大小写转换。

> char 性能好， varchar 性能比较差，原因是，varchar根据内容计算它所占用的空间，所以时间复杂度高于char。

> BINARY 和 VARBINARY 类似于 CHAR 和 VARCHAR，不同的是它们包含二进制字符串而不要非二进制字符串。也就是说，它们包含字节字符串而不是字符字符串。这说明它们没有字符集，并且排序和比较基于列值字节的数值值。

> BLOB 是一个二进制大对象，可以容纳可变数量的数据。有 4 种 BLOB 类型：TINYBLOB、BLOB、MEDIUMBLOB 和 LONGBLOB。它们区别在于可容纳存储范围不同。

> 有 4 种 TEXT 类型：TINYTEXT、TEXT、MEDIUMTEXT 和 LONGTEXT。对应的这 4 种 BLOB 类型，可存储的最大长度不同，可根据实际情况选择。



## 日期和时间类型

每个时间类型有一个有效值范围和一个"零"值，当指定不合法的MySQL不能表示的值时使用"零"值。

![MySQL日期和时间类型](/images/MySQL%E6%97%A5%E6%9C%9F%E5%92%8C%E6%97%B6%E9%97%B4%E7%B1%BB%E5%9E%8B.png)



## 练习

        create table emp (
            id int comment '编号',
            workno varchar(10) comment '工号',
            name varchar(10) comment '姓名',
            gender char(1) comment '性别',
            age tinyint unsigned comment '年龄',
            idcard char(18) comment '身份证号',
            entrydate date comment '入职时间'
        ) comment '员工表';
