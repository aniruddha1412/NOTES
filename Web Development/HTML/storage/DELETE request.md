## Characteristics of DELETE Requests
1. **Idempotent**: Repeating a DELETE request for the same resource should yield the same result. Example: Trying to delete an already-deleted resource still results in a successful status.
2. DELETE requests generally do not include a body, as the resource to be deleted is identified in the URL.
3. DELETE requests are generally not cached.

## Anatomy of a DELETE Request
```plaintext
DELETE /users/123 HTTP/1.1
Host: example.com
Authorization: Bearer <token>
```

## DELETE Request Responses
A DELETE request typically returns one of the following status codes:
- **200 OK**: The resource was successfully deleted, and a response body may provide additional details.
- **204 No Content**: The resource was deleted successfully, and no further content is returned.
- **404 Not Found**: The resource to delete was not found.
- **403 Forbidden**: The client does not have permission to delete the resource.
- **400 Bad Request**: The request is malformed or invalid.