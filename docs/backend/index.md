# Backend

Documentation on any Backend capabilities or changes made.

--------------------------------------------------------------

## 1. [New Feature]: Search products #142 
- Not started (Frontend)

--------------------------------------------------------------

## 2. [New Feature]: Order API Endpoint #139 – [COMPLETED]

### Summary

1. Implemented a RESTful API structure using Next.js App Router by creating route files under: app/api/<module_name>/route.ts

Example for orders:
app/api/orders/route.ts

2. Decoupled Route Handlers
   Each route.ts file acts as a thin HTTP layer that delegates business logic to internal handler functions. This improves modularity and testability.

3. Centralized Order Logic
   Created a dedicated module: src/api/orders/orderAPI.ts

4. This file houses all core CRUD operations for orders:
   createOrder
   getOrderById
   updateOrder
   deleteOrder
   getAllOrders

### Utility Functions Architecture

1. Introduced a structured utility system for reusable logic:
   src/utils/orders/
   src/utils/products/

2. Reusable, Typed Functions
   Each module contains reusable utility functions — such as input validation, data formatting, and helpers — scoped by feature. This makes logic composable and maintainable.

--------------------------------------------------------------

## 3. [New Feature]: User Information Page #101
- Not started (Frontend)

--------------------------------------------------------------

## 4. [New Feature]: Docker local environment #91 [COMPLETED]

### Summary

#### Docker Setup Progress
 - Installed Docker Desktop on the local machine.
 - Verified Docker installation and ensured the engine is running.
 - Created a Dockerfile to containerize the Next.js application using pnpm and Node.js base image.
 - Created a .dockerignore file to exclude unnecessary files and folders (e.g., node_modules, .git, .next) from being copied into the Docker image.
 - Built the Docker image using `docker build .`.
 - Resolved Docker build error by excluding node_modules in .dockerignore.
 - Created a docker-compose.yml to simplify running the local environment with a single command (docker-compose up).
 - Successfully ran the Next.js app inside a Docker container and confirmed it runs at http://localhost:3000.

Command to start the application in docker: `docker-compose up`

--------------------------------------------------------------

## 5. [New Feature]: Filter products #89
 - Not Started

--------------------------------------------------------------

## 6. [New Feature]: Improve product list page using cards. #84
 - Not Started

--------------------------------------------------------------

## 7. [New Feature]: Improve product list page using cards. #84
 - Not Started

--------------------------------------------------------------

## 8. [New Feature]: Enhance CI/CD with Pre-commit Hooks for Linting, Formatting, and Testing #82
 - Working
  
-------------------------------------------------------------