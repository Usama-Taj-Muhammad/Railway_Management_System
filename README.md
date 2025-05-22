# 🚆 Railway Management System – Microservices with Node.js, Docker & MongoDB

This project is a **Railway Management System** built using **Node.js**, **Express**, **MongoDB**, and **Docker Compose** following a **microservices architecture**. It features isolated services for authentication, user management, train scheduling, and booking.

---

## 📁 Project Structure
railway-management-system/
├── auth-service/ # Handles registration and login
├── user-service/ # Manages user profiles and data
├── train-service/ # Manages train schedules and details
├── booking-service/ # Handles ticket bookings
├── mongo/ # MongoDB data volume
├── docker-compose.yml # Docker config to run all services
└── README.md


---

## ⚙️ Technologies Used

- **Node.js** – Backend runtime
- **Express.js** – REST API framework
- **MongoDB** – NoSQL database
- **Mongoose** – MongoDB ODM
- **JWT** – Authentication tokens
- **Docker** – Containerization
- **Docker Compose** – Orchestration for microservices

---

## 🚀 How to Run the Project

### 1. Prerequisites

Make sure you have the following installed:

- Docker  
- Docker Compose  
- Git (to clone the repository)

### 2. Clone the Repository 

```bash
git clone https://github.com/your-username/railway-management-system.git
cd railway-management-system

### 3. Start All Services with Docker Compose
docker-compose up --build

📡 Microservice APIs Overview
🔐 Auth Service (localhost:5100)
Handles registration and login.

Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login and get token

👤 User Service (localhost:5101)
Handles user management.

Method	Endpoint	Description
GET	/api/users	Get all users
GET	/api/users/:id	Get user by ID
POST	/api/users	Create a new user

🚆 Train Service (localhost:5102)
Handles train information.

Method	Endpoint	Description
GET	/api/trains	Get all trains
POST	/api/trains	Add a new train
GET	/api/trains/:id	Get train by ID

🎟️ Booking Service (localhost:5103)
Handles train ticket bookings.

Method	Endpoint	Description
POST	/api/bookings	Book a train ticket
GET	/api/bookings/user/:userId	Get bookings by user ID
