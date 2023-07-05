#sqli #sqlite

Schema Table name is `sqlite_schema` but those are also working: `sqlite_master`, `sqlite_temp_schema`, `sqlite_temp_master`.

## Display Commands Used to Create DB
```sql
SELECT sql FROM sqlite_master
```

## List Tables

```sql
SELECT tbl_name FROM sqlite_master
```

```sql
group_concat(table_name) FROM information_schema.tables WHERE table_schema = 'sqli_one'
```

## List Columns

```sql
group_concat(column_name) FROM information_schema.columns WHERE table_name = 'MY_TABLE_NAME'
```