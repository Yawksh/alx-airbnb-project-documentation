# Backend Feature Requirement Specifications

This document outlines the technical and functional requirements for the following key backend features of the Airbnb Clone:

- User Authentication
- Property Management
- Booking System

---

## 1. User Authentication

### 🎯 Functional Requirements:
- Users can register as guests or hosts using email and password.
- Users can log in with email and password.
- Support for third-party authentication (OAuth2: Google, Facebook).
- JWT-based session management.
- Role-based access control (Guest, Host, Admin).

### 🛠 API Endpoints:

| Method | Endpoint             | Description                |
|--------|----------------------|----------------------------|
| POST   | /api/register        | Register a new user        |
| POST   | /api/login           | Log in existing user       |
| GET    | /api/profile         | Get authenticated user data|
| PUT    | /api/profile/update  | Update user profile        |

### 🔁 Input/Output Specs

**POST /api/register**
```json
// Request
{
  "name": "Yawukal",
  "email": "yaw@example.com",
  "password": "12345678",
  "role": "host"
}

// Response
{
  "message": "User registered successfully",
  "token": "JWT_TOKEN"
}
