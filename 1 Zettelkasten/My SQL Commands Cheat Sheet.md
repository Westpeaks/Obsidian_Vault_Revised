# Database Operations

### Create Database

```sql
CREATE DATABASE database_name;
CREATE DATABASE IF NOT EXISTS database_name;
```

### Show Databases

```sql
SHOW DATABASES;
```

### Use Database

```sql
USE database_name;
```

### Drop Database

```sql
DROP DATABASE database_name;
DROP DATABASE IF EXISTS database_name;
```

## Table Operations

### Create Table

```sql
CREATE TABLE table_name (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    age INT DEFAULT 0,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### Show Tables

```sql
SHOW TABLES;
DESCRIBE table_name;  -- Show table structure
SHOW CREATE TABLE table_name;  -- Show CREATE statement
```

### Alter Table

```sql
-- Add column
ALTER TABLE table_name ADD column_name datatype;

-- Drop column
ALTER TABLE table_name DROP COLUMN column_name;

-- Modify column
ALTER TABLE table_name MODIFY COLUMN column_name new_datatype;

-- Rename column
ALTER TABLE table_name CHANGE old_name new_name datatype;

-- Rename table
ALTER TABLE old_table_name RENAME TO new_table_name;
```

### Drop Table

```sql
DROP TABLE table_name;
DROP TABLE IF EXISTS table_name;
```

### Truncate Table

```sql
TRUNCATE TABLE table_name;  -- Delete all rows, reset AUTO_INCREMENT
```

## Data Manipulation (CRUD)

### INSERT - Create

```sql
-- Single row
INSERT INTO table_name (col1, col2) VALUES (val1, val2);

-- Multiple rows
INSERT INTO table_name (col1, col2) 
VALUES (val1, val2), (val3, val4), (val5, val6);

-- Insert from another table
INSERT INTO table_name (col1, col2)
SELECT col1, col2 FROM other_table WHERE condition;
```

### SELECT - Read

```sql
-- Basic select
SELECT * FROM table_name;
SELECT col1, col2 FROM table_name;

-- With WHERE clause
SELECT * FROM table_name WHERE condition;

-- DISTINCT values
SELECT DISTINCT column_name FROM table_name;

-- LIMIT results
SELECT * FROM table_name LIMIT 10;
SELECT * FROM table_name LIMIT 10 OFFSET 20;
```

### UPDATE - Update

```sql
UPDATE table_name 
SET col1 = val1, col2 = val2 
WHERE condition;
```

### DELETE - Delete

```sql
DELETE FROM table_name WHERE condition;
DELETE FROM table_name;  -- Delete all rows (use with caution!)
```

## Filtering and Sorting

### WHERE Clause Operators

```sql
-- Comparison
WHERE age = 25
WHERE age != 25
WHERE age > 25
WHERE age >= 25
WHERE age < 25
WHERE age <= 25

-- Logical operators
WHERE age > 18 AND city = 'NYC'
WHERE city = 'NYC' OR city = 'LA'
WHERE NOT age > 18

-- BETWEEN
WHERE age BETWEEN 18 AND 65

-- IN
WHERE city IN ('NYC', 'LA', 'Chicago')

-- LIKE (pattern matching)
WHERE name LIKE 'J%'        -- Starts with J
WHERE name LIKE '%son'      -- Ends with son
WHERE name LIKE '%an%'      -- Contains an
WHERE name LIKE '_ohn'      -- Second char is o, followed by hn

-- IS NULL / IS NOT NULL
WHERE email IS NULL
WHERE email IS NOT NULL
```

### ORDER BY

```sql
SELECT * FROM table_name ORDER BY column_name ASC;
SELECT * FROM table_name ORDER BY column_name DESC;
SELECT * FROM table_name ORDER BY col1 ASC, col2 DESC;
```

## Aggregate Functions

```sql
SELECT COUNT(*) FROM table_name;
SELECT COUNT(DISTINCT column_name) FROM table_name;
SELECT SUM(column_name) FROM table_name;
SELECT AVG(column_name) FROM table_name;
SELECT MIN(column_name) FROM table_name;
SELECT MAX(column_name) FROM table_name;
```

### GROUP BY

```sql
SELECT city, COUNT(*) 
FROM users 
GROUP BY city;

