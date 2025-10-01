# FullStack Product Management System

A minimal full-stack system for managing products with secure user authentication.  
Built using **Node.js**, **Express**, **MongoDB (Mongoose)**, **JWT**, and **bcryptjs**.

---

## Features

- User **registration** and **login** with hashed passwords (bcryptjs).
- **JWT authentication** for session management.
- Middleware to **protect routes** (create, update, delete).
- Product CRUD APIs:
  - Create product
  - List products (with filtering, sorting, pagination)
  - Get product by ID
  - Update product
  - Delete product

---

## Tech Stack

- **Backend:** Node.js, Express  
- **Database:** MongoDB with Mongoose  
- **Authentication:** JWT  
- **Password Hashing:** bcryptjs  
- **Configuration:** dotenv  

---

## Project Structure

FullStack-Product-Management-System/
├── app.js # App entry point
├── controllers/ # Business logic for users and products
├── lib/ # Helper functions (DB connection, etc.)
├── middleware/ # Auth middleware (JWT verification)
├── model/ # Mongoose models (User, Product)
├── routers/ # Express routers
├── project/ # Misc project configs or notes
├── .env # Environment variables (not in repo)
├── .gitignore
├── package.json
└── README.md

---

## Getting Started

### 1. Clone and install

```bash
git clone https://github.com/inders2290-source/FullStack-Product-Management-System.git
cd FullStack-Product-Management-System
npm install
2. Configure environment
Create a .env file in the project root:
MONGO_URI=<your-mongodb-uri>
SECRET_KEY=<your-jwt-secret>
3. Run the server
npm start
The app will start at http://localhost:3000 (or the port defined in your app).
API Reference
Auth Routes
POST /user/register → Register a new user
POST /user/login → Login and receive JWT token
Use this header for protected routes:
Authorization: Bearer <jwt-token>
Product Routes
GET /products → List all products
POST /products → Create product (protected)
GET /user/products/:id → Get product by ID
PUT /user/products/:id → Update product (protected)
DELETE /user/products/:id → Delete product (protected)
Security
Passwords are salted & hashed with bcryptjs.
JWT tokens are signed using a secret from .env.
.env is excluded via .gitignore to keep sensitive data safe.
Future Improvements
Frontend (React/Angular) integration for full UI.
Input validation (e.g., Joi, Zod).
Role-based access control (admin vs user).
Automated tests (unit/integration).
