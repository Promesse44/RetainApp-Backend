# Retain API

Backend API for Retain, a personal expense and budget manager.

This repository contains the Node.js/Express backend and PostgreSQL/Prisma data layer. 

## Deployment

The Backend is deployed on Render.
https://retainapp-backend.onrender.com

## Tech Stack

- Node.js
- Express
- Prisma
- PostgreSQL
- JWT authentication

## Repository Structure

- `apps/api` - backend application
- `apps/api/prisma` - Prisma schema, migrations, and seed script

## Local Setup

```bash
npm install
```

Create `apps/api/.env` with your backend environment variables.

Typical values:

- `DATABASE_URL`
- `JWT_SECRET`
- `JWT_REFRESH_SECRET`
- `JWT_EXPIRES_IN`
- `JWT_REFRESH_EXPIRES_IN`
- `CORS_ORIGINS`

## Database Commands

From the repository root:

```bash
npm run db:migrate
npm run db:seed
```

## Run Locally

```bash
npm run dev:api
```

The API runs on `http://localhost:4000` by default.

## API Routes

- `POST /api/auth/register`
- `POST /api/auth/login`
- `POST /api/auth/refresh`
- `GET /api/auth/me`
- `GET /api/expenses`
- `POST /api/expenses`
- `PUT /api/expenses/:id`
- `DELETE /api/expenses/:id`
- `GET /api/expenses/dashboard`
- `GET /api/budgets`
- `GET /api/budgets/:month`
- `PUT /api/budgets/:month`
- `GET /api/categories`
- `GET /api/admin/insights`
- `POST /api/admin/categories`
- `PUT /api/admin/categories/:id`
- `DELETE /api/admin/categories/:id`

## Deploying to Render

- Create a Render project for the backend.
- Add a PostgreSQL database.
- Deploy the API as a Web Service.
- Build command: `npm install && npx prisma generate && npx prisma migrate deploy`
- Start command: `npm start`
- Set `DATABASE_URL`, `JWT_SECRET`, `JWT_REFRESH_SECRET`, and `CORS_ORIGINS` in Render.

## Frontend Repo

The frontend is deployed separately from the `RetainApp-Frontend` repository on Vercel.
