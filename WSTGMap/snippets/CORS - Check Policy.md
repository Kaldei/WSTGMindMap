#cors

## Test Reflected Origin
Add `Origin: http://random/`
Vulnerable if response is:
```
Access-Control-Allow-Origin: http://random/
Access-Control-Allow-Credentials: true
```

## Test Trust null Origin
Add `Origin: null`
Vulnerable if response is:
```
Access-Control-Allow-Origin: null
Access-Control-Allow-Credentials: true
```