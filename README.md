
# 📚 Library Management System

A RESTful Library Management System built with **Java**, **Spring Boot**, and a **relational database**. This project is submitted as part of the CODE81 technical assessment.

---

## 📌 Features

- 📖 Book management with rich metadata (multi-author, publisher, genre hierarchy, etc.)
- 👥 Member management
- 🔐 System user management with **role-based access control**
  - Roles: `Administrator`, `Librarian`, `Staff`
- 🔄 Borrowing and returning transactions
- 🔒 Secure authentication and authorization
- 🧾 User activity logging
- 🧰 RESTful API for all entities

---

## 🧱 Tech Stack

- Java 17+
- Spring Boot
- Spring Security
- Spring Data JPA
- PostgreSQL (or MySQL)
- H2 for testing
- Maven
- Lombok
- Swagger / Postman (optional)

---

## 🗃️ Database Schema

The system contains the following main entities:

- `Book`: title, ISBN, edition, summary, language, cover image, etc.
- `Author`: supports many-to-many with books
- `Publisher`
- `Category`: supports hierarchical relationships
- `Member`: represents a borrower
- `User`: login account (Administrator, Librarian, Staff)
- `BorrowTransaction`: tracks borrow/return operations

📎 See `ERD.png` for full schema visualization.

---

## 🔐 Authentication & Authorization

- Basic Authentication with hashed passwords (BCrypt)
- Role-based access:
  - `ADMIN`: Full access to all endpoints
  - `LIBRARIAN`: Can manage books and borrowing
  - `STAFF`: Limited access
- Protected API routes with Spring Security

---

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/library-management-system.git
   cd library-management-system
   ```

2. Configure DB in `application.properties`

3. Build and run:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

4. Access API:
   ```
   http://localhost:8080/api/
   ```

---

## 📦 API Endpoints

> All routes are prefixed with `/api`

| Resource       | Endpoint Example                   | Description                  |
|----------------|------------------------------------|------------------------------|
| Books          | `GET /books`, `POST /books`        | CRUD operations for books    |
| Members        | `GET /members`, `POST /members`    | CRUD operations for members  |
| Users          | `GET /users`, `POST /users`        | User account management      |
| Borrowing      | `POST /borrow`, `POST /return`     | Manage borrow/return         |

📬 Postman Collection is included in `postman_collection.json`

---

## 🧪 Sample Data

Use the SQL script `sample_data.sql` to populate the database with dummy records.

---

## ✅ Notes

- Task duration: **4 days**
- Built for CODE81 technical assessment
- Focused on clean architecture and modular design

---

## 👨‍💻 Author

kerolles sobhy  
[LinkedIn](#) | [GitHub](#)
