### 基础查询

    语法：
        SELECT 查询列表 From 表名
    特点：
        1.查询列表可以是：表中的字段、常量值、表达式、函数
        2.查询的结果是一个虚拟的表格

#### 1.查询表中的单个字段

    SELECT last_name From employees;

#### 2.查询表中的多个字段

    SELECT last_name,salary,email From employees;

#### 3.查询表中的所有字段

    SELECT * From employees;
