# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---
## Clone Your Project
git clone https://github.com/Adish786/Microservices-Task-Submission.git
cd Microservices-Task-Submission

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```

---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```
2. Once the services are running, use the above endpoints to verify the functionality.

3.  Use Docker Compose to build and start all services: 
  sudo docker-compose up -d --build 
4. Check running containers: 
  sudo docker ps 

4. Access Each Service

Once containers are running, access each service from your browser or via curl:

Service URL Port User Service http://localhost:3000/users 3000 Product Service http://localhost:3001/products 3001 Order 
Service http://localhost:3002/orders 3002 Gateway 
Service http://localhost:3003/api/users 3003

On AWS EC2, replace localhost with your EC2 public IP (e.g., http://13.233.xx.xx:3000/users).

5. To stop and remove all containers: sudo docker-compose down 6:- Troubleshooting Tips

Issue Fix

Cannot connect to Docker daemon Run sudo systemctl start docker Missing script: start Add "scripts": { "start": "node app.js" } in package.json

Connection refused Check Security Group inbound ports (3000–3003)

Containers exit Check sudo docker logs <container_name>

Changes not applied Run sudo docker-compose down && sudo docker-compose up -d --build
