# Chapter 4: Spring Cloud Zuul
To unify our traffic to one service, we will be implementing an edge service application.
Take it as the gateway to your microservices, where you can stop, pass through and modify requests to the downstream services.
If you decide to scale up your microservice to 2 instances, Zuul will load balance requests to both instances to reduce load. 
For routing to the microservices our goal is to define the correct route to the correct service. 
For example /rental is mapped on rental service and /movie on the movie service.
With the help of Eureka, Zuul will find the correct microservices to handle the requests to.

## Exercise 
* Go to [Spring Initializr](https://start.spring.io/)
* Add following dependencies
    * Zuul
    * Eureka Discovery
    * Config Client
* Generate, unzip, put it in your local git.
* Change properties into yml.
* Externalize your configuration to the ws-config repo.
* Enable the reverse proxy by adding @@EnableZuulProxy on top of your application.
* Make it possible to fetch configuration from the config server.
* Make it possible to discover the microservices.

## End result
When starting all your applications, go to your Zuul address and try out your routing to the microservices.
Example: localhost:9090/rental/rentals

## Next Step
`git checkout chpt5-FeignClient`
