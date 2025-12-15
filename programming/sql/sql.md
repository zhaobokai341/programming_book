# **Ultimate SQL Cheat Sheet**

---

## **1. SELECT**

Retrieve data from one or more tables.

```sql
SELECT column1, column2 FROM table_name;
```

* Select all columns:

```sql
SELECT * FROM table_name;
```

* With `DISTINCT`:

```sql
SELECT DISTINCT column_name FROM table_name;
```

* With alias:

```sql
SELECT column1 AS c1, column2 AS c2 FROM table_name;
```

---

## **2. WHERE**

Filter rows based on conditions.

```sql
SELECT * FROM table_name
WHERE condition;
```

* Operators: `=, <>, !=, >, <, >=, <=`
* Logical: `AND, OR, NOT`
* Pattern: `LIKE 'pattern%'`
* Null check: `IS NULL`, `IS NOT NULL`
* Range: `BETWEEN value1 AND value2`
* Set: `IN (value1, value2, ...)`
* Existence: `EXISTS (subquery)`

---

## **3. INSERT**

Insert new rows.

```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```

* Insert multiple rows:

```sql
INSERT INTO table_name (column1, column2) VALUES 
(value1, value2), 
(value3, value4);
```

* Insert with SELECT:

```sql
INSERT INTO table_name (column1, column2)
SELECT column1, column2 FROM other_table;
```

---

## **4. UPDATE**

Modify existing rows.

```sql
UPDATE table_name
SET column1 = value1, column2 = value2
WHERE condition;
```

* Update all rows (no WHERE):

```sql
UPDATE table_name
SET column1 = value;
```

---

## **5. DELETE**

Remove rows.

```sql
DELETE FROM table_name
WHERE condition;
```

* Delete all rows:

```sql
DELETE FROM table_name;
```

---

## **6. CREATE TABLE**

Create a new table.

```sql
CREATE TABLE table_name (
    column1 datatype [constraints],
    column2 datatype [constraints],
    ...
);
```

* Common data types: `INT`, `BIGINT`, `DECIMAL`, `NUMERIC`, `FLOAT`, `CHAR(n)`, `VARCHAR(n)`, `TEXT`, `DATE`, `DATETIME`, `TIMESTAMP`, `BOOLEAN`

* Common constraints: `PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `NOT NULL`, `DEFAULT`, `CHECK`, `AUTO_INCREMENT` / `SERIAL`

---

## **7. ALTER TABLE**

Modify an existing table.

* Add column:

```sql
ALTER TABLE table_name ADD column_name datatype;
```

* Drop column:

```sql
ALTER TABLE table_name DROP COLUMN column_name;
```

* Modify column:

```sql
ALTER TABLE table_name MODIFY COLUMN column_name datatype;
```

* Add constraint:

```sql
ALTER TABLE table_name ADD CONSTRAINT constraint_name PRIMARY KEY (column_name);
```

---

## **8. DROP TABLE / DROP DATABASE**

Delete a table or database.

```sql
DROP TABLE table_name;
DROP DATABASE database_name;
```

---

## **9. INDEX**

Create an index to optimize queries.

```sql
CREATE INDEX index_name ON table_name (column_name);
```

* Unique index:

```sql
CREATE UNIQUE INDEX index_name ON table_name (column_name);
```

* Drop index:

```sql
DROP INDEX index_name;  -- MySQL
DROP INDEX index_name ON table_name;  -- SQL Server/PostgreSQL
```

---

## **10. JOIN**

Combine rows from multiple tables.

* **INNER JOIN**:

```sql
SELECT columns FROM table1
INNER JOIN table2 ON table1.column = table2.column;
```

* **LEFT (OUTER) JOIN**:

```sql
SELECT columns FROM table1
LEFT JOIN table2 ON table1.column = table2.column;
```

* **RIGHT (OUTER) JOIN**:

```sql
SELECT columns FROM table1
RIGHT JOIN table2 ON table1.column = table2.column;
```

* **FULL (OUTER) JOIN**:

```sql
SELECT columns FROM table1
FULL OUTER JOIN table2 ON table1.column = table2.column;
```

* **CROSS JOIN**:

```sql
SELECT * FROM table1 CROSS JOIN table2;
```

---

## **11. GROUP BY & HAVING**

Group rows and filter grouped data.

```sql
SELECT column, COUNT(*) 
FROM table_name
GROUP BY column
HAVING COUNT(*) > 5;
```

---

## **12. ORDER BY**

Sort result sets.

```sql
SELECT * FROM table_name
ORDER BY column_name ASC;  -- ascending
ORDER BY column_name DESC; -- descending
```

---

## **13. LIMIT / OFFSET**

Limit results.

```sql
SELECT * FROM table_name
LIMIT 5;  -- first 5 rows
```

```sql
SELECT * FROM table_name
LIMIT 5 OFFSET 10;  -- rows 11-15
```

---

## **14. CASE**

Conditional logic.

```sql
SELECT column1,
       CASE
           WHEN column2 > 50 THEN 'High'
           WHEN column2 <= 50 THEN 'Low'
           ELSE 'Unknown'
       END AS category
