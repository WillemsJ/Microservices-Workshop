# Chapter 5: The Inter-service/Inter-process communication 
When choosing a communication protocol between our microservices, the most used are REST and messaging. 
In this exercise, we will cover REST with Feign as communication client. 
Feign opens a channel and consumes endpoints between two microservices by setting up a REST client in your application.
Since the microservice you are communicating with will be secured, we will need to add security to our Feign client. 
Feign has integrated resilience and client-side load balancing inside the client.
Therefore, using the Feign client will prevent cascading failures and provide a fallback mechanism.

## Exercise 
* Add the Feign dependency to the rental and movie service
With the help of only one annotation, all default configuration has been done for you.
Just add @EnableFeignClients on top of your application class and you're good to go.

* Create a Feign client interface 
* //TODO 


## End result
When 

