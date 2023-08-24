# CF 401: Java // Reading Notes

## Class 32: GraphQL & Serverless

## Readings

[Intro to Serverless](https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9)

[AWS Amplify](https://aws.amazon.com/amplify/)

[GraphQL Intro](https://docs.amplify.aws/cli/graphql/data-modeling/)
- Just read the first few paragraphs, up until the query code

### Questions

1. What makes an API RESTful?
2. What is the benefit of using GraphQL? Any downsides?
3. Describe “serverless” to a new 301 Code Fellows student.

### Answers

1. RESTful APIs adhere to a set of architectural principles, including:
* Client-server architecture: The client and server are separate and communicate through a uniform interface.
* Statelessness: Each request from the client to the server contains all the information necessary to complete the request, and the server does not store any client state between requests.
* Cacheability: Responses from the server can be cached by the client to improve performance.
* Layered system: The client can access the server through a series of intermediate layers, such as load balancers or proxies.
* Uniform interface: The interface between the client and server is standardized, typically using HTTP methods (GET, POST, PUT, DELETE) and resource URIs.
2. The main benefit of using GraphQL is that it allows clients to request only the data they need, reducing the amount of data transferred over the network and improving performance. It also allows for more flexible queries, as clients can specify the shape and structure of the data they want. However, there are some downsides to using GraphQL, such as increased complexity and a steeper learning curve compared to traditional REST APIs. Additionally, some developers argue that GraphQL can lead to over-fetching or under-fetching of data if not used carefully.
3. Serverless is a cloud computing model where the cloud provider manages the infrastructure and automatically scales resources up or down based on demand. In a serverless architecture, developers write code in the form of functions that are triggered by events, such as HTTP requests or changes to a database. The cloud provider then runs these functions on a serverless platform, such as AWS Lambda or Azure Functions, and charges based on the number of function invocations and the amount of resources used. Serverless architectures can be more cost-effective and scalable than traditional server-based architectures, but they also come with some limitations, such as shorter execution times and limited control over the underlying infrastructure.
