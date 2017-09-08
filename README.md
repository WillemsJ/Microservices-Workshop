# Chapter 5: The Inter-service/Inter-process communication 
When choosing a communication protocol between our microservices, the most used are REST and messaging. 
In this exercise, we will cover REST with Feign as communication client. 
Feign opens a channel and consumes endpoints between two microservices by setting up a REST client in your application.
Since the microservice you are communicating with will be secured, we will need to add security to our Feign client. 
Feign has integrated resilience and client-side load balancing inside the client.
Therefore, using the Feign client will prevent cascading failures and provide a fallback mechanism.

## Exercise 
Add the Feign dependency to the rental and movie service.
With the help of only one annotation, all default configuration has been done for you.
Just add @EnableFeignClients on top of your application class and you're good to go.

The next exercises will be done in Spring Data, if you need more help with your exercises please consult 
[Spring Data JPA](https://docs.spring.io/spring-data/jpa/docs/1.11.6.RELEASE/reference/html/)
[Spring Data REST](https://docs.spring.io/spring-data/rest/docs/current/reference/html/)

### Movie Service
* Find me the movies that are still available.
### Rental Service
* Make a save method where rental gets saved and movie becomes unavailable.
  * Check first if the movie is available before saving.
* Make a soft delete method on rental where the movie gets back available.

### Tip 1
For making the Rental exercises happen, we will have to duplicate Movie class inside the Rental service to let the Feign Client work.
You can still choose which properties you would like to receive.
For example: creating a class with only the title.

### Tip 2
To receive an array from another microservice, use Resources<> around your object instead of List<>

### POST JSON body
```
{
   "name":"Kirk",
   "rentDate":"2017-09-09",
   "endDate":"2017-09-11",
   "movies": ["The Matrix","Blade Runner","Iron Man 3"]
}

```

[Documentation](http://projects.spring.io/spring-cloud/spring-cloud.html#spring-cloud-feign)

## End result
Go to localhost:<port zuul>/rental/movies/search for the first exercise
For the further exercises, use Postman for performing the operations.


