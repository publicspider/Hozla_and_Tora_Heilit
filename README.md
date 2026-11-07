# Hozla & Tora Heilit

Full-stack web platform built as a team project (5 developers),
using React, Node.js/Express, MongoDB and Docker.

> **My part:** 
-React pages and components, API integration

## Features
- Sign up / sign in with JWT-based authentication
- Role-based access: regular users and admins
- User requests, and a separate admin interface for handling them
- File upload
- Annual information management (admin)
- Run the whole stack with a single Docker Compose command

## Tech stack
| Layer | Technology |
|---|---|
| Frontend | React, Material UI (Material Dashboard 2 React template) |
| Backend | Node.js, Express, Mongoose |
| Database | MongoDB |
| Deployment | Docker, Docker Compose, nginx |

## Architecture

    Browser -> Frontend (React, :3000) -> Backend (Express, :5000) -> MongoDB

All three services run in one Docker network, defined in
`docker-compose.yaml`.

## Run locally
1. Create `Backend/.env` (see `Backend/.env.example`):

        PORT=5000
        DB_URL=mongodb://mongodb:27017/HozlaDB

2. Start everything:

        docker compose up --build

3. Open http://localhost:3000. The API is at http://localhost:5000/HozlaApi.

## Credits
The UI is based on the free Material Dashboard 2 React template by
Creative Tim (MIT license). See `Frontend/LICENSE.md`.
