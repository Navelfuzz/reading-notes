# CF301 Reading Notes Class 11: MongoDB and Mongoose

## Reading

[SQL vs. NoSQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

### Questions

1. Fill in the chart below with five differences between SQL and NoSQL databases:
2. What kind of data is a good fit for an SQL database?
3. Give a real world example.
4. What kind of data is a good fit a NoSQL database?
5. Give a real world example.
6. Which type of database is best for hierarchical data storage?
7. Which type of database is best for scalability?

### Answers

1. Table:

|SQL|NoSQL|
|---|-----|
|Relational databases with predefined schemas|Non-relational databases with dynamic schemas|
|Structured Query Language (SQL) is used for querying data|Querying is often done using alternative methods or APIs|
|ACID (Atomicity, Consistency, Isolation, Durability)|BASE (Basically Available, Soft state, Eventually consistent)|
|Suitable for complex and structured data|Suitable for unstructured or semi-structured data|
|Support for joins and complex transactions|No support for joins and limited transactional support|
2. SQL databases are a good fit for structured and relational data. They excel at handling complex relationships and enforcing data integrity through the use of predefined schemas.
3. Real-world example: An e-commerce website that stores information about products, orders, customers, and their relationships. The data in this scenario has well-defined structures, and the relationships between entities can be clearly defined and enforced using SQL databases.
4. NoSQL databases are a good fit for unstructured or semi-structured data. They are designed to handle large volumes of rapidly changing and diverse data. They provide flexibility and scalability.
5. Real-world example: A social media platform that stores user-generated content such as posts, comments, likes, and followers. The data in this scenario is often unstructured, varying in format, and can be highly dynamic. NoSQL databases can handle the scalability requirements of such platforms.
6. NoSQL databases are typically a better fit for hierarchical data storage. They allow for flexible and dynamic schemas, which can accommodate varying levels of nesting and complexity in the data structure.
7. NoSQL databases are generally better suited for scalability due to their distributed nature and ability to scale horizontally. They can handle large amounts of data and high traffic loads more effectively compared to traditional SQL databases.

## Videos

[SQL vs. NoSQL or MySQL vs. MongoDB](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

### Questions

1. What does SQL stand for?
2. What is a relational database?
3. What type of structure does a relational database work with?
4. What is a ‘schema’?
5. What is a NoSQL database?
6. How does it work?
7. What is inside of a MongoDB database?
8. Which is more flexible - SQL or MongoDB? and why.
9. What is the disadvantage of a NoSQL database?

### Answers

1. SQL stands for Structured Query Language.
2. A relational database is a type of database that organizes data into tables with rows and columns. It allows for the establishment of relationships between tables through keys, enabling efficient data retrieval and manipulation.
3. A relational database works with a tabular structure, where data is organized into tables. Each table consists of rows (records) and columns (attributes) that define the data structure.
4. A schema in the context of relational databases refers to the structure and organization of the database. It defines the tables, columns, data types, relationships, constraints, and rules that govern the data storage and manipulation.
5. A NoSQL database, also known as a non-relational database, is a type of database that does not follow the traditional relational model. It provides a flexible and schema-less approach to data storage, allowing for the storage and retrieval of unstructured or semi-structured data.
6. NoSQL databases work by storing data in various formats like key-value pairs, documents, wide-column stores, or graphs. They focus on scalability and performance by distributing data across multiple servers. NoSQL databases typically offer high availability, horizontal scaling, and flexible data models.
7. Inside a MongoDB database, the data is organized into collections, which are analogous to tables in a relational database. Each collection contains multiple documents, which are JSON-like data structures. Documents within a collection can have varying structures, providing flexibility to store different types of data.
8. MongoDB, being a NoSQL database, is generally considered more flexible than traditional SQL databases. It offers a dynamic and schema-less data model, allowing for the storage of varying data structures within a collection. This flexibility enables agile development and accommodates evolving data requirements without requiring strict schema definitions.
9. One disadvantage of NoSQL databases is the lack of support for complex queries involving multiple collections or relationships. NoSQL databases prioritize scalability and performance, often sacrificing some of the advanced querying capabilities offered by SQL databases. Additionally, NoSQL databases may have limited transactional support and may require additional effort for maintaining data consistency and integrity in certain scenarios.
