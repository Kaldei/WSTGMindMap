#sqli #oracle

## DB Version

```sql
SELECT * FROM v$version
```


## List Tables

Interesting column: `TABLE_NAME`.
```sql
SELECT * FROM all_tables
```


## List Columns
Interesting column: `COLUMN_NAME`.

```sql
SELECT * FROM all_tab_columns WHERE table_name = 'MY_TABLE_NAME'
```