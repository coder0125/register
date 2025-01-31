# Registration Web Application

A simple web application for managing registrations using Java Servlets, JDBC, 
and MySQL. The application allows users to create, read, update, and delete registration 
records in a MySQL database.

## Features

- **Create**: Add new registration entries.
- **Read**: View all registrations.
- **Update**: Modify existing registration details.
- **Delete**: Remove a registration from the database.

## Technologies Used

- **Java**: The primary language used for backend logic and servlets.
- **Servlets**: Used for handling HTTP requests and responses.
- **JDBC**: For database interaction.
- **MySQL**: The database management system used to store registration data.
- **Apache Tomcat**: The servlet container used for running the application.

## Prerequisites

Before running the application, ensure you have the following installed:

- **JDK 8+** (Java Development Kit)
- **Apache Tomcat 10.1** or later
- **MySQL Server** (with the appropriate JDBC driver)
- **Eclipse IDE** (or any other IDE that supports Java web development)
  
## Setup

### 1.  Set up MySQL Database


  To run this project, you will need to set up a MySQL database.
  Follow the steps below to create the database and the necessary table.

1. **Create the Database:**

   Run the following SQL query to create the database:

   sql
   CREATE DATABASE registrationdb;


USE registrationdb;

CREATE TABLE Registration (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL,
    Email VARCHAR(150) NOT NULL UNIQUE,
    DateOfBirth DATE NOT NULL,
    PhoneNumber VARCHAR(15),
    Address VARCHAR(255)
);

### 2. Configure Database Connection

** In the RegistrationDAO.java file, configure the database connection URL, username, and password:
      code--
                   private static final String JDBC_URL = "jdbc:mysql://localhost:3306/registrationdb";
                   private static final String JDBC_USER = "root";
                   private static final String JDBC_PASSWORD = "Indar@28929";
    

### 3. Build and Run the Project

**Build the project: Right-click on the project > Build Project.
   Deploy to Tomcat both (deploy in server and run the program in console)
       Right-click the project > Run As > Java Application on the console.



### 4. If using HTML PAGE: deploy in a server using Apache Tomcat

code --

     <!DOCTYPE html>
     <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Registration System</title>
    </head>
    <body>
          <h1>Registration Form</h1>
          <form action="/register" method="POST"> 
          <label for="name">Name:</label><br>
          <input type="text" id="name" name="name" required><br><br>
          <label for="email">Email:</label><br>
          <input type="email" id="email" name="email" required><br><br>
          <label for="dob">Date of Birth:</label><br>
          <input type="date" id="dob" name="dob" required><br><br>
          <label for="phone">Phone Number:</label><br>
          <input type="text" id="phone" name="phone"><br><br>
          <label for="address">Address:</label><br>
          <textarea id="address" name="address"></textarea><br><br>
         <input type="submit" value="Submit">
    </form>
    </body>
    </html>

     *****************************************************


    **Note**: This project has been developed with both features:
     *****************************************************************
  
1. The ability to **run the project on a server** (using **Spring Boot** , Apache Tomcat).
2. The option to **run the program using a UI front-end page** within **Eclipse**.

Both features are implemented, and you can choose the method that best suits your needs for running the project.

       
     
