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
* Push to the remote master.

* Go to [Spring Initializr](https://start.spring.io/)
* Add the following dependencies
    * Config Server
    * Actuator
* Generate, unzip and add to your local git.
* Change properties to yml file. 
* Figure out how the config server fetches his configuration of `ws-config` for the correct microservice
    

### Spring Cloud Config Client
* Go to your microservices
* Enable the config client by adding it to your classpath. 
* Create a bootstrap.yml file. 
* Place the Spring application name in the bootstrap
* Remove the application.yml

### [Documentation](http://cloud.spring.io/spring-cloud-static/spring-cloud-config/1.2.3.RELEASE/#_spring_cloud_config_server)

## End Result
When starting up your microservices you will see a fetch happening to the config server. 
If it is successful, your work is done here. 

## Next step
`git checkout chpt4-Zuul`

