#cors 

CORS is an HTTP-header based mechanism that allows resources (e.g., fonts, images, scripts) on a web page to be requested from another domain outside the domain from which the resource originated.

## Response Header Access-Control-Allow-Origin (ACAO)

Possibles values:
- Website: `my.website.com`
- Wildcard: `*`
- Null: `null`

## Response Header Access-Control-Allow-Credentials (ACAC)
Possible values:
- true
- false?

## Note

TOCHECK NOT SURE: Wilcard + Alllow-Credentials is not allowed :
```
Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true
```


