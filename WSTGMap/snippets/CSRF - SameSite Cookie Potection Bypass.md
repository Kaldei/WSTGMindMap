#csrf

## No anti-CSRF token and SameSite Lax
Use GET request to bypass Lax. If "Method not allowed" use the method override of the framework used: 
- Symfony: `<input type="hidden" name="_method" value="GET">`

