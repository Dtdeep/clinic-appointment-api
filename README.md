# Clinic Appointment API

This project is a simple Clinic Appointment API built using FastAPI and Docker.

## Laboratory Context

This project was developed in an offline Windows 11 laboratory environment.

Python was not installed directly on the computer. The application was executed using Docker and a
prebuilt Docker image named clinic-fastapi-base:1.0.

## Features

- Create clinic appointments

- View all appointments

- View one appointment

- Update appointment details

- Cancel appointments

## Authentication

This API uses a simple token-based authentication system for testing purposes.

### Test Account

- **Username:** admin
- **Password:** clinic123

### How to Log In

1. Go to `http://localhost:8000/docs` (Swagger UI)
2. Find the `POST /login` endpoint
3. Click "Try it out"
4. Enter the username and password from above
5. Click "Execute"
6. You will receive a token: `clinic-secret-token`

### Protected Endpoints

Once logged in, you can use these endpoints:

- `GET /appointments` - View all appointments
- `GET /appointments/{appointment_id}` - View one appointment
- `POST /appointments` - Create a new appointment
- `PUT /appointments/{appointment_id}` - Update an appointment
- `DELETE /appointments/{appointment_id}` - Cancel an appointment
- `GET /me` - View your user information

### Using the Token in Swagger

1. Click the green **"Authorize"** button at the top
2. Enter the token: `clinic-secret-token`
3. Click "Authorize" then "Close"
4. Now you can test any protected endpoint

### Important Note

This authentication system is **for learning only**. In a real application, you should:

- Never put passwords in code
- Use real database for storing tokens
- Use industry-standard security methods like JWT or OAuth
- Always protect sensitive data

## Technologies Used

- Python

- FastAPI

- Docker

- Git

## How to Run

docker compose up -- build
