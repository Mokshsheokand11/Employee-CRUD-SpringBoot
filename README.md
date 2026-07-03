# Employee Management CRUD Application

A simple **Employee Management System** built using **Java Spring Boot**, **Maven**, **Spring Data JPA**, **Hibernate**, and **MySQL**. This project performs CRUD (Create, Read, Update, Delete) operations through REST APIs. No frontend is used; all APIs are tested using **Postman**.

## Technologies Used
- Java 21
- Spring Boot 3
- Maven
- Spring Data JPA
- Hibernate ORM
- MySQL 8
- Postman
- IntelliJ IDEA

## Project Structure

```
src
└── main
    ├── java
    │   └── com.example.demo
    │       ├── controller
    │       ├── entity
    │       ├── repository
    │       ├── service
    │       └── DemoApplication.java
    └── resources
        └── application.properties
```

## Project Flow

```
Postman
   │
   ▼
EmployeeController
   │
   ▼
EmployeeService
   │
   ▼
EmployeeRepository
   │
   ▼
MySQL Database
```

## How It Works

1. User sends an API request using **Postman**.
2. The request reaches **EmployeeController**.
3. Controller calls **EmployeeService**.
4. Service communicates with **EmployeeRepository**.
5. Repository performs database operations using **Spring Data JPA**.
6. The response is returned back to Postman.

## Database

**Database:** `employee_db`

**Table:** `employees`

| Column | Type |
|---------|------|
| id | BIGINT (Primary Key, Auto Increment) |
| name | VARCHAR |
| department | VARCHAR |
| salary | DOUBLE |

## REST APIs

### Get All Employees
```
GET http://localhost:8080/employees
```

### Get Employee by ID
```
GET http://localhost:8080/employees/{id}
```

### Add Employee
```
POST http://localhost:8080/employees
```

```json
{
  "name":"Rahul",
  "department":"IT",
  "salary":50000
}
```

### Update Employee
```
PUT http://localhost:8080/employees/{id}
```

```json
{
  "name":"Rahul Sharma",
  "department":"Development",
  "salary":65000
}
```

### Delete Employee
```
DELETE http://localhost:8080/employees/{id}
```

## Running the Project

Clone the repository:

```bash
git clone <repository-url>
```

Configure MySQL in `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Build the project:

```bash
mvn clean install
```

Run the application:

```bash
mvn spring-boot:run
```

Test APIs in Postman using:

```
http://localhost:8080/employees
```

## Why Postman?

The focus of this project is backend development. Instead of building a frontend, Postman is used to test REST APIs directly. This makes it easier to verify CRUD operations and database connectivity before integrating any frontend framework like Angular or React.

## Features

- Employee CRUD Operations
- RESTful APIs
- Spring Boot Backend
- MySQL Integration
- Spring Data JPA
- Hibernate ORM
- Layered Architecture
- API Testing with Postman

## Future Improvements

- Angular Frontend
- User Authentication
- JWT Security
- Search & Filter
- Pagination
- Validation
- Exception Handling
- Swagger Documentation

## Learning Outcomes

- Spring Boot Project Structure
- REST API Development
- Maven Build Tool
- Spring Data JPA & Hibernate
- MySQL Integration
- CRUD Operations
- Layered Architecture
- Postman API Testing
- Git & GitHub Version Control

