#cors 

## Basis
A Cross Domain request happens when a website hosted on one domain tries to access resources (e.g. fonts, images, scripts, ...) hosted on another domain.

CORS is a security mechanism that allows to authorize or not Cross Domain request. The list of authorized configs (Origin, Method, Headers, ...) is set on the server side, but is enforced on the browser side.


## Security Boundary
CORS is part of security measure to prevent against CSRF attacks: a resource should not allow to be accessed by any website (e.g. attacker website).

Why? Because browsers sends cookies with requests: if an attacker website tells your browser to access a resource where you were already logged in (and CORS allows it), the attacker will be able to retrieve your account's data or perform action on your behalf on this resource. 

Note:
- CORS is a browser feature (there is no `Origin` when using Curl or Postman because there is no user sessions to hijack).


## Types of Cross Domain Requests 
- Simple (1 step)
	- Condition:
		- Method: `GET`, `HEAD`, `POST`
		- Headers: `Accept`, `Accept-Language`, `Content-Language`, `Content-Type`
		- Content-Type: `from-urlencoded`, `multipart/from-data`, `text/plain`
	- In that case the browser makes the request to the resource, but if the domain is not allowed, the browser will "block" the resources meaning not returning it to the client.  
- Preflighted (2 steps)
	- Condition: Anything that does not fall in the Simple request category
	- Before doing the actual request to the resource, the browser sends a preflight request (`OPTION`) to get the CORS policy (the cache policy has a TTL). 
	- The preflight request sends the following `Origin`, `Access-Control-Request-Method` and `Access-Control-Request-Headers`. 
	- If the CORS policy doesn't allow the domain, the browser will not proceed with the actual request to the resource.


## Response Header 

- `Access-Control-Allow-Origin`
	- Allowed Origin singular (can only return one, manage an allow list in the backend). 
	- Possibles values: `my.website.com`, `*`, `null`
- `Access-Control-Allow-Credentials`
	-  Allows to include cookies with the request.
	- Possible values: `true`or `false`
- `Access-Control-Allow-Methods`
	- Allowed Methods.
	- Possible values: `GET`, `POST`, `PUT`, `DELETE`, `OPTIONS`
- `Access-Control-Allow-Headers`
	- Allowed Header.
	- Examples: `Content-Type`, `Authorization`, `X-Custom-Header`
- `Access-Control-Expose-Header`
	- Control which Headers are exposed to the client JS
	- By default only those are exposed: `Cache-Control`, `Content-Language`, `Content-Length`, `Content-Type`, `Expires`, `Last-Modified` `Pragma`.

Note:
`Access-Control-Allow-Origin: *` + `Access-Control-Allow-Credentials: true` is not allowed.


## Resources
- [CORS - LearnThatStack](https://www.youtube.com/watch?v=cGg7aRcIm8o)