#sqli

## Resources
- https://portswigger.net/web-security/sql-injection/cheat-sheet
- https://pentestmonkey.net/cheat-sheet/sql-injection/mysql-sql-injection-cheat-sheet
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection 


## SQL Comments
#### Oracle
```sql
--comment
```

#### Microsoft
```sql
--comment
/*comment*/
```

#### PostgreSQL
```sql
--comment
/*comment*/
```

#### MySQL
```sql
-- comment (There is a space after the double dash)
/*comment*/
# comment
```


## Detection
```sql
'
%27
"
%22
#
%23
;
%3B
)
```
