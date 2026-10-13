# Taskora

Taskora is a project management application for planning workspaces, projects, tasks, and team collaboration. The app includes a dashboard, project and task views, team management, and workspace analytics.

## Overview

The project is split into two separate npm apps:

- `client/` — React + Vite frontend
- `server/` — Express API server with Clerk authentication middleware

## Tech stack

- React 19
- Vite
- Tailwind CSS
- Redux Toolkit
- React Router
- Clerk authentication
- Express 5
- Prisma (project dependency present in the server)

## Features

- Dashboard overview for project activity and stats
- Project listing and detail views
- Task detail and tracking screens
- Team management and member collaboration views
- Workspace/project analytics panels
- Clerk-based sign-in flow and protected app layout

## Requirements

- Node.js 20 or newer
- npm
- A Clerk application for authentication

## Getting started

Install dependencies for both apps:

```bash
cd client
npm install
```

```bash
cd server
npm install
```

### Environment variables

Create a `client/.env` file and add your Clerk publishable key:

```env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
```

Create a `server/.env` file with your Clerk credentials:

```env
CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
PORT=5000
```

Keep real credentials private. These files are ignored by Git and should never be committed.

## Running the app

Start the server in one terminal:

```bash
cd server
npm run server
```

Start the client in another terminal:

```bash
cd client
npm run dev
```

The Vite dev server usually runs at `http://localhost:5173`. The server listens on port `5000` by default and currently exposes a health-check route at `/` that returns `Server is running...`.

## Available scripts

### Client scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server |
| `npm run build` | Build the frontend for production |
| `npm run lint` | Run ESLint on the client codebase |
| `npm run preview` | Preview the production build locally |

### Server scripts

| Command | Description |
| --- | --- |
| `npm run server` | Start the API server with Nodemon |
| `npm start` | Start the API server with Node.js |

## Project structure

```text
client/         React frontend
server/         Express backend
README.md       Project overview and setup guide
```

## Current status

The frontend includes a working project-management UI with dashboard, projects, team, and task screens. The server is set up with Express, CORS, Clerk middleware, and environment configuration, but the application API routes are not yet implemented.

