#click_jacking #headers #csp 

## Content-Security-Policy: frame-ancestor
`frame-ancestors` can be added to `Content-Security-Policy`. This directive is similar to the behavior of `X-Frame-Options`.

## Not vulnerable to Click Jacking
```http
Content-Security-Policy: frame-ancestors 'none';
```

```http
Content-Security-Policy: frame-ancestors 'self';
```

## Might be vulnerable depending on allowed websites
```http
Content-Security-Policy: frame-ancestor https://a.website.com
```