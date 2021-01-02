# Spring Boot Microservice to Get Shortest Time and Connections between Cities

This project is based on two microservices developed using Spring Boot, Postgres and Docker. One Microservice provides data about Cities and Itineraries from a Postgres Database through a Rest Api. The other microservice consume the Rest Api and calculares Shortest time and connections paths between two cities using Dijkstra Algorithm. 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

1) [Java 1.8](https://www.java.com) - Java Version to compile and build the Microservices
2) [Maven](https://maven.apache.org/) - Maven to Build the Jars 
3) [Docker](https://www.docker.com/) - Deploy the containers for Postgres and Spring Boot

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be


1. Download the repository (https://github.com/DESCARTES25/ChallengeCompleteDocker)

2. Unzip the content in your local machine

3. Open a Console or Terminal (In my case Powershell)

	![alt text](https://github.com/DESCARTES25/ChallengeCompleteDocker/blob/master/powershell.png)

4. Build the Jar File for the Api Rest Microservice (Enter in **ChallengeRestApi-master** directory and launch **./mvnw clean install** )

	![alt text](https://github.com/DESCARTES25/ChallengeCompleteDocker/blob/master/ChallengeRestApi-master.png)

5. Build the Jar File for the Dijkstra Shortest City Path Rest Microservice (Enter in **Challenge-master** directory and launch **./mvnw clean install** ) 

	![alt text](https://github.com/DESCARTES25/ChallengeCompleteDocker/blob/master/Challenge-master.png)

6. Return to the Main directory **ChallengeCompleteDocker-master** and execute **docker-compose build** 

7. Return to the Main directory **ChallengeCompleteDocker-master** and execute **docker-compose up** 

## Testing the Services

Once the containers are running, the Postgres Database is filled with cities and itineraries, so we can test the service using these commands:

First, we can test the **Rest Api + Postgres** which is published in **localhost:8082**. (Using Postman)

![alt text](https://github.com/DESCARTES25/ChallengeCompleteDocker/blob/master/postman_get_cities.png)


	'''
	[
	    {
		"id": 1,
		"name": "Madrid"
	    },
	    {
		"id": 2,
		"name": "London"
	    },
	    {
		"id": 3,
		"name": "Berlin"
	    },
	    {
		"id": 4,
		"name": "Tokyo"
	    },
	    {
		"id": 5,
		"name": "Paris"
	    },
	    {
		"id": 6,
		"name": "New York"
	    }
	]

	'''

 

Later, we can test the **Shortest Path Rest Service** which is published in **localhost:8080**. 


## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Spring Boot](https://spring.io/) - The framework used to code the services
* [Maven](https://maven.apache.org/) - Dependency Management and Jar Building
* [Docker](https://www.docker.com/) - Used to deploy the services

## Authors

* **Daniel Escartín Daniel** - *Initial work* 




