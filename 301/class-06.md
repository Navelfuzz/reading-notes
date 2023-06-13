# CF301 Reading Notes Class 06: REST

## Readings

[What Google Learned from its Quest to Build the Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)

### Questions

1. To what extent did psychological safety impact your previous work experience?
2. How does this article inform your approach to working with others moving forward?

### Answers

1. I would say to a moderate effect due to an abrasive amount of people thinking their rank/grade is only properly recognized by the acknowledgment their ego receives.
2. I think it just serves as a reminder to me to keep in mind how important it is to be respectful of the poeple you work with and their needs and you'll likely find that reciprocated.

[How I explained REST to my brother](https://gist.github.com/brookr/5977550)

### Questions

1. Who is Roy Fielding?
2. Why don’t the techniques that we use in this class work well when we need to be able to talk to all of the machines in the world?
3. What is the HTTP protocol that Fielding and his friends created?
4. What does a `GET` do?
5. What does a `POST` do?
6. What does `PUT` do?
7. What does `PATCH` do?

### Answers

1. Some guy. He's smart. He's an American computer scientist and one of the principal authors of the HTTP specificiation and the originator of the `Representational State Transfer` also known as `REST` architectural style.
2. per the article, we aren't using a system that allows our code to be recognized with all of those machines. We are using a narrow representation of our information and sharing it amongst an isolated group that agrees to use machines in a very specific way. Whereas if we were using APIs we would have a way of braking out of that paradigm and joining the rest of the properly connected machines on the interwebs.
3. `Hypertext Transfer Protocol` is a model which `URL` is used to access a formated document.
4. A method which retrieves data from a server. It is read-only.
5. This method sends data to the server and creates a new resource. The resource it creates is subordinate to some other parent resource.
6. The PUT method is used to update an existing resource. If you want to update a specific resource (which comes with a sprecic URI) you can call the PUT method to that resource URI with the request body containing the complete new version of the resource you are tyring to update.
7. Similar to PUT as it updates an existing resource. However the difference is that PATCH can update specific details in its request body, whereas PUT requires a complete version. PATCH requires less info in the request body.

## API Keys

### API Keys Obtained:

Geocoding API
Weather Bit API
YELP API
Movie DB API