# Backend

Documentation on any Backend capabilities or changes made.

## [Feature] Order API Endpoint – Implementation Summary

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

## Utility Functions Architecture

1. Introduced a structured utility system for reusable logic:
   src/utils/orders/
   src/utils/products/

2. Reusable, Typed Functions
   Each module contains reusable utility functions — such as input validation, data formatting, and helpers — scoped by feature. This makes logic composable and maintainable.
