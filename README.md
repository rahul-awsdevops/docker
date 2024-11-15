# Appointment Booking System

This is a simple appointment booking system where users can fill out an appointment form, and the data will be stored in a PostgreSQL database. The project uses Express.js for the backend and PostgreSQL for data storage, running inside Docker containers.

## Features

- Users can submit their appointment details (name, age, email, phone, description).
- Appointment data is stored in a PostgreSQL database running in a Docker container.
- Node.js backend running in a separate Docker container.
- You can access and manage the database via pgAdmin.

## Getting Started

Follow the steps below to get the project up and running locally.

### Prerequisites

- Docker
- Docker Compose (optional)
- Node.js (for the backend)
- postgres

### Steps to Run the Project

#### 1. **Set Up PostgreSQL Docker Container**

To run PostgreSQL in a Docker container:

```bash
docker run --name postgres-container --network app-network -e POSTGRES_USER=admin -e POSTGRES_PASSWORD=password -e POSTGRES_DB=clinic -p 5432:5432 -d postgres
