#sqli #mysql

## DB Version

```sql
SELECT @@version
```


## List Tables

Interesting column: `TABLE_NAME`.
```sql
SELECT * FROM information_schema.tables
```


## List Columns
Interesting column: `COLUMN_NAME`.

```sql
SELECT * FROM information_schema.columns WHERE table_name = 'MY_TABLE_NAME'
```