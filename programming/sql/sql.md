````markdown
# SQL Instructions

## 1. **SELECT**
The `SELECT` statement is used to query the database and retrieve data.

```sql
SELECT column1, column2 FROM table_name;
````

* To select all columns:

```sql
SELECT * FROM table_name;
```

## 2. **INSERT**

The `INSERT` statement is used to insert new records into a table.

```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```

* Insert multiple rows:

```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2), (value3, value4);
```

## 3. **UPDATE**

The `UPDATE` statement is used to modify existing records in a table.

```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```

## 4. **DELETE**

The `DELETE` statement is used to delete records from a table.

```sql
DELETE FROM table_name WHERE condition;
```

* To delete all records:

```sql
DELETE FROM table_name;
```

## 5. **CREATE TABLE**

The `CREATE TABLE` statement is used to create a new table in the database.

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype
);
```

## 6. **ALTER TABLE**

The `ALTER TABLE` statement is used to modify an existing table structure.

* Add a new column:

```sql
ALTER TABLE table_name ADD column_name datatype;
```

* Drop a column:

```sql
ALTER TABLE table_name DROP COLUMN column_name;
```

## 7. **DROP TABLE**

The `DROP TABLE` statement is used to delete a table and all its data from the database.

```sql
DROP TABLE table_name;
```

## 8. **CREATE INDEX**

The `CREATE INDEX` statement is used to create an index (a faster lookup method) for a table.

```sql
CREATE INDEX index_name ON table_name (column_name);
```

## 9. **DROP INDEX**

The `DROP INDEX` statement is used to delete an index.

```sql
DROP INDEX index_name;
```

## 10. **JOIN**

The `JOIN` clause is used to combine rows from two or more tables based on a related column.

* **INNER JOIN**: Returns rows when there is a match in both tables.

```sql
SELECT columns FROM table1
INNER JOIN table2 ON table1.column = table2.column;
```

* **LEFT JOIN**: Returns all rows from the left table, even if there’s no match in the right table.

```sql
SELECT columns FROM table1
LEFT JOIN table2 ON table1.column = table2.column;
```

## 11. **GROUP BY**

The `GROUP BY` statement is used to group rows that have the same values into summary rows.

```sql
SELECT column, COUNT(*) FROM table_name
GROUP BY column;
```

## 12. **HAVING**

The `HAVING` clause is used to filter records after a `GROUP BY` is applied.

```sql
SELECT column, COUNT(*) FROM table_name
GROUP BY column
HAVING COUNT(*) > 5;
```

## 13. **ORDER BY**

The `ORDER BY` statement is used to sort the result set in either ascending or descending order.

```sql
SELECT * FROM table_name
ORDER BY column_name ASC;  -- ascending
```

```sql
SELECT * FROM table_name
ORDER BY column_name DESC;  -- descending
```

## 14. **DISTINCT**

The `DISTINCT` keyword is used to return only distinct (different) values.

```sql
SELECT DISTINCT column_name FROM table_name;
```

## 15. **LIMIT**

The `LIMIT` clause is used to specify the number of records to return.

```sql
SELECT * FROM table_name LIMIT 5;
```

## 16. **EXISTS**

The `EXISTS` operator is used to test for the existence of rows returned by a subquery.

```sql
SELECT column_name FROM table_name
WHERE EXISTS (SELECT 1 FROM other_table WHERE condition);
```

## 17. **IN**

The `IN` operator allows you to specify multiple values in a `WHERE` clause.

```sql
SELECT * FROM table_name
WHERE column_name IN (value1, value2, value3);
```

## 18. **BETWEEN**

The `BETWEEN` operator is used to filter the result set within a certain range.

```sql
SELECT * FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

## 19. **CASE**

The `CASE` statement is used to create conditions in SQL queries (like an IF-ELSE statement).

```sql
SELECT column1,
    CASE 
        WHEN column2 > 50 THEN 'High'
        WHEN column2 <= 50 THEN 'Low'
        ELSE 'Unknown'
    END AS category
FROM table_name;
```

## 20. **TRANSACTIONS**

A transaction is a way to execute multiple SQL queries as a single unit. Transactions ensure that all queries are executed successfully before committing to the database.

```sql
BEGIN TRANSACTION;

-- SQL statements here

COMMIT;  -- or ROLLBACK if there's an error
```

---

This is a basic overview of SQL instructions. Each command has various variations and nuances depending on the database system (e.g., MySQL, PostgreSQL, SQL Server, etc.).
