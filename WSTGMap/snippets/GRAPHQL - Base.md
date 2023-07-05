#graphql
## Query Schema

```bash
curl -s -X POST \ 
-H "Content-Type: application/json" \
-d "{ \"query\": \"{ __schema {types {name, fields {name}} } }\" }" \
http://[TAGET]/ | jq
```

## Query Value
```bash
curl -s -X POST \
-H "Content-Type: application/json" \
-d "{\"query\":\"{ myEndpoint(very_long_id:objectID) { value } }\"}"  \
http://[TAGET]/  | jq
```