# User Management System (Node.js + MySQL + Sequelize)

A full-stack backend system for managing user accounts, including registration, email verification, login/logout, password reset, and role-based access control.

---

##  Features

-  User Registration with Email Verification
-  Login with JWT & Refresh Token support
-  Secure Token Rotation and Revocation
-  Role-Based Authorization (Admin/User)
-  Password Reset via Email
-  API Documentation via Swagger UI
-  Input Validation with Joi
-  Sequelize ORM for MySQL

---

##  Tech Stack

- **Node.js** + **Express**
- **MySQL** + **Sequelize**
- **JWT** + **bcryptjs**
- **Nodemailer** (Ethereal email)
- **Swagger UI** for API documentation
- **Thunder Client / Postman** for testing

---

##  Project Structure


---

## locate the backend folder
```bash
cd backend
```

## ⚙️ Setup Instructions

### 1. Install dependencies

```bash
npm install
npm install express dotenv body-parser cookie-parser cors rootpath
npm install sequelize mysql2
npm install bcryptjs jsonwebtoken express-jwt joi
npm install nodemailer swagger-ui-express yamljs
npm install --save-dev nodemon


Run the app
bash
npm run dev
Visit: http://localhost:4000

🔑 API Endpoints
Method | Endpoint | Description
POST | /accounts/register | Register new user
POST | /accounts/authenticate | Login
POST | /accounts/refresh-token | Refresh JWT
POST | /accounts/revoke-token | Revoke a refresh token
POST | /accounts/verify-email | Verify email with token
POST | /accounts/forgot-password | Request password reset
POST | /accounts/reset-password | Reset password via token
GET | /accounts/ | Admin: View all accounts
GET | /accounts/:id | View account by ID

📚 API Documentation
Visit: http://localhost:4000/api-docs/#/

🧪 Test User Registration
Example JSON body:
{
  "title": "Mr",
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@email.com",
  "password": "Test1234",
  "confirmPassword": "Test1234",
  "acceptTerms": true
}

Email Testing (via Ethereal)
Uses Ethereal email for testing (check console log for preview URL). No real emails are sent.