-- With HAVING (filter groups)
SELECT city, COUNT(*) as count
FROM users 
GROUP BY city 
HAVING count > 10;
```

## Joins

### INNER JOIN

```sql
SELECT * FROM table1
INNER JOIN table2 ON table1.id = table2.table1_id;
```

### LEFT JOIN

```sql
SELECT * FROM table1
LEFT JOIN table2 ON table1.id = table2.table1_id;
```

### RIGHT JOIN

```sql
SELECT * FROM table1
RIGHT JOIN table2 ON table1.id = table2.table1_id;
```

### CROSS JOIN

```sql
SELECT * FROM table1
CROSS JOIN table2;
```

### Self Join

```sql
SELECT a.name, b.name 
FROM employees a, employees b 
WHERE a.manager_id = b.id;
```

## Indexes

```sql
-- Create index
CREATE INDEX index_name ON table_name (column_name);

-- Create unique index
CREATE UNIQUE INDEX index_name ON table_name (column_name);

-- Create composite index
CREATE INDEX index_name ON table_name (col1, col2);

-- Show indexes
SHOW INDEX FROM table_name;

-- Drop index
DROP INDEX index_name ON table_name;
```

## Constraints

```sql
-- Primary Key
CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT
);

-- Foreign Key
CREATE TABLE orders (
    id INT PRIMARY KEY,
    user_id INT,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

-- Unique
CREATE TABLE users (
    email VARCHAR(100) UNIQUE
);

-- Not Null
CREATE TABLE users (
    name VARCHAR(100) NOT NULL
);

-- Check
CREATE TABLE users (
    age INT CHECK (age >= 18)
);

-- Default
CREATE TABLE users (
    status VARCHAR(20) DEFAULT 'active'
);
```

## Subqueries

```sql
-- Subquery in WHERE
SELECT * FROM users 
WHERE id IN (SELECT user_id FROM orders WHERE total > 100);

-- Subquery in FROM
SELECT avg_age FROM (
    SELECT AVG(age) as avg_age FROM users GROUP BY city
) as subquery;

-- Correlated subquery
SELECT * FROM users u1
WHERE salary > (SELECT AVG(salary) FROM users u2 WHERE u2.dept = u1.dept);
```

## Common String Functions

```sql
CONCAT(str1, str2)           -- Concatenate strings
UPPER(str)                   -- Convert to uppercase
LOWER(str)                   -- Convert to lowercase
LENGTH(str)                  -- String length
SUBSTRING(str, start, len)   -- Extract substring
TRIM(str)                    -- Remove leading/trailing spaces
REPLACE(str, old, new)       -- Replace substring
```

## Common Date Functions

```sql
NOW()                        -- Current date and time
CURDATE()                    -- Current date
CURTIME()                    -- Current time
DATE(datetime)               -- Extract date part
YEAR(date)                   -- Extract year
MONTH(date)                  -- Extract month
DAY(date)                    -- Extract day
DATE_ADD(date, INTERVAL 1 DAY)
DATE_SUB(date, INTERVAL 1 MONTH)
DATEDIFF(date1, date2)       -- Difference in days
```

## Transaction Control

```sql
START TRANSACTION;
-- SQL statements here
COMMIT;

-- Or rollback if needed
ROLLBACK;
```

## User Management

```sql
-- Create user
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';

-- Grant privileges
GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost';
GRANT SELECT, INSERT ON database_name.table_name TO 'username'@'localhost';

-- Show grants
SHOW GRANTS FOR 'username'@'localhost';

-- Revoke privileges
REVOKE ALL PRIVILEGES ON database_name.* FROM 'username'@'localhost';

-- Drop user
DROP USER 'username'@'localhost';

-- Reload privileges
FLUSH PRIVILEGES;
```

## Utility Commands

```sql
-- Show current database
SELECT DATABASE();

-- Show MySQL version
SELECT VERSION();

-- Show current user
SELECT USER();

-- Show table size
SELECT 
    table_name,
    ROUND(((data_length + index_length) / 1024 / 1024), 2) AS "Size (MB)"
FROM information_schema.TABLES
WHERE table_schema = 'database_name';

-- Kill a query
SHOW PROCESSLIST;
KILL process_id;
```


## Links:

2025111527