# Task Manager REST API ✅

## Overview

Task Manager REST API is a backend application built with Java and Spring Boot that allows users to create, update, search, filter, and delete tasks.

This project demonstrates REST API design, layered architecture (Controller–Service–Repository), and database integration using Spring Data JPA.

---

## Features

* Create new tasks
* View all tasks
* Get task by ID
* Update task details
* Delete tasks
* Filter tasks by status (TODO, IN_PROGRESS, DONE)
* Search tasks by title
* Automatic timestamp tracking (createdAt, updatedAt)

---

## Tech Stack

* Java 17
* Spring Boot
* Spring Web
* Spring Data JPA
* H2 Database (in-memory)
* Maven

---

## Project Structure

```
task-manager-api/
├── controller/   → Handles API requests
├── service/      → Business logic
├── repository/   → Database access
├── model/        → Data models (Task, TaskStatus)
└── resources/    → Configuration files
```

---

## API Endpoints

| Method | Endpoint                  | Description      |
| ------ | ------------------------- | ---------------- |
| GET    | /api/tasks                | Get all tasks    |
| GET    | /api/tasks/{id}           | Get task by ID   |
| POST   | /api/tasks                | Create new task  |
| PUT    | /api/tasks/{id}           | Update task      |
| DELETE | /api/tasks/{id}           | Delete task      |
| GET    | /api/tasks?status=TODO    | Filter by status |
| GET    | /api/tasks?search=keyword | Search by title  |

---

## Example Request

### Create Task

```
POST /api/tasks
```

Body:

```
{
  "title": "Finish project",
  "description": "Complete Spring Boot API",
  "status": "TODO"
}
```

---

## How to Run

1. Clone the repository

```
git clone https://github.com/YOUR_USERNAME/task-manager-api.git
cd task-manager-api
```

2. Run the application

```
mvn spring-boot:run
```

3. Open in browser

```
http://localhost:8080/api/tasks
```

---

## H2 Database Console

Access database at:

```
http://localhost:8080/h2-console
```

Settings:

```
JDBC URL: jdbc:h2:mem:taskdb
Username: sa
Password: (leave empty)
```

---

## What I Learned

* Building REST APIs using Spring Boot
* Structuring applications with layered architecture
* Using JPA for database operations
* Designing clean API endpoints
* Handling real-world backend logic

---

## Future Improvements

* Add user authentication
* Connect to MySQL/PostgreSQL
* Add pagination and sorting
* Build frontend (React)

---
