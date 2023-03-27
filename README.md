# Spring Boot CRUD Example with Hibernate and H2 Database

This is a simple CRUD (Create, Read, Update, Delete) REST API created using Spring Boot 2.4.3, Hibernate as an ORM and H2 as a database. It provides endpoints to manage a list of users with their first name, last name, and email address.
Prerequisites

To build and run the application, you will need:

    Java 11 or later
    Apache Maven 3.6.0 or later
    An IDE like IntelliJ IDEA or Eclipse (optional)
    Postman or any other tool for testing REST API

Getting Started

To run the application, first, clone the repository:


    git clone https://github.com/sescorcia/crud-example.git



Then, navigate to the project directory:


    cd crud-example

## Building and Running the Application

To build and run the application, execute the following command:


    mvn spring-boot:run

This will start the application on http://localhost:8080.
Testing the API

You can test the API using a REST client tool like Postman or cURL. The following endpoints are available:

    GET /api/users: Retrieve all users.
    GET /api/users/{id}: Retrieve a specific user by ID.
    POST /api/users: Create a new user.
    PUT /api/users/{id}: Update an existing user by ID.
    DELETE /api/users/{id}: Delete a user by ID.

All endpoints expect and return JSON data.

Here is an example of creating a new user using cURL:



    curl -X POST \
        http://localhost:8080/api/users \
        -H 'Content-Type: application/json' \
        -d '{
        "firstName": "John",
        "lastName": "Doe",
        "email": "john.doe@example.com"
        }'

## Configuration

You can modify the application configuration in the src/main/resources/application.properties file. The default configuration uses H2 as an in-memory database and sets Hibernate to create and update the database schema automatically.
Conclusion

In this project, we created a simple CRUD REST API using Spring Boot 2.4.3, Hibernate as an ORM, and H2 as a database. We also demonstrated how to test the API using a REST client tool and provided some basic configuration options.