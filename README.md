# MedQuiz Fullstack Project

This repository contains the fullstack MedQuiz application, including both the backend (Node.js/Express/MongoDB) and frontend (Next.js/React).

## Project Structure

```
MEDQUIZ/
  ├── MedQuizBackEnd/   # Backend API (Node.js, Express, MongoDB)
  └── MDKKUQUIZ/        # Frontend app (Next.js, React)
```

## Features
- User authentication and roles (JWT, NextAuth)
- Quiz, keyword, report, and score management
- Admin and S-admin dashboards
- RESTful API endpoints
- Modern, responsive frontend

## Prerequisites
- Node.js 18+
- MongoDB (running locally on your machine or VM)
- Docker & Docker Compose (for containerized setup)

---

## Backend Setup (`MedQuizBackEnd`)

1. **Install dependencies:**
   ```sh
   cd MedQuizBackEnd
   npm install
   ```
2. **Create a `.env` file:**
   See below for required variables.
3. **Start MongoDB locally** (default port 27017).
4. **Run the backend server:**
   ```sh
   npm start
   ```
   The server will run on `http://localhost:5000` by default.

### Environment Variables Example (`MedQuizBackEnd/.env`)
```
MONGO_URI=mongodb://localhost:27017/medquiz
JWT_SECRET=your_jwt_secret
JWT_COOKIE_EXPIRE=30
NODE_ENV=development
PORT=5000
```

---

## Frontend Setup (`MDKKUQUIZ`)

1. **Install dependencies:**
   ```sh
   cd MDKKUQUIZ
   npm install
   ```
2. **Configure backend API URL:**
   - Edit `src/config/apiRoutes.ts` if your backend runs on a different host/port.
3. **Run the frontend app:**
   ```sh
   npm run dev
   ```
   The app will run on `http://localhost:3000` by default.

---

## Docker & Docker Compose

You can run both backend and frontend using Docker Compose:

1. **Build and start all services:**
   ```sh
   docker-compose up --build
   ```
2. **Access the apps:**
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend API: [http://localhost:5000](http://localhost:5000)

> **Note:** MongoDB is not included as a Docker service. You must run MongoDB locally on your machine or VM.

### MongoDB Connection
- **On Mac/Windows:** Use `mongodb://host.docker.internal:27017/medquiz` in your backend `.env`.
- **On Linux:** Use `mongodb://localhost:27017/medquiz` and set `network_mode: "host"` for the backend in `docker-compose.yml`.

---

## Folder Details
- **MedQuizBackEnd/**: Backend API, see `MedQuizBackEnd/README.md` for more details.
- **MDKKUQUIZ/**: Frontend app, see `MDKKUQUIZ/README.md` (if available) for more details.

---

## License
This project is for educational and internal use. See individual files for more details. 
