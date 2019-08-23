# Using POSTMAN for QA Automation
 
This example shows how to use POSTMAN to run automation tests against an API

**Prerequisites:**     These only need to be installed once on your local development computer.

  [Java 8 Oracle or OpenJDK is preferred](https://openjdk.java.net/install/)  
  [Node.js 8+](https://nodejs.org/)  
  [POSTMAN](https://www.getpostman.com/)  
  [MAVEN](https://maven.apache.org/download.cgi)  
  
  Also need newman from the npm dependencies. after your install Node.js
``` bash 
% npm install -g newman
```

* [Getting Started](#getting-started)
* [Links](#links)
* [Testing](#testing)
* [License](#license)

## Getting Started


## TESTING

Utilizing a FAKE API for demonstration purposes. [FAKE API](http://fakerestapi.azurewebsites.net)

This API has the basic CRUD interface for multiple resources siuch as Activities, Books, and Authors.

We will use one of these resources to show how we can use postman to access the APi and then verify the data is correct.
 
Creating and running tests in POSTMAN is handled via the UI. 
The best way is to create a colleciton to store the API requests and tests.


### Integration of the API and Postman Collections and Environments  
Prequisite: Install newman. newman is the command line runner for POSTMAN tests.
``` bash 
% npm install -g newman
```
This will run the default tests against a local running API server that will be running via docker compose.
``` bash 
mvn clean verify -P postman-integration-tests  
```

Here is an example that would pass in an environment variable however its not used in thios project.
``` bash  
mvn clean verify -P postman-integration-tests -Dpostman.env=stage  
```


## License

Apache 2.0, see [LICENSE](LICENSE).