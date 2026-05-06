 # User API - REST API with PostgreSQL

A REST API built with Node.js and Express.js connected to a PostgreSQL database. Supports full CRUD operations on user data.

## Tech Stack
- Node.js
- Express.js
- PostgreSQL
- Postman (for testing)

## Prerequisites
- Node.js installed
- PostgreSQL installed and running

## Getting Started

### 1. Clone the repository
git clone https://github.com/yourusername/user-api.git
cd user-api

### 2. Install dependencies
npm install

### 3. Set up PostgreSQL
Connect to PostgreSQL and run:
CREATE DATABASE userdb;
\c userdb
CREATE TABLE users (id SERIAL PRIMARY KEY, name VARCHAR(100) NOT NULL, email VARCHAR(100) UNIQUE NOT NULL, age INT NOT NULL);

### 4. Configure environment variables
Create a .env file in the root folder:
DB_USER=postgres
DB_HOST=localhost
DB_NAME=userdb
DB_PASSWORD=your_password_here
DB_PORT=5432

### 5. Start the server
node index.js

Server will run on http://localhost:3000

## API Endpoints

| Method | Endpoint | Description |
|--------|------------|---------------------|
| GET | /users | Get all users |
| GET | /users/:id | Get a single user |
| POST | /users | Create a new user |
| PUT | /users/:id | Update a user |
| DELETE | /users/:id | Delete a user |

## Example Request (POST /users)
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25
}

## Example Response
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25
}
