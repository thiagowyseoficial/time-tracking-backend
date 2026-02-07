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

```
controller → service → repository → database
```

Key principles:
- Clean Code
- SOLID principles
- Business rules handled in the service layer
- Database constraints for data integrity
- DTOs for input/output isolation

---

## 🗂️ Domain Model

Main entities:

- **User**
- **Role**
- **Project**
- **Task**
- **TimeEntry**

Key characteristics:
- Well-defined relationships (OneToMany, ManyToOne)
- Indexes for performance
- Unique and NOT NULL constraints
- Audit fields (`created_at`, `updated_at`)

---

## 📌 API Endpoints (Examples)

### Authentication
```
POST /auth/login
POST /auth/register
```

### Users
```
GET    /users
GET    /users/{id}
PUT    /users/{id}
DELETE /users/{id}
```

### Projects
```
POST   /projects
GET    /projects
PUT    /projects/{id}
ARCHIVE /projects/{id}
```

### Time Entries
```
POST   /time-entries/start
POST   /time-entries/stop
POST   /time-entries/manual
GET    /time-entries/report
```

---

## 📊 Business Rules Examples

- A user cannot have two active timers at the same time
- Time entries cannot overlap
- Only project members can register time
- Archived projects do not accept new time entries

---

## 🐳 Running the Project

### Prerequisites
- Docker
- Docker Compose

### Run
```bash
docker-compose up -d
```

The API will be available at:
```
http://localhost:8080
```

Swagger documentation:
```
http://localhost:8080/swagger-ui.html
```

---

## 🧪 Tests

- Unit tests for services
- Mocked repositories
- Focus on business rules and edge cases

Run tests:
```bash
mvn test
```

---

## 📈 Future Improvements

- Redis cache for reports
- Export reports to CSV/PDF
- Activity audit log
- Rate limiting
- Integration with frontend dashboard

---

## 👨‍💻 Author

**Thiago Wyse**  
Backend Developer  
Specialized in Java, Spring Boot, APIs, and database modeling.

---

## 📄 License

This project is licensed under the MIT License.
