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

#### 4.查询常量值

    SELECT 100;

#### 5.查询表达式

    SELECT 100*98;

#### 6.查询函数

    SELECT VERSION();

#### 7.起别名

    好处：
        1.便于理解
        2.如果要查询的字段有重名的情况，可以使用别名区分
    
    方式一、使用AS

    SELECT last_name AS 姓，first_name AS 名 FROM employees;

    方式二、使用空格

    SELECT last_name 姓,first_name 名 FROM employees;

#### 8.去重

    SELECT DISTINCT department_id FROM employees;

#### 9.+号的作用

    仅仅只有一个功能：运算符

    SELECT 100+90;  
    两个操作数都为数值时，则做加法运算

    SELECT '123'+9;
    其中一方为字符型，会试图将字符型转换成数值型，如果成功，在做加法运算

    SELECT 'Jhon'+90;
    如果转换失败则将字符型转换为0

    SELECT NULL+0;
    只要有其中一方为NULL，则结果必为NULL

### 条件查询

    语法：
        SELECT 查询列表 FROM 表名 WHERE 筛选条件
    
    分类:
        一、按条件表达式筛选
            条件运算符：< > = <> >= <=

        二、按逻辑表达式筛选
            逻辑运算符：&& || ！ 
            作用：用于连接条件表达式。

        三、模糊查询
            LIKE
            BETWEEN AND
            IN
            IS NULL

#### 1.条件表达式查询

    SELECT * FROM employees WHERE salary>12000;

    SELECT last_name,department_id FROM employees WHERE department_id<>90;

#### 2.按逻辑表达式查询

    SELECT last_name,salary,commission_pct
    FROM employees
    WHERE salary>=10000 AND salary<=20000;

    SELECT *
    FROM employees
    WHERE department_id<=90 OR department_id>=110 OR salary>15000;

    SELECT *
    FROM employees
    WHERE NOT(department_id>90 AND department_id<110) OR salary>15000;




