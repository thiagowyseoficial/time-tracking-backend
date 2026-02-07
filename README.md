# ⏱️ Time Tracking Backend

A RESTful API for **time tracking and work hour management**, designed for teams, freelancers, and companies that need accurate control over worked hours, projects, and productivity.

This project was built with a **backend-first mindset**, focusing on **clean architecture, strong business rules, and database modeling**.

---

## 🚀 Features

### Authentication & Security
- User registration and login
- JWT-based authentication
- Role-based access control (ADMIN / USER)
- Secure password hashing

### Time Tracking
- Start, pause, and stop timers
- Manual time entries
- Validation to prevent overlapping time records
- Automatic duration calculation

### Project & Task Management
- Create and manage projects
- Assign users to projects
- Create tasks within projects
- Project status control (ACTIVE / ARCHIVED)

### Reports
- Total worked hours by:
  - User
  - Project
  - Date range
- Daily and monthly summaries
- Ready for export integration (CSV / PDF)

---

## 🛠️ Tech Stack

- **Java 17**
- **Spring Boot**
- Spring Web
- Spring Data JPA
- Spring Security + JWT
- **PostgreSQL**
- Flyway (database migrations)
- Docker & Docker Compose
- Swagger / OpenAPI
- JUnit & Mockito (tests)

---

## 🧱 Architecture

The project follows a **layered architecture**, separating responsibilities clearly:

