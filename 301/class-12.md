# CF301 Reading Notes Class 12: CRUD

## Reading

[Status Codews Based on REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

### Questions

1. In your own words, describe what each group of status code represents:
    - 100’s = 
    - 200’s =
    - 300’s =
    - 400’s =
    - 500’s =
2. What is a status code 202?
3. What is a status code 308?
4. What code would you use if an update didn’t return data to a client?
5. What code would you use if a resource used to exist but no longer does?
6. What is the ‘Forbidden’ status code?

### Answers

1. Code Answers:
    - Header part of the request has been received and the server will try to comply with transmission command of the client.
    - Success codes.
    - Redirection codes.
    - Client Error codes.   
    - Server Error codes.
2. 'Accepted' by server but not yet processed. Asynchronous 
3. 308 is an HTTP status code that represents "Permanent Redirect." It is similar to the 301 (Moved Permanently) status code, but it instructs the client to use the redirected URL for future requests, without changing the request method. It indicates that the resource requested has been permanently moved to a different location.
4. If an update doesn't return data to a client, you would typically use the status code 204, which stands for "No Content." It indicates that the request was successfully processed, but there is no content to send back in the response payload. It is often used for operations that don't require a response body, such as deleting a resource.
5. If a resource used to exist but no longer does, the appropriate status code to use is 410, which stands for "Gone." It indicates that the requested resource is no longer available on the server and will not be available again in the future. Unlike the 404 (Not Found) status code, which implies a temporary absence, 410 explicitly states that the resource is permanently gone.
6. The "Forbidden" status code is represented by 403 in the HTTP protocol. It indicates that the server understands the client's request, but the server is refusing to fulfill it. This status code is typically used to indicate that the client does not have sufficient permissions to access the requested resource. It is a way for the server to communicate that the requested action is forbidden or prohibited.


## Videos

[Build A REST API with Node.js, Express, & MongoDB - Quick](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

### Questions

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
2. What is middleware?
3. What does app.use(express.json()) do?
4. What does the /:id mean in a route?
5. What is the difference between PUT and PATCH?
6. How do you make a default value in a schema?
7. What does a 500 error status code mean?
8. What is the difference between a status 200 and a status 201?

### Answers

1. It is recommended to pull the MongoDB database string out of the server code and put it into the .env file for security and flexibility reasons. Storing sensitive information like database credentials in the code itself can pose a security risk, especially if the code is version-controlled or shared publicly. By using an environment variable (stored in the .env file), you can keep the sensitive information separate from the codebase. This approach allows you to easily manage different configurations for different environments (e.g., development, staging, production) without modifying the code.
2. Middleware is a concept in web development that refers to a function or set of functions that sits between the incoming request and the final route handler. It acts as a bridge to perform various tasks such as request preprocessing, authentication, logging, error handling, and more. Middleware functions can modify the request or response objects, execute additional code, or terminate the request-response cycle. They provide a way to add modular and reusable functionality to an application's request processing pipeline.
3. this is middleware used in Express.js to parse incoming requests with JSON payloads. It is responsible for parsing the request body, assuming it is in JSON format, and attaching the parsed data to the `req.body` property. 
4. In a route, the /:id is a route parameter or a dynamic segment that represents a variable part of the URL. The :id syntax allows you to define a placeholder for a value that can be extracted from the URL during the request handling process. For example, a route like /users/:id can match URLs such as /users/123 or /users/abc, where 123 and abc would be the values extracted for the id parameter in the request handler.
5. PUT is used to completely replace or update an existing resource with the request payload. PATCH, is used to partially update a resource.
6. For default properties we would:

        const userSchema = new mongoose.Schema({
            name: {
                type: String,
                default: 'John Doe'
            },
            age: {
                type: Number, 
                default: 25
            }
        });

7. indicates an internal server error. It is a generic error responpse that indicates something unexpected went wrong on the server-side, preventing it from fulfilling the request.
8. 1
8. Real answer: 200 (OK) - Request has been processed. It typically implies that the request was understood, accepted, and the server was able to respond with the requested resource operation. 201 (Created) - also a success code but has specific meaning when used in combination with POST requests. It indicates that the request has been successfully processed, and as a result, a new resource has been created on the server. 
