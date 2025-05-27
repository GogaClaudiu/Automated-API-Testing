# Automated-API-Testing

This Postman collection is designed to test the functionalities of the public [Reqres.in](https://reqres.in) REST API, which simulates a typical user management system. The collection covers a wide range of endpoints for both user and resource operations and includes automated test scripts.

## 📦 Collection Overview

- **Name:** Reqres API Testing Project
- **Description:** A Postman collection to validate the functionality and reliability of Reqres.in user and resource management endpoints.
- **Total Requests:** 14
- **Test Scripts:** JavaScript (Postman)

---

## ✅ Included Endpoints and Tests

### 👥 Users
| Request Name              | Method | Endpoint                   | Description                                   |
|--------------------------|--------|----------------------------|-----------------------------------------------|
| List Users               | GET    | `/api/users?page=2`        | Fetches paginated user list. Validates page and response time. |
| Single User              | GET    | `/api/users/2`             | Fetches a single existing user.               |
| Single User Not Found    | GET    | `/api/users/23`            | Tests behavior when user is not found.        |
| Create User              | POST   | `/api/users`               | Creates a new user with JSON payload.         |
| Update User              | PUT    | `/api/users/2`             | Fully updates a user with PUT request.        |
| Delete User              | DELETE | `/api/users/2`             | Deletes a specific user.                      |
| Delayed Response         | GET    | `/api/users?delay=3`       | Simulates delayed server response.            |

### 📁 Resources
| Request Name              | Method | Endpoint                   | Description                                   |
|--------------------------|--------|----------------------------|-----------------------------------------------|
| List All Resources       | GET    | `/api/unknown`             | Lists all available resources.                |
| Single Resource          | GET    | `/api/unknown/2`           | Fetches a single known resource.              |
| Resource Not Found       | GET    | `/api/unknown/23`          | Tests behavior when resource is not found.    |

### 🔐 Authentication
| Request Name              | Method | Endpoint                   | Description                                   |
|--------------------------|--------|----------------------------|-----------------------------------------------|
| Register Successful      | POST   | `/api/register`            | Registers a user with email and password.     |
| Register Unsuccessful    | POST   | `/api/register`            | Simulates registration with missing password. |
| Login Successful         | POST   | `/api/login`               | Logs in with valid credentials.               |
| Login Unsuccessful       | POST   | `/api/login`               | Simulates login with missing credentials.     |

---

## 🧪 Automated Tests

- **Global Test:** Ensures response time is below `1000ms`.
- **Custom Test (List Users):**
  - Verifies that the `page` field in the JSON response equals `2`.

---

## 🧷 Headers

Most requests include the following optional header for simulated authentication:
