Todo App (NestJS + React + Vite)

📌 Overview
This is a full-stack Todo application built using NestJS for the backend and React (Vite) for the frontend. The project follows a monorepo structure, where both the frontend and backend reside in the same parent directory.

The application supports user authentication and offers two roles:

NORMAL_USER_ROLE – Can manage their own todos.

ADMIN – Has additional privileges to manage users.


🚀 Getting Started

Prerequisites
Ensure you have the following installed before running the project:

Node.js (v20 or above)

NPM (comes with Node.js)


📂 Project Structure:

/todo-app
│── /todo-backend      # NestJS backend
│── /react-app-vite    # React frontend (Vite)
│── README.md



🛠 Backend Setup (NestJS)

1️⃣ Navigate to the backend folder:
cd todo-backend

2️⃣ Install dependencies
npm install

3️⃣ Start the backend in development mode
npm run start:dev

The backend will now be running. Make sure it's running before starting the frontend.


🎨 Frontend Setup (React + Vite)


1️⃣ Navigate to the frontend folder
cd react-app-vite

2️⃣ Install dependencies
npm install

3️⃣ Start the frontend
npm run dev

Once started, the application will be live at:
🔗 http://localhost:4000/


🔑 User Roles & Features

1️⃣ NORMAL_USER_ROLE
A normal user can:
✔ Sign up
✔ Log in
✔ Manage their todos

**Active Todos Tab:**
*Add new todos
*View uncompleted todos
*Mark todos as completed
*Delete todos

**Completed Todos Tab:**
*View completed todos
*Delete completed todos


2️⃣ ADMIN ROLE

An admin user has all functionalities of a normal user, plus:
✔ "USERS" Tab in Navbar

*Admin can view all registered users
*Delete users (a deleted user cannot log in again)

📌 Environment Variables

To properly run the project, ensure you have the required environment variables set up.

For the backend (todo-backend), create a .env file and include:

PORT=YOUR_BACKEND_PORT
DATABASE_URL=YOUR_DATABASE_CONNECTION_STRING
JWT_SECRET=YOUR_SECRET_KEY
etc

For the frontend (react-app-vite), update .env file if needed:
VITE_API_BASE_URL=http://localhost:3000

🔐 Authentication & Logout Mechanism

The application uses JWT (JSON Web Token) for authentication.

When a user logs in, they receive a JWT token, which must be included in requests to access protected routes.

**Logout Mechanism:**
The frontend clears the stored JWT token upon logout, effectively logging out the user.
Since JWTs are stateless, logout is handled by removing the token from the frontend storage (local storage/session storage).

🏗 Technologies Used

Backend: NestJS, TypeScript, Node.js, Express, PostgreSQL, JWT Authentication

Frontend: React, Vite

👨‍💻 Contribution

If you'd like to contribute, feel free to fork the repository and submit a pull request.


