
# 💼 Job Board REST API Application

This is a Spring Boot-based REST API project built to manage job postings, companies, and their associated reviews. It demonstrates best practices in building a scalable and modular REST API with full CRUD functionality, JPA integration, and Spring Boot Actuator for monitoring.

---

## 🚀 Features

### ✅ Job APIs
- Fetch all jobs
- Fetch a single job by ID
- Create a new job
- Update a job
- Delete a job

### ✅ Company APIs
- Get all companies
- Get a specific company
- Create a new company
- Update company info
- Delete a company
- Define and manage relationships between Companies and Jobs

### ✅ Review APIs
- Add a review to a company
- Get all reviews for a specific company
- Fetch, update, and delete reviews by review ID
- Manage company-review relationships

### ✅ Spring Boot Actuator
- Health check endpoints (`/health`)
- Application info endpoint (`/info`)
- Metrics (`/metrics`)
- Logger and beans inspection
- Graceful shutdown via `/shutdown` endpoint

---

## 🛠️ Technologies Used

- **Spring Boot**
- **Spring Web**
- **Spring Data JPA**
- **H2/In-memory DB**
- **Postman (for testing)**
- **Spring Boot Actuator**
- **Maven**

---

## 🧱 Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com.example.jobapi/
│   │       ├── controller/
│   │       ├── service/
│   │       ├── repository/
│   │       ├── model/
│   │       └── JobApiApplication.java
│   └── resources/
│       ├── application.properties
│       └── data.sql (optional)
```

---

## 📦 Setup & Run

```bash
# Clone the project
git clone https://github.com/2004roshan/Job-Application.git
cd job-api

# Run the application
./mvnw spring-boot:run
```

Visit `http://localhost:8080` to access endpoints.

---

## 📬 API Endpoints Overview

### 🔹 Jobs
| Method | Endpoint           | Description          |
|--------|--------------------|----------------------|
| GET    | `/jobs`            | Get all jobs         |
| GET    | `/jobs/{id}`       | Get job by ID        |
| POST   | `/jobs`            | Create new job       |
| PUT    | `/jobs/{id}`       | Update a job         |
| DELETE | `/jobs/{id}`       | Delete a job         |

### 🔹 Companies
| Method | Endpoint               | Description            |
|--------|------------------------|------------------------|
| GET    | `/companies`           | List all companies     |
| GET    | `/companies/{id}`      | Get company by ID      |
| POST   | `/companies`           | Create a new company   |
| PUT    | `/companies/{id}`      | Update a company       |
| DELETE | `/companies/{id}`      | Delete a company       |

### 🔹 Reviews
| Method | Endpoint                                          | Description                       |
|--------|---------------------------------------------------|-----------------------------------|
| POST   | `/companies/{companyId}/reviews`                  | Add a review                      |
| GET    | `/companies/{companyId}/reviews`                  | Get all reviews for a company     |
| GET    | `/companies/{companyId}/reviews/{reviewId}`       | Get review by ID                  |
| PUT    | `/companies/{companyId}/reviews/{reviewId}`       | Update review by ID               |
| DELETE | `/companies/{companyId}/reviews/{reviewId}`       | Delete review by ID               |

---

## 📊 Actuator Endpoints

Available at: `http://localhost:8080/actuator`

- `/health`
- `/info`
- `/metrics`
- `/beans`
- `/loggers`
- `/shutdown` *(if enabled)*

---

## 🧪 Postman Collection

You can import the provided Postman collection (if any) to test all endpoints easily.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
