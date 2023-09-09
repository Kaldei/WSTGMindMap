#cookie 

## Ressource
https://portswigger.net/web-security/csrf/bypassing-samesite-restrictions

## SameSite=None
When setting a cookie with SameSite=None, the website must also include the Secure attribute, which ensures that the cookie is only sent in encrypted messages over HTTPS. Otherwise, browsers will reject the cookie and it won't be set. 

## SameSite=lax (Default with chrome)
 Browsers will send the cookie in cross-site requests, but only if both of the following conditions are met:
 - The request uses the GET method.
 - The request resulted from a top-level navigation by the user, such as clicking on a link.

## SameSite=Strict (Old default)
If the target site for the request does not match the current site, it will not include the cookie. 