Treatment Tracer Project
Project Overview
 Treatment Tracer is a microservices-based application designed to manage and trace medical treatments and related information. It leverages the power of:
•	Spring Boot
•	Spring Cloud
•	Spring Cloud Config
•	Eureka Server (Service Discovery)
•	Spring Cloud Gateway (API Gateway)
•	Kafka (Event Streaming)
•	Docker & Docker Compose (Containerization)
•	MySQL (Database)

 Project Architecture
The project follows a microservices architecture with the following components:
1.	Config Server - Centralized configuration management.
2.	Eureka Server - Service discovery.
3.	API Gateway - Routing and load balancing.
4.	User Profile Service - Manages user profiles.
5.	Auth Service - Handles authentication and JWT token management.
6.	Treatment Service - Tracks and manages treatment details.
7.	Bookmark Service - Allows bookmarking of treatments.
8.	Kafka - Event streaming between services.
9.	MySQL - Relational database management.

Project Setup
    Clone the Repository
    git clone https://github.com/pbhendarkar/treatment-tracer.git
    cd treatment-tracer

Build and Run using Docker Compose
Step 1: Clean and package the services
             mvn clean package -DskipTests
Step 2: Build and start the services
             docker-compose up --build -d
Step 3: Check running containers
            docker ps

Access the Services
Service	Port	URL
Eureka Server	8761	Eureka Dashboard
API Gateway	8080	Gateway
Auth Service	8082	Auth API
User Profile	8081	User API
Treatment	8083	Treatment API
Bookmark	8084	Bookmark API
Config Server	8085	Config Server Health

		
		
		
		
Testing the APIs

🛂 Authentication
Login Endpoint:
POST http://localhost:8080/auth/login

Payload:		
{
  "username": "user",
  "password": "password"
}

User Profile
Get User Profile:
GET http://localhost:8080/users/{userId}		

Treatment Details
Get Treatment:
GET http://localhost:8080/treatments/{treatmentId}

Bookmark Management
Get Bookmarks:
GET http://localhost:8080/bookmarks

Useful Commands
🔍 Check Logs
docker-compose logs -f {service-name}
Stop All Containers		
docker-compose down
Remove All Containers and Images
docker system prune -a		
		

