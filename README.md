# AppServer — Connecting To MongooseDB
Lightweight Node.js server providing a REST API for movie shows and bookings.
## Features
- Simple REST endpoints for movies, shows, users, and bookings
- MongoDB (or other DB) connection via `configs/db.js`
- Background/workflow functions in `inngest/index.js`
- Minimal, production-ready entry point: `server.js`
## Prerequisites
- Node.js 18+ and npm
- A running database (MongoDB, Postgres, etc.) configured in environment variables
## Quickstart
1. Install dependencies
```bash
cd server
npm install
```
2. Set environment variables (example)
```bash
PORT=3000
DATABASE_URL=mongodb://localhost:27017/appdb
JWT_SECRET=your_jwt_secret
```
3. Start the server
```bash
npm start
# or
node server.js
```
The API will be available at `http://localhost:3000` (or the value of `PORT`).
## Project Structure

- `server.js` — application entry point
- `configs/db.js` — database connection setup
- `inngest/index.js` — background
- `models/` 
- `package.json` — scripts and dependencies
- `vercel.json` — optional deployment settings

## Environment Variables
- `PORT` — port to run the server on
- `DATABASE_URL` — connection string for your database
- `JWT_SECRET` — secret for signing auth tokens (if used)
Add any other service-specific variables your deployment requires.
## Scripts

- `npm start` — run `node server.js`
- Add test and lint scripts as needed in `package.json`.
## Deployment

The repo includes `vercel.json` for deploying to Vercel (if desired). For other platforms, ensure environment variables and any build steps are configured.

If you want, I can add an API reference, example requests, or a deployment guide next.
