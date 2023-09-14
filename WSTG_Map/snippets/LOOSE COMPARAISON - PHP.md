#loose_comparison #php

## Resources
https://book.hacktricks.xyz/network-services-pentesting/pentesting-web/php-tricks-esp

![[loose_comparison_php.png]]

## Interesting
- A string which doesn't start with a number and a number: True
- `0e12…` and `0e98…`: True because `e` is interpreted an exponent (`0e…` and `0` also True).
- `strcasecmp()` or `strcmp()` → Send empty array instead of string will be True.

