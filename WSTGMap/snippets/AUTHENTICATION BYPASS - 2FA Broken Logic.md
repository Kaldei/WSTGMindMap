#authentication_bypass #mfa

## A cookie is assigned when successfully log in and then 2FA code is asked:
https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-broken-logic
1. Log in with valid user
2. Change the value of the cookie to another valid username
3. Brute force 2FA code.