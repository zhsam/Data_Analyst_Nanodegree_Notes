# 优达学城 - 数据分析师(入门) ｜ Udacity- Data Analyst Term1
- [回首页](https://github.com/zhsam/Data_Analyst_Nanodegree_Notes)
- [看Term1(本文)](https://github.com/zhsam/Data_Analyst_Nanodegree_Notes/blob/master/Term1-%20%E6%95%B0%E6%8D%AE%E5%88%86%E6%9E%90(%E5%85%A5%E9%97%A8).md)
- [看Term2](https://github.com/zhsam/Data_Analyst_Nanodegree_Notes/blob/master/Term2-%20%E6%95%B0%E6%8D%AE%E5%88%86%E6%9E%90(%E8%BF%9B%E9%98%B6).md)
- [看面试经验](https://github.com/zhsam/Data_Analyst_Nanodegree_Notes/blob/master/%E9%9D%A2%E8%AF%95%E7%BB%8F%E9%AA%8C-%E5%BF%AB%E6%89%8B-%E6%95%B0%E6%8D%AE%E5%88%86%E6%9E%90%E5%B8%88.md)

## 课程目录
- 1.欢迎来到第一学期 (Welcome to Term1!)
  - 欢迎来到纳米学位 (Welcome to Nanodegree Program)
  - 数据分析师的一天 (The Life of a Data Analyst)
  - 项目准备：SQL与 移动平均(Project Prep. SQL and Moving Average)
  - [项目]探索气候趋势 [Project] Explore Weather Trends
- 2.Python入门 (Introduction to Python)
  - 为什么要Python？ (Why Python Programming)
  - 数据类型与运算符 (Data Types and Opertors)
  - 控制流 (Control Flow)
  - 函数 (Functions)
  - 脚本撰写 (Scripting)
  - Numpy (Python包)
  - Pandas (Python包)
  - [项目]美国共享单车数据分析 [Project] Explore US Bikeshare Data
- 3.数据分析入门 (Introduction to Data Analysis)
  - Anaconda
  - Jupyter Notebooks
  - 数据分析流程 (The Data Anlysis Process)
  - 数据分析流程-案例1 (Data Analysis Process - Case Study 1)
  - 数据分析流程-案例2 (Data Analysis Process - Case Study 2)
  - 数据分析工作流 (Programming Workflow for Data Analysis)
  - SQL基础 (Basic SQL)
  - SQL Joins
  - SQL Aggregations
  - SQL Subqueries & Temporary Tables
  - SQL Data Cleaning
  - [Advanced] SQL Window Functions
  - [Advanced] SQL Advanced JOINs & Performance Tunning
  - [Project] Investigate a Dataset
- 4.实战统计学 (Practical Statistics)
  - 描述统计-1 (Descriptive Statistics - Part1)
  - 描述统计-2 (Descriptive Statistics - Part2)
  - 录取问题-案例分析 (Admissions Case Study)
  - 概率 (Probability)
  - 白努力定理 (Binomial Distribution)
  - 条件概率 (Conditional Probability)
  - 贝叶斯定理 (Bayes Rule)
  - Python概率练习 (Python Probability Practice)
  - 正态分布定理 (Normal Distribution Theory)
  - 抽样与中央极限定理 (Sampling distributions and the Central Limit Theorem)
  - 信赖区间 (Confidence Intervals)
  - 假设检定 (Hypothesis Testing)
  - 案例分析: AB测试 (Case Study: A/B tests)
  - 回归 (Regression)
  - 多元线性回归 (Multiple Linear Regression)
  - 逻辑回归 (Logistic Regression)
  - [项目]分析AB测试结果 ([Project] Analyze A/B Test Results)
- 5.恭喜与下一步 (Congratulations and Next Steps)

<hr></hr>

## 1.欢迎来到第一学期 (Welcome to Term1!)

### 1-3 项目准备：SQL与 移动平均(Project Prep. SQL and Moving Average)
**SQL 基本介绍**
- SELECT & FROM：从某个表里，选取XXX。
- LIMIT：限制返回的行数
- ORDER BY：排序方式
- WHERE：特定条件
- LIKE：模糊查询
- IN：
`select * from user_info where user_id in (1001, 1002)`
- NOT：不等于
- AND, BETWEEN：
  - AND： 同时符合一些条件
  - BETWEEN： 在两个条件之间
- OR：只要某个条件成立就成立

**移动平均 Moving Average, MA**
- 指的是一次计算一段区间内的平均值，而非单天的数值。 <br>
- 移动平均可抚平短期波动，反映出长期趋势或周期。 <br>
- 例：想看01/01 - 01/31数据的7日移动平均情况， <br>
01/07 = 01/01 - 01/07的数据均值 <br>
01/08 = 01/02 - 01/08的数据均值 <br>
以此类推

## 2.Python入门 (Introduction to Python)
## 3.数据分析入门 (Introduction to Data Analysis)

### 3-8 SQL Joins
- JOIN 顾名思义为将表进行连接
```
SELECT o.*, a.*
FROM demo.orders o
JOIN demo.accounts a
ON orders.account_id = accounts.id
```

- JOIN的分类
  - **LEFT JOIN**
  - RIGHT JOIN
  - OUTER JOIN
  - FULL OUTER JOIN

### 3-9 SQL Aggregations
- count( ): 计数  不考虑 null
- sum ( ): 求和
- min( ): 最小值
- max( ): 最大值
- avg( ): 均值

- NULL: 空值，无法使用 '=', 只能用 IS NULL ／ IS NOT NULL

- GROUP BY — 有统计函数，需要有 Group by

- DISTINCT

- HAVING — 类似 WHERE

- DATE

- CASE — if then statements in SQL
  - 范例1
```
CASE WHEN  platform_id = 1 OR(AND) platform_id = 0 THEN 0 ELSE  1  END as is_facebook
```
  - 范例2
```
SELECT a.name, SUM(total_amt_usd) total_spent,
     CASE WHEN SUM(total_amt_usd) > 200000 THEN 'top'
     WHEN  SUM(total_amt_usd) > 100000 THEN 'middle'
     ELSE 'low' END AS customer_level
FROM orders o
JOIN accounts a
ON o.account_id = a.id
WHERE occurred_at > '2015-12-31'
GROUP BY 1
ORDER BY 2 DESC;
```

### 3-10 SQL Subqueries & Temporary Tables
- Subqueries
先运行内层查询，在运行外层查询。
子查询可以放在 FROM之后、或者WHERE之中。

  - 范例1 - 最常见的子查询
```
SELECT *
FROM (SELECT DATE_TRUNC('day',occurred_at) AS day,
           channel, COUNT(*) as events
     FROM web_events
     GROUP BY 1,2
     ORDER BY 3 DESC) sub;
```
  - 范例2 - 子查询在 WHERE
```
SELECT AVG(standard_qty) avg_std, AVG(gloss_qty) avg_gls, AVG(poster_qty) avg_pst
FROM orders
WHERE DATE_TRUNC('month', occurred_at) =
     (SELECT DATE_TRUNC('month', MIN(occurred_at)) FROM orders);
```
  - 范例3 - 多层子查询
```
SELECT t3.id, t3.name, t3.channel, t3.ct
FROM (SELECT a.id, a.name, we.channel,  COUNT(*) ct
      FROM accounts a
      JOIN web_events we
      ON a.id = we.account_id
      GROUP BY a.id, a.name, we.channel) t3
JOIN (SELECT t1.id, t1.name, MAX(ct) max_chan
      FROM (SELECT a.id, a.name, we.channel,  COUNT(*) ct
            FROM accounts a
            JOIN web_events we
            ON a.id = we.account_id
            GROUP BY a.id, a.name, we.channel) t1
      GROUP BY t1.id, t1.name) t2
ON t2.id = t3.id AND t2.max_chan = t3.ct
ORDER BY t3.id, t3.ct;
```
  - 范例4 - 多重JOIN
```
SELECT t3.rep_name, t3.region_name, t3.total_amt
FROM(SELECT region_name, MAX(total_amt) total_amt
     FROM(SELECT s.name rep_name, r.name region_name, SUM(o.total_amt_usd) total_amt
             FROM sales_reps s
             JOIN accounts a
             ON a.sales_rep_id = s.id
             JOIN orders o
             ON o.account_id = a.id
             JOIN region r
             ON r.id = s.region_id
             GROUP BY 1, 2) t1
     GROUP BY 1) t2
JOIN (SELECT s.name rep_name, r.name region_name, SUM(o.total_amt_usd) total_amt
     FROM sales_reps s
     JOIN accounts a
     ON a.sales_rep_id = s.id
     JOIN orders o
     ON o.account_id = a.id
     JOIN region r
     ON r.id = s.region_id
     GROUP BY 1,2
     ORDER BY 3 DESC) t3
ON t3.region_name = t2.region_name AND t3.total_amt = t2.total_amt;
```
- WITH
WITH 又被称之为公用表表达式 (Common Table Expression, CTE)

  - 范例1 - 简单WITH
```
WITH events AS (SELECT DATE_TRUNC('day', occurred_at) AS day,
                channel,
                COUNT(*) AS event_count
                FROM demo.web_events_full
                ORDER BY 1, 2)

SELECT channel,
       AVG(event_count) AS avg_event_count
FROM events
ORDER BY 1
ORDER BY 2 DESC
```
  - 范例2 - 多项 WITH
```
WITH t1 AS (
   SELECT AVG(o.total_amt_usd) avg_all
   FROM orders o
   JOIN accounts a
   ON a.id = o.account_id),
t2 AS (
   SELECT o.account_id, AVG(o.total_amt_usd) avg_amt
   FROM orders o
   GROUP BY 1
   HAVING AVG(o.total_amt_usd) > (SELECT * FROM t1))
SELECT AVG(avg_amt)
FROM t2;
```

### 3-11 SQL Data Cleaning
**截取数据**
- LEFT: 截取左边数来第几位
`LEFT(phone_number, 3)`
- RIGHT: 截取右边数来第几位
`RIGHT(phone_number, 8)`
- POSITION：回传该特定字符，从左侧起出现的位置
- STRPOS：字符串的位置函数
```
SELECT LEFT(name, STRPOS(name, ' ') -1 ) first_name,
       RIGHT(name, LENGTH(name) - STRPOS(name, ' ')) last_name
FROM sales_reps;
```
- LOWER：全部变成小写
- UPPER：全部变成大写

**串接数据**
- CONCAT：将字符串在一块
`CONCAT(first_name, ' ', last_name)`
- ||
`first_name || ' ' || last_name`

**进阶时间函数**
- CAST：把数据变成某种格式
两种cast的方法：
  - (1) AS
  ```
  SELECT (SUBSTR(date, 7, 4) || '-' || LEFT(date, 2) || '-' || SUBSTR(date, 4, 2) AS DATE) new_date
  FROM sf_crime_data;
  ```
  - (2) ::
```
SELECT (SUBSTR(date, 7, 4) || '-' || LEFT(date, 2) || '-' || SUBSTR(date, 4, 2))::DATE new_date
FROM sf_crime_data;
```
- COALESCE：处理空值
```
SELECT COALESCE(a.id, a.id) filled_id, a.name, a.website, a.lat, a.long, a.primary_poc, a.sales_rep_id, COALESCE(o.account_id, a.id) account_id, o.occurred_at, COALESCE(o.standard_qty, 0) standard_qty, COALESCE(o.gloss_qty,0) gloss_qty, COALESCE(o.poster_qty,0) poster_qty, COALESCE(o.total,0) total, COALESCE(o.standard_amt_usd,0) standard_amt_usd, COALESCE(o.gloss_amt_usd,0) gloss_amt_usd, COALESCE(o.poster_amt_usd,0) poster_amt_usd, COALESCE(o.total_amt_usd,0) total_amt_usd
FROM accounts a
LEFT JOIN orders o
ON a.id = o.account_id;
```

### 3-12 [Advanced] SQL Window Functions
**Window Function 1**

**Window Function 2**

**ROW_NUMBER**

**Rank**

**Aggregations in Window Function**

**Alias for Multiple Window Function**

 **Comparing a Row to Previous Row**

**Percentiles**

### 3-13 [Advanced] SQL Advanced JOINs & Performance Tunning
**FULL OUTER JOIN**

**Self JOINs**

**UNION**

**Performance Tuning**

## 4.实战统计学 (Practical Statistics)
### 4-1 描述统计-1 (Descriptive Statistics - Part1)

### 4-2 描述统计-2 (Descriptive Statistics - Part2)

### 4-3 录取问题-案例分析 (Admissions Case Study)

### 4-4 概率 (Probability)

### 4-5 白努力定理 (Binomial Distribution)

### 4-6 条件概率 (Conditional Probability)

### 4-7 贝叶斯定理 (Bayes Rule)

### 4-8 Python概率练习 (Python Probability Practice)

### 4-9 正态分布定理 (Normal Distribution Theory)

### 4-10 抽样与中央极限定理 (Sampling distributions and the Central Limit Theorem)

### 4-11 信赖区间 (Confidence Intervals)

### 4-12 假设检定 (Hypothesis Testing)

### 4-13 案例分析: AB测试 (Case Study: A/B tests)

### 4-14 回归 (Regression)

### 4-15 多元线性回归 (Multiple Linear Regression)

### 4-16 逻辑回归 (Logistic Regression)

### [项目]分析AB测试结果 ([Project] Analyze A/B Test Results)
