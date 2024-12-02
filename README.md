# 3-tier-architecture-using-docker-compose
This repository contains a three-tier architecture web application built using Docker Compose. It includes a web layer, an application layer, and a database layer, all containerized for seamless deployment.

1. What is Docker Compose?
Docker Compose is a tool that allows you to define and manage multi-container Docker applications. It uses a YAML file (docker-compose.yml) to configure the services, networks, and volumes required for your application.

Key Features:
Define multiple services in one file.
Start all containers with a single command.
Automatically handle networking between services.
2. Benefits of Docker Compose
Simplified Configuration: All service configurations in one file.
Environment Isolation: Easily replicate production environments.
Scalability: Scale services up or down with a single command.
Portability: Consistent deployment across different systems.
Efficient Networking: Automatically links services without manual network configuration.
3. Structure of the System
This system follows a three-tier architecture:

a. Web Layer
Handles the user interface and serves static files.

Structure:
plaintext
Copy code
