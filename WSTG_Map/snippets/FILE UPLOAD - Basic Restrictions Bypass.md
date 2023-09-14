#file_upload 

# Client side filter
- Proxy and modify request after successfully passed client side restriction.
- Proxy and drop JavaScript related to file upload when loading page.
- Disable JavaScript in the browser.


# Extension filter
If only .php is filtered, try other extensions: 
```
.phtml
.php3
.php4
.php5
.php7
.phps
.php-s
.pht
.phar
```


# MIME Type restriction
MIME (Multipurpose Internet Mail Extension) Types are used as an identifier for files.
Originally used in email for attachments, it is now also used when files are being transferred over HTTP(S). 

The MIME Type for a file upload is attached in the Content-Type header as follows: 
```
Content-Type: <type>/<subtype>
``` 

MIME Types list: https://developer.mozilla.org/fr/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types