## 以下两张基于 id 列，分别使用 INNER JOIN、LEFT JOIN、 RIGHT JOIN 的结果是什么?
```
Table1

id name

1 table1_table2

2 table1

Table2

id name

1 table1_table2

3 table2
```

## 举例: INNER JOIN
```sql
SELECT Table1.id, Table1.name, Table2.id, Table2.name
FROM Table1
INNER JOIN Table2
ON Table1.id = Table2.id;

-- 结果：取 满足 Table1.id = Table2.id 条件的所有值；交集
```

## LEFT JOIN
```sql
SELECT Table1.id, Table1.name, Table2.id, Table2.name
FROM Table1
LEFT JOIN Table2
ON Table1.id = Table2.id;

-- 结果： Table1 存在，但Table2 不存在的值也显示，但Table2.id，Table2.name 列为NULL
```
## RIGHT JOIN
```sql
SELECT Table1.id, Table1.name, Table2.id, Table2.name
FROM Table1
RIGHT JOIN Table2
ON Table1.id = Table2.id;

-- 结果： Table2 存在，但Table1 不存在的值也显示，但Table1.id，Table1.name 列为NULL
```


![avatar](https://images2017.cnblogs.com/blog/1035967/201709/1035967-20170907174926054-907920122.jpg)

[参考文档-MySQL的JOIN（一）：用法](https://www.cnblogs.com/fudashi/p/7491039.html)