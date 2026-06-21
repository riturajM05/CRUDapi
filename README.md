# softNexis Task 1

A full-stack product management application built with a React + Vite frontend and an Express + MongoDB backend. The app supports product listing, creation, editing, and deletion.

## Features

- View all products
- Add new products
- Edit existing products
- Delete products
- Simple validation on product creation and update
- Backend API with Express and Mongoose
- Frontend built with React, React Router, Tailwind CSS, and Axios

## Tech stack

- Frontend
  - React
  - Vite
  - React Router DOM
  - Axios
  - Tailwind CSS
- Backend
  - Node.js
  - Express
  - Mongoose
  - express-validator
  - dotenv
  - CORS

## Repository structure

- `backend/` - Express API server
  - `controllers/` - request handlers
  - `routes/` - API routes
  - `models/` - Mongoose data schemas
  - `middleware/` - request validation
- `frontend/` - React application
  - `src/` - React components, services, and styling

## Prerequisites

- Node.js 18+ / npm
- MongoDB instance or Atlas cluster

## Setup

### Backend

1. Change into the backend folder:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file with your MongoDB connection string:
   ```env
   MONGODB_URI=mongodb://localhost:27017/your_database_name
   ```
4. Start the server:
   ```bash
   npm run server
   ```

The backend listens on `http://localhost:3000` and exposes routes under `/api/products`.

### Frontend

1. Change into the frontend folder:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the frontend dev server:
   ```bash
   npm run dev
   ```

The frontend runs on `http://localhost:5173` by default and communicates with the backend at `http://localhost:3000/api/products`.

## API Endpoints

- `GET /api/products/list` - fetch all products
- `POST /api/products/create` - create a new product
- `PUT /api/products/modify/:_id` - update an existing product
- `DELETE /api/products/remove/:_id` - delete a product

### Product schema

- `name` (string, required)
- `price` (number, required, > 0)
- `inStock` (boolean, default: true)

## Notes

- The backend allows `http://localhost:5173` via CORS.
- Product validation is applied on create and update.
- If using a remote MongoDB Atlas cluster, ensure your network and credentials are configured correctly.

## Troubleshooting

- If the frontend cannot reach the backend, confirm the backend server is running and `MONGODB_URI` is valid.
- Inspect browser console and terminal logs for request failures and validation messages.

## License

This repository does not specify a license.
