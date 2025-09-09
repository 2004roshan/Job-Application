

---

# 💼 Job Application REST API

A Spring Boot-based REST API to manage **Jobs, Companies, and Reviews**, demonstrating best practices in **layered architecture, JPA integration, and application monitoring** with Spring Boot Actuator.

---

## 🚀 Features

### 🔹 Job APIs

* Create, fetch, update, and delete jobs
* Associate jobs with companies

### 🔹 Company APIs

* Manage company details (CRUD)
* Link companies with jobs and reviews

### 🔹 Review APIs

* Add, update, and delete reviews for companies
* Fetch all reviews or a specific review by ID

### 🔹 Monitoring & Observability

* Integrated **Spring Boot Actuator**

  * `/health` → Application health
  * `/info` → App metadata
  * `/metrics` → Runtime metrics
  * `/shutdown` → Graceful shutdown (if enabled)

---

## 🛠️ Tech Stack

* **Spring Boot** (REST API development)
* **Spring Data JPA** (ORM & persistence)
* **H2 Database** (in-memory testing)
* **Spring Boot Actuator** (monitoring & health checks)
* **Postman** (API testing)
* **Maven** (build tool)

---

## 📂 Project Structure

```
src/
 └── main/java/com/job/firstjobapp/
     ├── company/       # Company entity, repository, service, controller
     ├── job/           # Job entity, repository, service, controller
     ├── review/        # Review entity, repository, service, controller
     ├── FirstjobappApplication.java
 └── resources/
     ├── application.properties
```

---

## ⚙️ Setup & Run

```bash
# Clone repository
git clone https://github.com/<your-username>/job-application-rest-api.git
cd job-application-rest-api

# Run application
./mvnw spring-boot:run
```

App will start at: `http://localhost:8080`

---

## 📬 Example API Endpoints

### Jobs

* `GET /jobs` → Get all jobs
* `GET /jobs/{id}` → Get job by ID
* `POST /jobs` → Add new job
* `PUT /jobs/{id}` → Update job
* `DELETE /jobs/{id}` → Delete job

### Companies

* `GET /companies` → Get all companies
* `POST /companies` → Add company
* `PUT /companies/{id}` → Update company
* `DELETE /companies/{id}` → Delete company

### Reviews

* `POST /companies/{companyId}/reviews` → Add review
* `GET /companies/{companyId}/reviews` → Get all reviews for a company
* `PUT /companies/{companyId}/reviews/{reviewId}` → Update review
* `DELETE /companies/{companyId}/reviews/{reviewId}` → Delete review

---

## 📊 Actuator Endpoints

* `/actuator/health`
* `/actuator/info`
* `/actuator/metrics`
* `/actuator/loggers`
* `/actuator/shutdown` (if enabled)

---

## 🧪 Testing

* Import the Postman collection (if included)
* Validate CRUD operations for Jobs, Companies, and Reviews
* Test health and metrics endpoints via `/actuator`

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---
