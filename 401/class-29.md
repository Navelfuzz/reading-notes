# CF 401: Java // Reading Notes

## Class 29: Rooms & Rooms & Rooms

## Readings

[Overview: Saving data with Room](https://developer.android.com/training/data-storage/room)

[Defining entities in Room](https://developer.android.com/training/data-storage/room/defining-data)

[Related entities in Room](https://developer.android.com/training/data-storage/room/relationships)

[Accessing data with Room](https://developer.android.com/training/data-storage/room/accessing-data#java)

### Questions

1. What database engine is Room wrapped around? Do you think this is a good choice? Why or why not?
2. Do Rooms have any similarities to JPA?
3. Describe a DAO in your own words

### Answers

1. Room is wrapped around SQLite database engine. SQLite is good for mobile applications because it is lightweight and reliable. Room is an abstraction layer that makes SQLite easier to work with as it reduces the amount of boilerplate.
2. Yes. Both provide an abstraction layer over the underlying database engine, allowing developers wot work with objects instread of raw SQL. Both use annotations to map between objects and tables.
3. A DAO (Data Access Object) is an interface between the application and database. It defines methods for application interaction with the database (inserting, updating, deleting). It is a buffer allowing a developer to work with objects instead of the raw SWL. 
