# 3-tier-architecture-using-docker-compose
This repository contains a three-tier architecture web application built using Docker Compose. It includes a web layer, an application layer, and a database layer, all containerized for seamless deployment.

1. What is Docker Compose?
Docker Compose is a tool that allows you to define and manage multi-container Docker applications. It uses a YAML file (docker-compose.yml) to configure the services, networks, and volumes required for your application.

Key Features:
Define multiple services in one file.
Start all containers with a single command.
Automatically handle networking between services.

2. Benefits of Docker Compose :
   
Simplified Configuration: All service configurations in one file.
Environment Isolation: Easily replicate production environments.
Scalability: Scale services up or down with a single command.
Portability: Consistent deployment across different systems.
Efficient Networking: Automatically links services without manual network configuration.

4. Structure of the System
This system follows a three-tier architecture:

a. Web Layer
Handles the user interface and serves static files.

Structure:
web/
├── Dockerfile
├── default.conf
└── myhtmlcode/
    └── index.html


Components:
Dockerfile: Configuration for the web container (e.g., Nginx setup).
default.conf: Custom Nginx configuration.
myhtmlcode/index.html: Static HTML content.

b. Application Layer
Processes business logic.

Structure:
app/
├── Dockerfile
└── myphpcode/
    └── index.php

Components:
Dockerfile: Configuration for the app container (e.g., PHP setup).
myphpcode/index.php: PHP code for the application logic.

c. Database Layer
Stores and manages data.

Structure:
db/
├── Dockerfile
├── init.sh
└── init.sql

Components:
Dockerfile: Configuration for the database container.
init.sh: Initialization script for database setup.
init.sql: SQL file to create tables and seed data.


How to Run :
   
1. Clone the repository:
git clone <repository-url>
cd <repository-folder>

2. Run the Docker Compose file:
   docker-compose up --build

3. Access the application:

Web: http://localhost:<web-port>
App: Communicates with web and database internally.
Database: Internal service for data persistence.

4. Stop and clean up:
 docker-compose down --volumes




