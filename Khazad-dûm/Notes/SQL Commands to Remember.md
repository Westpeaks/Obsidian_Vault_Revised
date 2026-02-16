2025-01-21 22:23

Tags: [[SQL]] [[Fundamentals]]

# SQL Commands to Remember

### Selecting Unique Values 

```
SELECT DISTINCT VALUE FROM TABLE;
```

### Selecting Even Rows

```
SELECT VALUE FROM TABLE WHERE VALUEID % 2 = 0;
```

### Count Two Rows and Return the Difference Between the Counts

#### In this example the count of rows are of the same row, the difference being between the over all count and the count of unique values. 

```
SELECT 
    (COUNT(VALUE) - COUNT(DISTINCT VALUE)) AS difference
FROM 
    TABLE;
```

## References



