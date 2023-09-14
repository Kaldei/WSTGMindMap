#sqli 

## DB Version
### Microsoft and MySQL
```sql
SELECT @@version
```

### Oracle
```sql
SELECT * FROM v$version
```
Interesting columns: `BANNER`, `VERSION`.

### PostgreSQL
```sql
SELECT version()
```


---
## List DB Tables
Interesting column: `TABLE_NAME`.

### Non-Oracle DB
```sql
SELECT * FROM information_schema.tables
```

### Oracle DB
```sql
SELECT * FROM all_tables
```


---
## List Table Columns
Interesting column: `COLUMN_NAME`.

### Non-Oracle DB
```sql
SELECT * FROM information_schema.columns WHERE table_name = 'MY_TABLE_NAME'
```

### Oracle DB
```sql
SELECT * FROM all_tab_columns WHERE table_name = 'MY_TABLE_NAME'
```