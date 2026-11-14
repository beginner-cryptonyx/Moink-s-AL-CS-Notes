---
subject:
  - cs
---

# DDL and DML
DDL used to work on [[Database (CS)|database]] structure
DML used to work on data stored in database
## DDL:
- **Data Definition Language**
1. Used to **create**, **modify** and **remove** data structures from a [[Database Types|Relational Database]]
2. Must end with **Semicolon**

## DML:
- **Data Manipulation Language**
1. used to **Add**, **Modify**, **Delete** and **Retrieve**, data stored in [[Database Types|Relational Database]]

# Common Operations
1. [[Creating a table with SQL]]
2. [[Adding a foreign key]]
3. [[Inserting Value into a table with SQL]]
4. [[Deleting Row in SQL]]
5. [[Dropping Table in SQL]]

# Commands and Syntax

## DLL Commands:

#### CREATE DATABASE:
The `CREATE DATABASE` statement is used to create a new database.
```SQL
CREATE DATABASE database_name;
```

#### CREATE TABLE:
The `CREATE TABLE` statement is used to create a new table within a database.
```SQL
CREATE TABLE table_name (
	column1 datatype constraint,
	column2 datatype constraint,
	...
);
```

#### ALTER TABLE

## DML Commands

### Query Commands
#### SELECT - FROM:
```SQL
--syntax
SELECT column1, column2 FROM table_name 
SELECT DISTINCT column1, column2, FROM table -- unique values only

--example
SELECT DISTINCT Country FROM Customers;
```

#### WHERE
The `WHERE` clause is used to filter records.
It is used to extract only those records that fulfill a specified condition.
```sql
SELECT _column1_, _column2, ...
FROM table_name
WHERE condition
```

#### ORDER BY
The `ORDER BY` clause is used to sort the result set in ascending or descending order. The default is ascending.

```SQL
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC], column2 [ASC|DESC];
```

#### GROUP BY:
The `GROUP BY` clause groups rows with the same values into summary rows, often used with aggregate functions like `COUNT`, `SUM`, `AVG`, etc.

```SQL
SELECT column1, aggregate_function(column2)
FROM table_name
GROUP BY column1;
```

#### INNER JOIN:
The `INNER JOIN` keyword selects records with matching values in both tables.
```SQL
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

#### SUM:
The `SUM` function returns the total sum of a numeric column.
```SQL
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```

#### COUNT:
The `COUNT` function returns the number of rows that match a specified condition.
```SQL
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

#### AVG:
The `AVG` function returns the average value of a numeric column.
```sql
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

### Maintenance Commands:

#### INSERT INTO:
The `INSERT INTO` clause is used to insert new records into a table.

```SQL
-- Insert into all columns
INSERT INTO table_name
VALUES (value1, value2, ...);

-- Insert into specific columns
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

#### DELETE FROM:

The `DELETE FROM` clause is used to delete records from a table.
```sql
DELETE FROM table_name
WHERE condition;
```
> **Note**: If the `WHERE` clause is omitted, **all records** in the table will be deleted.

#### Update:

The `UPDATE` clause is used to modify existing records in a table.
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```