2024-05-15 10:31

Tags: [[Troubleshooting]] 

# Atlassian Interview Questions SQL Queries

**SELECT**: The `SELECT` statement is used to retrieve data from one or more tables in a database. It allows you to specify the columns you want to retrieve and the conditions for filtering rows.

Example:

sql

```
SELECT column1, column2 FROM table_name WHERE condition;
```
    
- **FROM**: The `FROM` clause specifies the table or tables from which to retrieve data. It is used in conjunction with the `SELECT` statement.
    
    Example:
    
    sql
    
```
SELECT column1, column2 FROM table_name;
```
    
- **WHERE**: The `WHERE` clause is used to filter rows based on specified conditions. It allows you to retrieve only the rows that meet the specified criteria.
    
    Example:
    
    sql
    
```
SELECT column1, column2 FROM table_name WHERE condition;
```
    
- **INSERT INTO**: The `INSERT INTO` statement is used to add new rows of data into a table.
    
    Example:
    
    sql
    
```
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```
    
- **UPDATE**: The `UPDATE` statement is used to modify existing data in a table.
    
    Example:
    
    sql
    
```
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
    
- **DELETE**: The `DELETE` statement is used to remove one or more rows from a table.
    
    Example:
    
    sql
    
```
DELETE FROM table_name WHERE condition;
```
    
- **GROUP BY**: The `GROUP BY` clause is used to group rows that have the same values into summary rows.
    
    Example:
    
    sql
    
```
SELECT column1, COUNT(*) FROM table_name GROUP BY column1;
```
    
- **HAVING**: The `HAVING` clause is used in combination with the `GROUP BY` clause to filter groups of rows.
    
    Example:
    
    sql
    
```
SELECT column1, COUNT(*) FROM table_name GROUP BY column1 HAVING COUNT(*) > 1;
```
    
- **ORDER BY**: The `ORDER BY` clause is used to sort the result set in ascending or descending order based on one or more columns.
    
    Example:
    
    sql
    

```
SELECT column1, column2 FROM table_name ORDER BY column1 ASC, column2 DESC;
```
    

### ==Also check your notes to discuss projects and furhter commands==

2024-05-15 10:31

Tags:

# Atlassian Interview Questions SQL Queries




## References


