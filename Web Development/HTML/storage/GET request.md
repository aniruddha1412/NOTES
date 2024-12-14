## Characteristics of GET Requests
1. **Idempotent**: Making the same GET request multiple times will result in the same outcome.
2. **Safe**: GET does not change the server state.
3. **Caching**: Responses from GET requests are often cached by browsers and intermediate servers (like CDNs) for faster access.
4. **Query Parameters**:
	- Data can be sent to server via the URL using query parameters.
	- Example: `https://example.com/search?query=books&sort=asc`

## Anatomy of a GET Request
```plaintext
GET /books?author=Hemingway HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
Accept: application/json
```

## Limitations of GET Requests
- Limited URL length.
- Not Secure for Sensitive Data as the query parameters are visible in the URL and can be cached also.
- Over-reliance on caching can cause stale data to be served.