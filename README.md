# Very difficult coding challenge

These are the tasks for the very difficult coding challenge. 

## 1. Git

Check out the source code from this git repository: 

```
https://github.com/reiz/analytics_ms-0
```

## 2. Install dependencies

Take a look at the project and install all the dependencies with the package manager which is used in the project. 

## 3. IDE

Create meta files for your desired IDE through the package manager.

## 4. Open the project in an IDE

Open the project in your favorite IDE. Your favorite IDE is either Eclipse or IntelliJ IDEA. 

## 5. Compile 

Compile the project with mvn. If it doesn't compile, fix it! 

## 6. Package 

Package the project into a JAR file, without running the tests. 

## 7. Run 

Run the JAR file. If the application doesn't come up correctly, fix it!

The application has a dependency to MongoDB. Make sure that a MongoDB instance is running. 
If that is not the case, you can start a MongoBD Docker Container with this command: 

```
docker run --name mongodb -p 27017:27017 -p 28017:28017 -d versioneye/mongodb:3.4.6
```

## 8. Extend - Create Endpoint

After you fixed the application and make it run successfully, 
you can reach it in the browser under `http://localhost:8080`. 
There are 2 Endpoints available: 

 - `http://localhost:8080/logs`
 - `http://localhost:8080/logs/count`

Add another Endpoint which is available under `http://localhost:8080/logs/create` through HTTP POST. 
The Endpoint should accept a JSON payload in the HTTP Body, build a `Log` Model out of it 
and create a new entry in the database.

You can use Postman to build and fire an HTTP POST Request. 

## 9. Extend - Get By ID

Add another Endpoint which is available under `http://localhost:8080/logs/{id}`. 
The last part should be the primary ID of the Log entity in the database. 
The Endpoint should load the corresponding object from the database and 
return it's JSON representation via HTTP Response. 

## 10. Extend - Scheduler

There is a class `ScheduledTask` with the method `runBackgroundJob()`. 
Configure the application that way, that the method is executed every 5 seconds in the background. 

## 11. Build the Docker image

Build a Docker image with the application in it and call it `liveperson/spring:0.0.1`. 

## 12. Run Docker

Run the Docker container that way that the application is available under `http://localhost:8080` on the Host system.
