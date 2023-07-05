#click_jacking #headers

## X-Frame-Options
`X-Frame-Options` is used to control if the page can be included in an iframe.

## Not vulnerable to Click Jacking
```http
X-Frame-Options: deny
```

```http
X-Frame-Options: sameorigin
```

## Might be vulnerable depending on allowed websites
```http
X-Frame-Options: allow-from https://a.website.com
```