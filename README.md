# Chapter 3: Spring Cloud Config Server 
Aside from discovering our services, we need a way to centralize and externalize our configuration.
In the theory class, we explained that we follow the 12 factor app as guidelines in building microservices. 
One of these principles is a strict separation of config from code.
This is because config varies substantially across deploys, code does not. 
Spring Cloud Config server provides an HTTP, resource-based API for external configuration to tackle this issue.

## Exercise 

### Spring Cloud Config Server
The Config server needs a repository where all the config is stored. 
* Go to your GitHub and add a new repository.
* Name this `ws-config` and clone the repo. 
* Add a yml file for each microservice named after the configured application name.

{% highlight yml %}
 spring:
   application:
     name: applicationName
{% endhighlight %}

* Go to [Spring Initializr]
* Add the following dependencies
    * Eureka Discovery
    * Config Server
    * Actuator
* Generate, unzip and add to your local git.
* Figure out how the config server fetches his configuration of `ws-config` for the correct microservice
    

### Spring Cloud Config Client
* Go to your microservices
* Enable the config client by adding it to your classpath. 
* Create a bootstrap.yml file. 
* Configure the config client in the bootstrap.
* Find out how to fetch the configuration of the server.



# Next step
`git checkout chpt4-Zuul`

