# Salon Management API

A simple REST API for managing salons, salon services, and user authentication.

## Tech Used

* Node.js
* Express.js
* Supabase
* JWT
* bcryptjs
* dotenv

## Features

* User registration and login
* Password hashing using bcrypt
* JWT authentication
* Salon CRUD operations
* Service CRUD operations
* Top 5 salons by rating
* Search salons by city
* Available services filter
* Request logging
* Input validation

## API Routes

### Authentication

* `POST /register`
* `POST /login`

### Salons

* `GET /salons`
* `GET /salons/:id`
* `POST /salons`
* `PUT /salons/:id`
* `DELETE /salons/:id`
* `GET /salons/top`
* `GET /salons/city/:city`

### Services

* `GET /salons/:id/services`
* `POST /salons/:id/services`
* `PUT /services/:id`
* `DELETE /services/:id`
* `GET /services/available`

JWT is required for protected POST, PUT and DELETE routes.

## Database

Supabase is used with three tables:

* `users`
* `salons`
* `services`

Services are connected to salons using `salonId`.

## Run Locally

```bash
npm install
npm run dev
```

Create a `.env` file with:

```env
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
JWT_SECRET=your_jwt_secret
PORT=5001
```

## Live API

https://salon-management-api-3qjs.onrender.com

## Author

Aditya Yadav
