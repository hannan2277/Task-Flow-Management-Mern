# TaskFlow Management App

A simple full-stack task management application built with Express.js and React. The app allows users to add, view, edit, delete, and mark tasks as complete or incomplete.

## Tech Stack

- Frontend: React + Vite
- Backend: Node.js + Express.js
- Database: MongoDB with Mongoose
- Styling: Tailwind CSS

## Project Structure

```bash
Task-Flow-Management-App-Structure/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── .env
│   ├── index.js
│   ├── package.json
│   └── readme.md
├── frontend/
│   ├── src/
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
├── README.md
└── .gitignore
```

## Features

- Add new tasks
- View all tasks
- Fetch single task details by ID
- Update task name and status
- Delete tasks
- Toggle task completion state
- Responsive UI

## Backend API Endpoints

Base URL: `http://localhost:4000/api`

### Get all tasks
- `GET /all-task`

### Get a single task
- `GET /single-task/:id`

### Add a task
- `POST /add-task`
- Body:
  ```json
  {
    "name": "Complete project report"
  }
  ```

### Update a task
- `PUT /update-task/:id`
- Body:
  ```json
  {
    "name": "Updated task title",
    "isComplete": "yes"
  }
  ```

### Delete a task
- `DELETE /delete-task/:id`

## Environment Setup

### Backend
Create a `.env` file inside the `backend` folder:

```env
PORT=4000
MONGO_URL=mongodb://localhost:27017/todo
```

## Installation

### 1. Install backend dependencies

```bash
cd backend
npm install
```

### 2. Install frontend dependencies

```bash
cd frontend
npm install
```

## Run the Application

### Start backend

```bash
cd backend
npm run dev
```

### Start frontend

```bash
cd frontend
npm run dev
```

The frontend will run on Vite's local dev server, typically at:

```bash
http://localhost:5173
```

The backend will run at:

```bash
http://localhost:4000
```

## Notes

- Make sure MongoDB is running locally before starting the backend.
- The task model stores `isComplete` as either `"yes"` or `"no"`.
- This project is intended for learning and basic task-management workflows.

## License

This project is for educational use.
