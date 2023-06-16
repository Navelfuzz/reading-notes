# CF301 Reading Notes Class 08: APIs

## Readings

[API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)

### Questions

1. What does REST stand for?
2. REST APIs are designed around a ____.
3. What is an identifier of a resource? Give an example.
4. What are the most common HTTP verbs?
5. What should the URIs be based on?
6. Give an example of a good URI.
7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
8. What status code does a successful `GET` request return?
9. What status code does an unsuccessful `GET` request return?
10. What status code does a successful `POST` request return?
11. What status code does a successful `DELETE` request return?

### Answers

1. Representational State Transfer
2. Resource
3. Uniform Resource Identifier (URI). From Microsofts page: https://adventure-works.com/orders/1 would be a particular customer order
4. Post, Get, Put, & Delete
5. Nouns
6. `https://adventure-works.com/customers/5/orders`
7. A "chatty" API is one that imposes a larger load on the web server. This will incur more requests for what is essentially requests for improperly organized/built APIs.
8. 200
9. 404
10. 201
11. 204
