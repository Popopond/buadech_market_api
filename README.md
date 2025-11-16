# 💧 Water Stock API

Backend system for managing bottled water stock in packs. Built with **Java Spring Boot + Gradle** and **PostgreSQL**.  

---

## 🛠️ Tech Stack
- Java 17, Spring Boot 3.4, Spring Data JPA  
- PostgreSQL 16, HikariCP, Lombok, Validation API  
- Gradle

---

## ⚡ Features
- Product management: add/update/list water products  
- Stock management: record in/out, view history  
- REST API examples:  
  - `GET /api/water` → list products  
  - `POST /api/water/{id}/add-stock?qty=` → add stock  

---

## 🔧 Setup & Run

1. **Clone project**  
```bash
git clone <repo-url>
cd water-stock-api


2 **Install PostgreSQL & create DB/user**

CREATE DATABASE waterstock;
CREATE USER pond WITH ENCRYPTED PASSWORD 'your_password';
GRANT ALL PRIVILEGES ON DATABASE waterstock TO pond;
Configure application.properties

3. **Configure application.properties**
spring.datasource.url=jdbc:postgresql://localhost:5432/waterstock
spring.datasource.username=pond
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
Run project

4. **Run project**
./gradlew bootRun