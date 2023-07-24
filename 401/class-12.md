# CF 401: Java // Reading Notes

## Class 12: Spring: Accessing Data & JPA, Comparing Repositories (Baeldung)

## Readings

[Spring guide: Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

### Questions

1. How are query methods defined when using Spring Data JPA?
2. Which dependencies will you need in order to complete the Spring guide?
3. What annotations are used to specify an auto generated identification number for an Entity?

### Answers

1. When using Spring Data JPA, query methods are defined by simply declaring method signatures in a Spring Data repository interface. Spring Data JPA will automatically generate the query based on the method name, eliminating the need to write explicit SQL queries.
2. To complete the Spring guide, you will need the following dependencies in your Spring Boot project:
* `spring-boot-starter-web`: This provides essential web-related functionalities for building web applications using Spring Boot.
* `spring-boot-starter-data-jpa`: This dependency sets up Spring Data JPA with Hibernate as the JPA provider, making it easy to work with databases.
* `h2`: This is an in-memory database that allows you to persist and retrieve data during the application's runtime. It is commonly used for testing and development.
* `spring-boot-starter-thymeleaf`: Thymeleaf is a popular templating engine used for rendering HTML pages, and this dependency enables its integration with Spring Boot.
* Other dependencies may be needed depending on the specific Spring guide you are following, but these are the core dependencies that are commonly used.
3. To specify an auto-generated identification number (primary key) for an Entity in Spring Data JPA, you use the `@GeneratedValue` annotation in combination with `@Id`. Typically, the `@Id` annotation is used to mark a field in the Entity class as the primary key, and `@GeneratedValue` is used to indicate that the value for this field will be generated automatically by the underlying database.

[Baeldung: Comparing Repositories](https://www.baeldung.com/spring-data-repositories)

### Questions

1. Which of the Spring Data Repositories covered in the readings has the most methods available to it?
2. Name a downstide of a Spring Data Repository.
3. How would you define an operation to find a student based on their name in a repo named StudentRepository which extends JpaRepository?

### Answers

1. JpaRepository contains the full APIs of CRUD and PagingAndSortingRepository
2. We have to be careful not to expose internal implementation details or let Crud limit control over methods.
3. In a Java-based project, if you have a repository named `StudentRepository` that extends `JpaRepository`, it means you are using Spring Data JPA. This repository allows you to perform CRUD (Create, Read, Update, Delete) operations on the `Student` entity, where `Student` is the entity representing a student record in your application.

To find a student based on their name, you can define a method in the `StudentRepository` interface following Spring Data JPA's query method naming conventions. The method should start with "findBy," followed by the name of the property you want to use for the search, in this case, "name." Spring Data JPA will automatically generate the query based on the method name.

Here's how you would define the operation to find a student by name:

import org.springframework.data.jpa.repository.JpaRepository;

        public interface StudentRepository extends JpaRepository<Student, Long> {
            // Method to find a student by their name
            Student findByName(String name);
        }
