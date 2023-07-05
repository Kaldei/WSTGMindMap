#xmli #xml



## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
 <userInfo>
  <lastName>Name</lastName>
 </userInfo>
```

## Injection
```xml
<?xml version="1.0"?>
<!DOCTYPE replace [<!ENTITY myVar "[MY_INJECTION_PAYLOAD]">]>
 <userInfo>
  <lastName>&myVar;</lastName>
 </userInfo>
```