# CF 401: Java // Reading Notes

## Class 13: Spring tests and relationships

## Readings

[Related data in Spring (only read section 3 (One-to-Many Relationship)](https://www.baeldung.com/spring-data-rest-relationships#one-to-many-relationship)

### Questions

1. Name a few real life examples of “One To Many” relatioships.
2. Given two entities, one named Player and one named Team, if you wanted to create a one to many relationship with those entities which would be the one and which would be the many?
3. Explain one to many relationships to a non-technical friend.

### Answers

1. Parent and Children: A parent can have multiple children, but each child has only one parent (in most typical family structures). Teacher and Students: A teacher can have many students in a classroom, but each student has only one teacher for that class. Company and Employees: A company can have many employees, but each employee works for only one company.
2. In this scenario, the "one" would be the "Team," and the "many" would be the "Player." This means that one team can have multiple players, but each player is associated with only one specific team.
3. Imagine you have a box of crayons and several sheets of paper. Each crayon box (the "one") is associated with many sheets of paper (the "many"). So, you take one crayon box and use it to draw on multiple sheets of paper. However, each sheet of paper is only connected to one specific crayon box. In the same way, a one-to-many relationship in databases or real life means that there is a connection between two sets of things where one set (the "one") is related to many elements in the other set (the "many"). The "many" elements can belong to only one of the "one" elements, just like each sheet of paper belongs to only one crayon box. This type of relationship is common in various situations, such as parents and their children, a company and its employees, or a team and its players.

[Baeldung: Spring Integration Testing](https://www.baeldung.com/integration-testing-in-spring)

### Questions

1. Describe the difference between a unit test and an integration test.
2. What is the object that provides support for Spring MVC Testing?
3. What does the “perform()” method do in a Spring integration test?

### Answers

1. An integration test aims to check how multiple units or components of a software application work together and interact with each other. It verifies the integration points between different parts of the application, such as APIs, services, or databases. Integration tests provide confidence that the various parts of the application function correctly when combined. Unlike unit tests, integration tests may involve real dependencies and external resources, making them slower and sometimes more complex to set up. Wheras unit tests only test a small piece of code and have limited dependencies.
2. The object that provides support for Spring MVC Testing is the "MockMvc" class.
3. The "perform()" method in a Spring integration test (using MockMvc) is used to execute an HTTP request against a specific controller endpoint.
