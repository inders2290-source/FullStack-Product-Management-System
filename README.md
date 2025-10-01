# FullStack Product Management System

A **Node.js + Express + MongoDB** application that implements secure authentication and product management APIs.  
This project demonstrates backend and full-stack skills: user auth, protected routes, and CRUD operations.

---

## Features

- User Authentication  
  - Register & login with hashed passwords (bcryptjs)  
  - JWT-based authentication and authorization  

- Product Management  
  - Create, Read, Update, Delete products  
  - Filtering, sorting, and pagination  

- Security  
  - Password hashing with bcryptjs  
  - JWT middleware for protecting routes  
  - Environment variables via dotenv  

---

## Tech Stack

- **Backend:** Node.js, Express  
- **Database:** MongoDB (Mongoose)  
- **Auth:** JWT, bcryptjs  
- **Config:** dotenv  

---

## Project Structure

```bash
FullStack-Product-Management-System/
├── app.js              # Entry point
├── controllers/        # Business logic for users/products
├── lib/                # Helpers (e.g., DB connection)
├── middleware/         # Auth middleware
├── model/              # Mongoose schemas (User, Product)
├── routers/            # Express routers
├── project/            # Project configs/notes
├── .env                # Environment variables (ignored in git)
├── package.json
└── README.md
````

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/inders2290-source/FullStack-Product-Management-System.git
cd FullStack-Product-Management-System
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment

Create a `.env` file in the project root:

```env
MONGO_URI=your-mongodb-uri
SECRET_KEY=your-jwt-secret
```

### 4. Run the app

```bash
npm start
```

The server runs on [http://localhost:3000](http://localhost:3000).

---

## API Endpoints

### Auth

* **POST** `/user/register` → Register new user
* **POST** `/user/login` → Login & receive JWT

Use this header for protected routes:

```
Authorization: Bearer <your-jwt-token>
```

### Products

* **GET** `/products` → List products
* **POST** `/products` → Create product (protected)
* **GET** `/user/products/:id` → Get product by ID
* **PUT** `/user/products/:id` → Update product (protected)
* **DELETE** `/user/products/:id` → Delete product (protected)

---

## Future Improvements

* Add frontend (React/Angular) for UI
* Role-based access (admin vs user)
* Input validation (Joi/Zod)
* Automated testing (Jest, Supertest)
* API documentation with Swagger

---

## Contributing

Contributions are welcome.

1. Fork this repo
2. Create a branch (`feature/your-feature`)
3. Commit your changes
4. Push & open a PR
