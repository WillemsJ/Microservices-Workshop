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

The next exercises will be done in Spring Data, if you need more help with your exercises please consult the [documentation](https://docs.spring.io/spring-data/jpa/docs/1.11.6.RELEASE/reference/html/)

### Rental Service

* Find me the movies that are still available.
* Get me the most recent rented movies.
* Get me the rented movies of Kevin VH.

#### Extra
* Make a save rental method where movie gets updated.
* Make a soft delete method on rental where the movie gets back available.



[Documentation](http://projects.spring.io/spring-cloud/spring-cloud.html#spring-cloud-feign)


## End result
Go to localhost:<port zuul>/rental/rentals/search
Here you will all the GET requests.
For the extra exercises, use Postman for performing the operations.

