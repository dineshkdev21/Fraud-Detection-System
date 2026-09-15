# Digital Banking & Fraud Detection System

A **microservices-based digital banking system** built with Java and Spring Boot to simulate secure banking transactions and real-time fraud detection. The project demonstrates **event-driven architecture, distributed transaction management, caching, API security, and asynchronous communication** using modern backend technologies.

## 🚀 Key Features

* Secure user authentication and authorization using **JWT and Role-Based Access Control (RBAC)**
* Account and transaction management through **RESTful APIs**
* Real-time transaction processing using **Apache Kafka**
* Rule-based fraud detection for suspicious transactions
* **Redis** caching for low-latency access to frequently used transaction and risk data
* **Saga Pattern** for managing distributed transactions and implementing compensating actions
* Microservices-based architecture with independently deployable services
* Centralized exception handling, request validation, and structured API responses
* Unit and integration testing using **JUnit 5 and Mockito**
* Containerized services using **Docker**
* Automated build, test, and deployment pipeline using **GitLab CI/CD**
* Maven-based project and dependency management

## 🏗️ Architecture

The system consists of independently deployable services communicating through **REST APIs and Apache Kafka events**.

**Core Services:**

* API Gateway
* Authentication Service
* Account Service
* Transaction Service
* Fraud Detection Service
* Notification Service

### Transaction Flow

```text
Client
  ↓
API Gateway
  ↓
JWT Authentication
  ↓
Transaction Service
  ↓
Kafka → Fraud Detection Service
              ↓
        Fraud Validation
          ↙         ↘
      APPROVED     BLOCKED
         ↓            ↓
    Complete      Compensate
    Transaction   Transaction
```

## 🛠️ Tech Stack

**Backend:** Java, Spring Boot, Spring Data JPA
**Architecture:** Microservices, Event-Driven Architecture, Saga Pattern
**Messaging:** Apache Kafka
**Caching:** Redis
**Database:** SQL
**Security:** JWT, RBAC
**Build:** Maven
**Containerization:** Docker
**CI/CD:** GitLab CI/CD
**Testing:** JUnit 5, Mockito
**API:** RESTful APIs
