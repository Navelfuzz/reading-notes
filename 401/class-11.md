# CF 401: Java // Reading Notes

## Class 11: Spring App Basics, MVC, & Thymeleaf

## Readings

[Spring App Basics](https://spring.io/guides/gs/serving-web-content/)

### Questions

1. What role do the @Controller classes play in a Spring MVC application?
2. Explain to a non-technical friend what a GET request is.
3. What annotation should be placed on your Spring Boot application class?

### Answers

1. In a Spring MVC application, the `@Controller` classes play a crucial role in handling and processing incoming HTTP requests from clients (like web browsers or mobile apps). These classes are a part of the Spring Framework, which is a popular framework for building web applications. The `@Controller` annotation is used to mark a Java class as a controller, indicating that it will handle incoming requests.
When a user interacts with a web application (e.g., by clicking a link or submitting a form), their action triggers an HTTP request to the server. The `@Controller` classes listen for these requests and determine which method within the controller should handle each specific type of request (e.g., GET, POST, PUT, DELETE).
The methods inside the `@Controller` class are annotated with other annotations like `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc., to specify the URL path and the type of HTTP request they can handle. Once a request matches the URL and type specified in one of these methods, it gets executed, and the controller generates an appropriate response, often by returning data or rendering a view to be shown on the user's browser.
2. Imagine you're at a restaurant and you want to order something from the menu. When you tell the waiter what you want, you are making a "GET request." In simple terms, a GET request is like asking for information or requesting something specific from a server, just like you ask the waiter for a particular dish.
In the digital world, when you use a web browser or a mobile app, you're actually communicating with servers (big computers) that host websites and services. When you type a website's address in your browser or click on a link, your browser sends a GET request to the server, asking it to send back a specific web page or data. The server then processes your request and responds by sending the requested information back to your browser, which displays it for you to see.
3. In a Spring Boot application, the main class that serves as the entry point of the application should be annotated with `@SpringBootApplication`. This annotation is a combination of three other annotations: `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`.

[Spring MVC and Thymeleaf](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

### Questions

1. What method allows for a variable defined in Java (in your Spring Controller) to be dispalyed in HTML with the help of Thymeleaf?
2. Explain the role of a @Controller class in a Spring MVC application.
3. What is a model attribute refered to in Thymeleaf?

### Answers

1. In Thymeleaf, the method that allows a variable defined in a Java Spring Controller to be displayed in HTML is by using the `${variableName}` syntax. This syntax is part of Thymeleaf's expression language and is enclosed within the HTML tags or attributes. When the Thymeleaf template is processed and rendered on the server-side, the `${variableName}` expression is replaced with the actual value of the variable from the Spring Controller.
2. The role of a `@Controller` class in a Spring MVC application is to handle incoming HTTP requests from clients and provide appropriate responses. These classes are a central part of the Model-View-Controller (MVC) design pattern implemented in the Spring Framework.
3. In Thymeleaf, a model attribute refers to an object or data that is passed from a Spring Controller to the Thymeleaf template for rendering. When a Spring Controller method processes a request, it often needs to prepare some data that will be displayed in the HTML template.
