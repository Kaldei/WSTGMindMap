#csrf

Note: In the HTTP specification this header is misspelled (Referer instead of Referrer). Only the header is misspelled.

## Depend on Referer Header present
- Add `<meta name="referrer" content="never">`


## Depend on domain being present in the Referer Header
- Add header `Referrer-Policy: unsafe-url` (otherwise modern browses, strip the Referer header)
- Add `<script>history.pushState("", "", "/?[TARGET_DOMAIN]")</script>`

## Depend on domain being present at the beginning of the Referer header
- Use a subdomain corresponding