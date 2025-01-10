# Three-Tier Notes-App Using Docker

## Project Overview
This is a scalable, containerized web application following the **three-tier architecture** (frontend, backend, and database). The application allows users to create and manage notes and is built using:

- **Nginx** as the reverse proxy (frontend)
- **Django** for the application logic (backend)
- **MySQL** for persistent data storage (database)

The application is containerized using **Docker** and orchestrated with **Docker Compose** to ensure isolated environments, easy deployment, and seamless integration between the components. The architecture supports scalability and reliability with features such as health checks and environment variables.

## Technologies Used
- **Nginx**: Reverse proxy and load balancer for the frontend.
- **Django**: Backend application handling the business logic.
- **MySQL**: Relational database for storing persistent data.
- **Docker**: For containerization of the services.
- **Docker Compose**: To manage multi-container Docker applications.

## Features
- Scalable containerized setup using **Docker**.
- Orchestrated with **Docker Compose** for managing multiple services.
- Health checks to ensure all services are up and running.
- Environment variable support for sensitive configurations.
- Auto-scaling capabilities for high availability.

## Getting Started

### 1. Build and Run the Application

Use Docker Compose to build and start the services.
```bash
docker-compose up --build
```

#### This command will:

- Build the Docker images for Nginx, Django, and MySQL.
- Start the containers and link them via a custom network.

### 2. Access the Application

Once all services are up, you can access the application in your browser:

- Nginx (Reverse Proxy): http://localhost
- Django Admin (Backend): http://localhost/admin
- MySQL (Database): Runs in the background and is accessible within the app.

### 3. Stop the Application

To stop and remove the containers:
```bash
docker-compose down
```
### Health Checks
Health checks are configured to ensure that the services are up and running:

- Django: Health check to ensure the web application is responsive.
- MySQL: Health check to ensure the database is ready to accept connections
