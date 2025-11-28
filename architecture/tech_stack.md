# 🛠 Technology Stack – Binnacle Backend

This document outlines the full technology stack used in the **Binnacle Backend**, organized by purpose and architectural layer.

---

## 🧱 Core Frameworks

| Technology         | Version     | Purpose                            |
|--------------------|-------------|-------------------------------------|
| **Java**           | 21 (LTS)    | Primary language                    |
| **Spring Boot**    | 3.5.0       | Application framework               |
| **Spring Modulith**| 1.4.0-RC1   | Modular architecture enforcement    |
| **Lombok**         | 1.18.30     | Boilerplate reduction               |
| **Maven**          | 3.8+        | Build and dependency management     |

---

## 🧪 Testing & QA

| Technology               | Version     | Purpose                         |
|--------------------------|-------------|----------------------------------|
| **JUnit 5**              | 5.12.2      | Unit & integration testing       |
| **Spring Security Test** | Built-in    | Role and auth test support       |
| **Spring Modulith Test** | Built-in    | Module boundary verification     |
| **Mockito**              | Latest      | Mocking and isolation testing    |
| **AssertJ**              | 3.25.2      | Fluent assertion library         |
| **Jacoco**               | Latest      | Code coverage reports (optional) |

---

## 🔐 Security

| Technology       | Version   | Purpose                              |
|------------------|-----------|---------------------------------------|
| **Spring Security** | Built-in | AuthN & AuthZ                        |
| **Auth0 Java JWT**  | 4.4.0   | JWT creation and verification         |

---

## ☁️ Cloud & DevOps

| Technology    | Version     | Purpose                                |
|---------------|-------------|-----------------------------------------|
| **AWS SDK v2**| 2.25.28     | AWS service integration                 |
| S3            | —           | File/image storage                      |
| SNS           | —           | Notifications (SMS/Email)              |
| **Flyway**    | Latest      | Database schema migrations              |
| **Docker**    | Optional    | Containerization for deployment         |
| **GitHub Actions** | —     | CI/CD pipeline (tests, builds)          |

---

## 💾 Data Layer

| Technology           | Version     | Purpose                              |
|----------------------|-------------|---------------------------------------|
| **PostgreSQL**       | 42.7.5 (driver) | Relational database                 |
| **Spring Data JPA**  | Built-in    | Repository abstraction over JPA       |
| **Hibernate**        | 6.x         | ORM provider, audit support           |

---

## 📡 API & Documentation

| Technology         | Version     | Purpose                            |
|--------------------|-------------|-------------------------------------|
| **Spring Web**     | Built-in    | RESTful API with controllers        |
| **SpringDoc OpenAPI** | 2.7.0   | Swagger UI and OpenAPI generation   |
| **Jackson**        | Built-in    | JSON serialization/deserialization  |

---

## 🧠 Architecture & Patterns

| Practice                   | Usage Description                            |
|----------------------------|-----------------------------------------------|
| **Hexagonal Architecture** | Clean separation of domain/core/infrastructure |
| **DDD (Domain-Driven Design)** | Entities, Value Objects, Use Cases        |
| **Ports and Adapters**     | Clear input/output boundaries                 |
| **Event-Driven**           | Asynchronous module communication             |
| **Strategy Pattern**       | Pluggable logic for reporting/stats modules   |

---

## 🗂 Modules (Spring Modulith)

Each module follows a **self-contained structure** with explicit dependencies defined using `@ApplicationModule`.

| Module         | Purpose                        |
|----------------|--------------------------------|
| `ronda`        | Patrol rounds and events       |
| `user`         | User and authentication logic  |
| `checkIn`      | Guard presence tracking        |
| `route`        | Patrol route configuration     |
| `urbanization` | Neighborhood and locality data |
| `notification` | SNS-based alerting             |
| `statistics`   | Metrics and reporting          |
| `security`     | JWT and access control         |
| `common`       | Shared logic, exceptions, DTOs |

---

## ✅ Summary

This stack enables:
- Clean architecture (modular, layered)
- Scalable cloud-ready services
- High developer productivity with clear separation of concerns
- Enterprise-grade testing, security, and documentation

🟡 **Optional**: Add badges for Java, Spring Boot, and AWS in the GitHub README.

---

> For any questions or clarifications, please refer to [README.md](../README.md) or contact the author.
