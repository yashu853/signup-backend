# Signup Backend API

## Database Setup

Run these SQL commands to create the database and users table:

```sql
CREATE DATABASE IF NOT EXISTS signup_db;

USE signup_db;

CREATE TABLE IF NOT EXISTS users (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL UNIQUE,
  phone VARCHAR(20) NOT NULL UNIQUE,
  password VARCHAR(255) NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## How to run

1. Set your `.env` file with DB credentials
2. Run `npm install`
3. Run `npm start`
4. Test POST `/api/signup` via Postman with JSON body:

```json
{
  "name": "Your Name",
  "email": "your.email@example.com",
  "phone": "1234567890",
  "password": "yourpassword"
}
```
