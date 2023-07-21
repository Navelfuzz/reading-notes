# CF 401: Java // Reading Notes

## Class 09: High-level HTTP & Java

## Readings

[Review: High-level HTTP](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)

### Questions

1. What are the five steps in the HTTP Request Lifecycle?
2. What are the two things the client needs before it can make an HTTP Request?
3. Explain the four way handshake and what it does.

### Answers

1. DNS Resolution, Establishing TCP Connection, Sending HTTP Rqst, Processing Rqst @ Server, Sending HTTP Response
2. URL & HTTP method (GET POST PUT DELETE)
3. Client Sends SYN, Server Sends SYN-ACK, Client Sends ACK, Connection Established

[Java HTTP Request example](https://www.baeldung.com/java-http-request)

### Questions

1. True or False: When making an HTTP request, you MUST follow any redirect returned by the request. Back up your answer.
2. Which built-in Java class can be used to perform an HTTP request?
3. What HTTP status codes represent a successful response? A redirect? A client error?

### Answers

1. False: When making an HTTP request, following redirects is not mandatory. The HTTP specification allows servers to send redirect responses (e.g., status codes 301, 302, 307, etc.) with location headers, indicating that the requested resource has moved to a different URL. However, whether to follow redirects or not is determined by the client, and it depends on the configuration or implementation of the client application. Some clients automatically follow redirects by default, while others may require manual handling of redirects or even choose not to follow them at all.
2. In Java, the built-in class that can be used to perform an HTTP request is HttpURLConnection. It is available in the java.net package and provides basic support for making HTTP requests to a server and handling responses.
3. HTTP status codes are three-digit numbers returned by the server to indicate the result of the HTTP request. Here are some common HTTP status codes representing different types of responses:

**Successful Responses (2xx):**

* 200 OK: The request was successful, and the server has returned the requested data.
* 201 Created: The request was successful, and the server has created a new resource as a result.
* 204 No Content: The server successfully processed the request, but there is no data to send back (typically used for DELETE requests).

**Redirect Responses (3xx):**

* 301 Moved Permanently: The requested resource has moved permanently to a new URL, and all future requests should be directed to that URL.
* 302 Found: The requested resource temporarily resides under a different URL. It is often used for temporary redirects.
* 307 Temporary Redirect: Similar to 302, but the request method should not be changed when following the redirect.

**Client Error Responses (4xx):**

* 400 Bad Request: The server could not understand the request due to client error (e.g., malformed request syntax).
* 401 Unauthorized: Authentication is required, and the client must provide valid credentials to access the requested resource.
* 404 Not Found: The requested resource could not be found on the server.

