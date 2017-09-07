# Chapter 2: Service Registry 
Since we are working with a distributed system, the services don't know of each other existence.
So how do we let the services discover each other for querying data, etc...? 
To tackle this issue, Spring Cloud provides us the ability to register our services with Eureka.
Eureka as a service is comparable to a phone book for your microservices.
Each service registers itself with the service registry and tells the registry where it lives.

## Exercise
* Go to [Spring Initializr](https://start.spring.io/)
* Name the project eureka
* Add the Eureka Server dependency
* Generate, unzip and add it to your local git folder
* [Link](http://cloud.spring.io/spring-cloud-static/spring-cloud-netflix/1.3.4.RELEASE/) the two microservices to the Eureka server. 
* Run the three applications.

If you found the solution, the logs will tell you that they register themselves with Eureka.

## End result
* Go to the Eureka application: localhost:<port>/eureka 
* You should now see an UI Eureka dashboard with both the microservices registered.


## Next step
 ```sh
   git checkout chpt3-ConfigServer
   ```





