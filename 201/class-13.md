# Readings Class 13: Local Storage and How to use it on Websites

*Questions*

1. Why would a developer use local storage for a web application?
2. What information should not be stored in local storage?
3. Local storage can store what type of data? How would you convert it to that type before storing?

*Answers*

1. Because web apps are "stateless" meaning you have a singular use instance of ongoing data. Local storage
will allow you to "save" progress and return to it later.
2. user data/information.
3. Strings only. Use: `JSON.stringify()` and `JSON.parse()`
