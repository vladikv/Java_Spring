# 🛒 E-Commerce Management Platform

> Full-Stack Web Application · 2025

## 📋 Description

Designed and built a production-ready full-stack e-commerce platform from scratch. The system features a RESTful API backend with JWT-based authentication, role-based access control, and automated image processing — paired with a modern React frontend for managing products and categories.

---

## ✨ Key Features

- 🔐 **JWT authentication** with role-based access control (USER / ADMIN) using Spring Security
- 📦 **Full REST API** with CRUD operations for products, categories, users, and images — documented via Swagger UI
- 🖼️ **Automatic image resizing** on upload — generates 5 optimized sizes (150px → 1200px) using Thumbnailator
- 🗃️ **Redux** for global state management with persistent JWT token handling via localStorage
- 📝 **Reusable form components** with Formik + Yup validation — including drag-and-drop image upload
- 🐳 **Dockerized** — containerized with Docker for consistent deployment across environments

---

## 🚀 Getting Started

### Prerequisites
- Java 21
- MariaDB
- Node.js 18+
- Maven

### Backend
```bash
cd _2.WebApp
mvn clean package
java -jar target/spu123.jar
```

### Frontend
```bash
cd my-app
npm install
npm run dev
```

### Or with Docker
```bash
cd _2.WebApp
docker-compose up --build
```

After startup:
- Frontend: http://localhost:5173
- Backend API: http://localhost:8080
- Swagger UI: http://localhost:8080/swagger-ui/index.html

---

## Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=flat&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=flat&logo=hibernate&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat&logo=apachemaven&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=swagger&logoColor=black)

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
![Redux](https://img.shields.io/badge/Redux-593D88?style=flat&logo=redux&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat&logo=axios&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)

### Tools
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ_IDEA-000000?style=flat&logo=intellijidea&logoColor=white)

---

## Project Structure

```
Java_Spring/
├── _2.WebApp/          # Spring Boot backend
│   ├── src/main/java/org/example/
│   │   ├── controllers/    # REST controllers
│   │   ├── entities/       # JPA entities
│   │   ├── services/       # Business logic
│   │   ├── repositories/   # JPA repositories
│   │   └── security/       # JWT & Spring Security
│   ├── Dockerfile
│   └── docker-compose.yml
│
└── my-app/             # React frontend
    ├── src/
    │   ├── components/ # UI components
    │   ├── store/      # Redux store
    │   ├── entities/   # TypeScript types
    │   └── env/        # Environment variables
    └── package.json
```

---

## API Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| POST | `/api/account/register` | Register new user | No |
| POST | `/api/account/login` | Login, returns JWT | No |
| GET | `/api/categories` | Get all categories | No |
| POST | `/api/categories` | Create category | Yes |
| PUT | `/api/categories/{id}` | Update category | Yes |
| DELETE | `/api/categories/{id}` | Delete category | Yes |
| GET | `/api/products` | Get all products | No |
| POST | `/api/products` | Create product | Yes |
| PUT | `/api/products/{id}` | Update product | Yes |
| DELETE | `/api/products/{id}` | Delete product | Yes |

> Endpoints marked Yes require `Authorization: Bearer <token>` header
