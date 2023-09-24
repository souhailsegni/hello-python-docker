# hello-python-docker
Python-docker
Hello world Application

Developing stack:

Python Flask:Python Flask is a lightweight web framework for building web applications. It simplifies the process of developing web applications by providing tools and libraries for routing, handling HTTP requests and responses, and creating web APIs. Flask is known for its simplicity and flexibility, making it a popular choice for building small to medium-sized web applications and microservices in Python.

PostgreSQL:PostgreSQL is a powerful, open-source relational database management system (RDBMS) known for its robustness, extensibility, and reliability. It is commonly used to store and manage structured data, offering features such as ACID compliance, advanced indexing, and support for complex data types. PostgreSQL is known for its strong community support and is widely used in both small-scale and enterprise-level applications for data storage and retrieval.

sqlalchemy: SQLAlchemy is a popular Python library used for Object-Relational Mapping (ORM) and database abstraction. It provides a set of tools and an interface for developers to interact with relational databases in a Pythonic way, allowing them to work with database tables and records as if they were Python objects. SQLAlchemy supports multiple database systems and offers flexibility and abstraction, making it easier to work with databases in Python applications, from simple scripts to complex web applications.

The application serve following endpoint structure and return the HTTP status codes appropriate to each operation.

Following are the implemented endpoints:

Name Method URL saves PUT /hello/ returns GET /hello/

Query Description:

The query endpoint return all configs that satisfy the query argument.

Query 1:

Description: Saves/updates the given user’s name and date of birth in the database. Request: PUT /hello/ { “dateOfBirth”: “YYYY-MM-DD” } Response: 204 No Content Note: must contain only letters. YYYY-MM-DD must be a date before the today date.

Query 2:

Description: Returns hello birthday message for the given user Request: Get /hello/ Response: 200 OK Response Examples:

A. If username’s birthday is in N days:

{ “message”: “Hello, ! Your birthday is in N day(s)” } B. If username’s birthday is today:

{ “message”: “Hello, ! Happy birthday!” }# happy-birthday-python Python App

dockerizing the app :

Build and run the application with Docker Compose:
-Build the images and spin up the containers:
  >> docker-compose up -d --build
-Build The Docker Image:
  >> docker build -t image name:<version>
-Publish The Docker Image:
1 Tag Your Image:  
 >> docker tag your-image-name:your-tag your-dockerhub-username/your-image-name:your-tag
2 Log in to Docker Hub:
 >> docker login
3 Push Your Image:
  >> docker push your-dockerhub-username/your-image-name:your-tag
4 Wait for the Push to Complete: 
5 erify on Docker Hub: 
