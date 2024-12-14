## Characteristics of PATCH Requests
1. Only the fields specified in the request body are modified (partial updates).
2. The request body contains only the fields to be updated.
3. PATCH is not designed to create a resource if it does not exist (unlike PUT).

## Anatomy of a PATCH Request

```plaintext
PATCH /books/1 HTTP/1.1
Host: example.com
Content-Type: application/json
Content-Length: 39

{
  "title": "The Great Gatsby"
}
```

## Response from PATCH Request
A patch request should return an appropriate status code: 
- **200 OK**: Indicates the resource was successfully updated.
- **204 No Content**: Indicates that the request was successfully processed, but no response body is returned to the client.
- **400 Bad Request**: Indicates invalid input data.
- **404 Not Found**: Indicates the resource to be updated was not found.