HTTP status codes are three-digit numbers returned by the server to indicate the outcome of an HTTP request.

HTTP status codes are divided into five classes, each serving a distinct purpose.

---

### 1. Informational (1xx)
These status codes indicate that the server has received the request and is continuing the process. These are rarely used in practice.

- **100 Continue**: The client should continue with the request, or ignore if the request has already been completed.
- **101 Switching Protocols**: The server is switching protocols as requested by the client (e.g., upgrading to WebSocket).
- **102 Processing** (WebDAV): The server has received the request, but the processing is not yet complete.

**Common use**: These are typically used for debugging or during long processes.

---

### 2. Successful (2xx)
These codes indicate that the request was successfully processed by the server. If a request is successful, it will typically return one of the following:

- **200 OK**: The request was successful, and the server has returned the requested data (for GET requests) or performed the requested action (for POST, PUT, or DELETE).
    - **Example**: A `GET` request that retrieves data or a `POST` request that successfully creates a resource.
	
- **201 Created**: The request has been fulfilled, and a new resource has been created. Often used with `POST`.
    - **Example**: A user profile has been created after a `POST` request.
	
- **202 Accepted**: The request has been accepted for processing, but the processing has not been completed. This does not guarantee the action will be successful.
    - **Example**: A request to process a background task.
	
- **204 No Content**: The request was successful, but there is no content to return. Often used after a successful `DELETE` request or when there’s no content to return for `PUT`.
    - **Example**: A `DELETE` request that removes a resource but doesn't return any data.
	
- **205 Reset Content**: The server successfully processed the request and suggests the client reset the document view.
    
- **206 Partial Content**: The server is returning a portion of the resource, typically used for partial downloads (e.g., `Content-Range` header for large files).
    - **Example**: A client requests part of a large file for download.

---

### 3. Redirection (3xx)
These status codes indicate that the client must take additional action to complete the request, typically by following a different URL.

- **300 Multiple Choices**: The requested resource has multiple representations, and the user must choose one. (Rarely used in practice)
    
- **301 Moved Permanently**: The resource has been permanently moved to a new URL. Future requests should use the new URL.
    - **Example**: A website that has permanently changed its domain name.
	
- **302 Found** (Previously "Moved Temporarily"): The resource has been temporarily moved to a different URL. The client should continue to use the original URL for future requests.
    - **Example**: A temporary redirect, like when a user is redirected to a login page after attempting to access a restricted area.
	
- **303 See Other**: The server is redirecting the client to a different URL (typically used after a `POST` request to avoid resubmission).
    
- **304 Not Modified**: The resource has not been modified since the last request. This is used for caching purposes, indicating the client can use its cached version.
    - **Example**: A browser checking if the page has changed before rendering.
	
- **307 Temporary Redirect**: The resource has been temporarily moved to a different URL, but unlike 302, the client must repeat the request with the original method (e.g., `POST` remains `POST`).
    
- **308 Permanent Redirect**: Similar to 301, but the client must repeat the request using the same method (e.g., `POST` remains `POST`).
    
---

### 4. Client Error (4xx)
These status codes indicate that there was an error with the client's request, either due to incorrect syntax or unauthorized access.

- **400 Bad Request**: The server could not understand the request due to invalid syntax. This is a general error for incorrect requests.
    - **Example**: Missing parameters or an incorrect JSON format in the request body.
	
- **401 Unauthorized**: The client must authenticate to access the resource. This is typically used when authentication credentials are missing or incorrect.
    - **Example**: A request for a protected resource without a valid API key or token.
	
- **402 Payment Required**: Reserved for future use, often used in payment-related systems.
    
- **403 Forbidden**: The client is authenticated but does not have permission to access the resource.
    - **Example**: A user trying to access an admin-only page.
	
- **404 Not Found**: The requested resource could not be found on the server. This is one of the most common status codes.
    - **Example**: A URL that doesn’t exist.
	
- **405 Method Not Allowed**: The HTTP method used is not allowed for the requested resource.
    - **Example**: A `POST` request made to a resource that only accepts `GET`.
	
- **406 Not Acceptable**: The server can serve the resource but the client requests a format that the server does not support for that particular resource.
    
- **408 Request Timeout**: The server timed out waiting for the request from the client.
    - **Example**: A client takes too long to send the request data.
	
- **410 Gone**: The resource is no longer available and has been permanently removed.
    - **Example**: A deleted page or deprecated API endpoint.
	
---

### 5. Server Error (5xx)
These status codes indicate that there was an error with the server itself, meaning the problem lies on the server side and not with the client's request.

- **500 Internal Server Error**: A generic error message indicating the server encountered an unexpected condition that prevented it from fulfilling the request.
    - **Example**: A bug or misconfiguration on the server.
	
- **501 Not Implemented**: The server does not support the functionality required to fulfill the request.
    - **Example**: Trying to use an unsupported HTTP method.
	
- **502 Bad Gateway**: The server, while acting as a gateway or proxy, received an invalid response from the upstream server.
    - **Example**: A proxy server failing to communicate with an upstream server.
	
- **503 Service Unavailable**: The server is temporarily unavailable, typically due to being overloaded or down for maintenance.
    - **Example**: A website temporarily unavailable due to maintenance.
	
- **504 Gateway Timeout**: The server, acting as a gateway or proxy, did not receive a timely response from an upstream server.
    
- **505 HTTP Version Not Supported**: The server does not support the HTTP protocol version used in the request.