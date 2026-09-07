# Hospital Management System

A full-stack hospital management application with a React frontend and a Spring Boot backend, featuring JWT-based user authentication.

## Project Structure

This repo contains two independent apps:

```
hospital-frontend-main/   # React + Vite frontend
hospital-backend-main/    # Spring Boot backend
```

## Features

- User signup and login (JWT-based authentication)
- Protected dashboard route after login
- REST API backend with Spring Security
- MySQL-backed user persistence via Spring Data JPA

## Tech Stack

**Frontend**
- React 19, Vite 7
- React Router DOM (routing)
- Axios (API calls)

**Backend**
- Java, Spring Boot 3.4
- Spring Security, JJWT (JSON Web Tokens)
- Spring Data JPA, MySQL
- Maven

## Getting Started

### Backend

```bash
cd hospital-backend-main
./mvnw spring-boot:run
```

Runs on `http://localhost:8080` by default. Update MySQL credentials in `application.properties` before running.

### Frontend

```bash
cd hospital-frontend-main
npm install
npm run dev
```

Runs on `http://localhost:5173` by default (Vite's default dev server port).

## Pages

- **Signup** — create a new account
- **Login** — authenticate and receive a JWT
- **Dashboard** — landing page after successful login

## API Endpoints

| Method | Endpoint        | Description                        |
|--------|-----------------|-------------------------------------|
| POST   | `/auth/signup`  | Register a new user |
| POST   | `/auth/login`   | Authenticate a user |

## Related

The backend here shares its authentication module with [hospital-auth-service](https://github.com/EswarVasireddy/hospital-auth-service) — this repo is the full frontend + backend pairing.
