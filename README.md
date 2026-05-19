Warehouse Management System – Microservices Architecture
Overview

The Warehouse Management System is a scalable microservices-based backend application developed using Java and Spring Boot. The project is designed to manage products, inventory, warehouses, customers, orders, and delivery routes through independently deployable services communicating via REST APIs.

The system follows industry-standard microservices architecture principles including centralized API routing, service discovery, JWT-based authentication, inter-service communication, and distributed database management.

Features
JWT-based Authentication and Authorization
API Gateway for centralized routing
Eureka Server for service discovery
Product Management Service
Inventory Management Service
Warehouse Management Service
Customer Management Service
Order Management Service
Role-Based Access Control
Inter-Service Communication using Feign Client
Secure Stateless Authentication
Route Optimization using Dijkstra’s Algorithm
Architecture

The system is divided into the following microservices:

1. Eureka Server
Handles service registration and discovery.
2. API Gateway
Central entry point for all client requests.
Performs JWT token validation and request routing.
3. Auth Service
User registration and login.
JWT token generation and authentication.
4. Product Service
Product CRUD operations.
Product information management.
5. Inventory Service
Inventory tracking and stock management.
Communicates with Product Service using Feign Client.
6. Warehouse Service
Warehouse management operations.
Route management between warehouses.
Implements Dijkstra’s Algorithm to calculate shortest delivery paths.
7. Customer Service
Customer registration and profile management.
Stores customer-related information and order associations.
8. Order Service
Order creation and processing.
Communicates with Inventory, Warehouse, and Customer services.
Technologies Used
Backend
Java
Spring Boot
Spring Security
Spring Cloud Gateway
Spring Data JPA
Hibernate
Spring Web
OpenFeign
Database
MySQL
Security
JWT Authentication
Role-Based Authorization
Microservices
Netflix Eureka
API Gateway
Feign Client
Build Tool
Maven
Security Implementation
Stateless authentication using JWT
Secure API access using Spring Security
API Gateway level token validation
Role-based authorization for protected endpoints
Secure inter-service communication
Inter-Service Communication

Feign Clients are used for communication between microservices. Services communicate through REST APIs registered in Eureka Server without hardcoded URLs.

Example:

Inventory Service communicates with Product Service
Order Service communicates with Inventory, Warehouse, and Customer Services
Route Optimization

The Warehouse Service includes route optimization functionality using Dijkstra’s Algorithm.

Features:

Calculates shortest path between warehouses
Optimizes delivery routes
Reduces transportation distance and delivery time
Project Structure
warehouse-management-system
│
├── eureka-server
├── api-gateway
├── auth-service
├── customer-service
├── product-service
├── inventory-service
├── warehouse-service
└── order-service
API Flow
Client
   ↓
API Gateway
   ↓
Microservices
   ↓
Database

Example:

Client → Gateway → Order Service → Inventory Service → Product Service
Key Highlights
Distributed microservices architecture
Scalable and modular backend design
Enterprise-level security implementation
Centralized API routing and authentication
Optimized warehouse routing using graph algorithms
RESTful API development following best practices
Future Enhancements
Docker and Kubernetes deployment
Kafka-based asynchronous communication
Redis caching
Monitoring with Prometheus and Grafana
CI/CD pipeline integration
Notification and Email services
Author

K Tejesh

Backend Developer | Java | Spring Boot | Microservices | MySQL