FROM table_name;
```

---

## **15. TRANSACTIONS**

Ensure multiple statements execute as a single unit.

```sql
BEGIN TRANSACTION;

-- SQL statements here

COMMIT;   -- save changes
ROLLBACK; -- undo changes
```

---

## **16. AGGREGATE FUNCTIONS**

| Function      | Description    |
| ------------- | -------------- |
| `COUNT(*)`    | Number of rows |
| `SUM(column)` | Sum of values  |
| `AVG(column)` | Average value  |
| `MIN(column)` | Minimum value  |
| `MAX(column)` | Maximum value  |

---

## **17. STRING FUNCTIONS**

| Function                     | Description         |
| ---------------------------- | ------------------- |
| `CONCAT(str1, str2, ...)`    | Concatenate strings |
| `LENGTH(str)`                | String length       |
| `SUBSTRING(str, start, len)` | Extract substring   |
| `UPPER(str)` / `LOWER(str)`  | Change case         |
| `TRIM(str)`                  | Remove spaces       |
| `REPLACE(str, old, new)`     | Replace substring   |

---

## **18. DATE & TIME FUNCTIONS**

| Function                                         | Description                 |
| ------------------------------------------------ | --------------------------- |
| `NOW()` / `CURRENT_TIMESTAMP`                    | Current date & time         |
| `CURDATE()`                                      | Current date                |
| `CURTIME()`                                      | Current time                |
| `DATE(column)`                                   | Extract date                |
| `YEAR(column)` / `MONTH(column)` / `DAY(column)` | Extract parts of date       |
| `DATEDIFF(date1, date2)`                         | Difference in days          |
| `DATE_ADD(date, INTERVAL n unit)`                | Add interval to date        |
| `DATE_SUB(date, INTERVAL n unit)`                | Subtract interval from date |

---

## **19. CONSTRAINTS**

| Constraint                  | Description              |
| --------------------------- | ------------------------ |
| `PRIMARY KEY`               | Unique identifier        |
| `FOREIGN KEY`               | References another table |
| `UNIQUE`                    | Unique values            |
| `NOT NULL`                  | Column must have value   |
| `CHECK`                     | Column value check       |
| `DEFAULT`                   | Default value            |
| `AUTO_INCREMENT` / `SERIAL` | Auto increment numbers   |

---

## **20. SUBQUERIES**

Nested queries for advanced filtering.

```sql
SELECT column FROM table1
WHERE column IN (SELECT column FROM table2 WHERE condition);
```

* Exists:

```sql
SELECT column FROM table1
WHERE EXISTS (SELECT 1 FROM table2 WHERE table1.id = table2.id);
```

---

## **21. SET OPERATORS**

| Operator           | Description                       |
| ------------------ | --------------------------------- |
| `UNION`            | Combine results (distinct)        |
| `UNION ALL`        | Combine results (all rows)        |
| `INTERSECT`        | Rows common to both queries       |
| `EXCEPT` / `MINUS` | Rows in first query not in second |

---

## **22. VIEWS**

Create a virtual table.

```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name
WHERE condition;
```

* Update or drop view:

```sql
ALTER VIEW view_name AS
SELECT ...;

DROP VIEW view_name;
```

---

## **23. STORED PROCEDURES & FUNCTIONS**

* **Stored Procedure**:

```sql
CREATE PROCEDURE procedure_name(parameters)
BEGIN
    -- SQL statements
END;
```

* **Function**:

```sql
CREATE FUNCTION function_name(parameters)
RETURNS datatype
BEGIN
    -- SQL statements
    RETURN value;
END;
```

---

## **24. TRIGGERS**

Automatically execute on events.

```sql
CREATE TRIGGER trigger_name
BEFORE INSERT ON table_name
FOR EACH ROW
BEGIN
    -- SQL statements
END;
```

---

## **25. TRANSACTION ISOLATION LEVELS**

| Level              | Description                                 |
| ------------------ | ------------------------------------------- |
| `READ UNCOMMITTED` | Can read uncommitted changes                |
| `READ COMMITTED`   | Only read committed changes                 |
| `REPEATABLE READ`  | Same select yields same rows in transaction |
| `SERIALIZABLE`     | Highest isolation, prevent phantom reads    |

---

This cheat sheet now includes **all core SQL commands, advanced features, constraints, aggregate functions, string/date functions, transactions, joins, subqueries, views, procedures, triggers, and set operators**, covering **MySQL, PostgreSQL, SQL Server, and standard SQL syntax**.
