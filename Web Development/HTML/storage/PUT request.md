## Characteristics of PUT Requests
1. **Idempotent**: Repeated identical PUT requests will produce the same outcome.
2. A PUT request replaces the entire resource with the data in the request body.
	- For partial updates, a [[PATCH request]] is used instead.
3. Data is sent in the body of the request.
4. Responses to PUT requests are generally not cached.
5. PUT requests can also be designed to create resource if it does not exist.

## Anatomy of a PUT Request
```plaintext
PUT /books/1 HTTP/1.1
Host: example.com
Content-Type: application/json
Content-Length: 62

{
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald"
}
```

## Responses from PUT Request
- **200 OK**: Indicates the resource was successfully updated.
- **204 No Content**: Indicates that the request was successfully processed, but no response body is returned to the client.
- **400 Bad Request**: Indicates invalid input data.
- **404 Not Found**: Indicates the resource to be updated was not found.