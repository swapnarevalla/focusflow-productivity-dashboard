# FocusFlow — Personal Productivity Dashboard

FocusFlow is a small full-stack productivity app built with React and Node.js/Express. Users can manage tasks, filter by status, view a live productivity summary, and run a 25-minute focus timer. The API stores tasks in a local JSON file.

## Tech stack
- React + Vite: interactive frontend
- Node.js + Express: REST API backend
- JSON file: simple local task persistence
- CSS: responsive dashboard UI

## Requirements
Install Node.js (LTS) and npm.

## Run locally
Open two terminals from the project root.

Terminal 1 — backend:
```bash
cd server
npm install
npm run dev
```
Backend runs at http://localhost:5000.

Terminal 2 — frontend:
```bash
cd client
npm install
npm run dev
```
Open the local URL printed by Vite, usually http://localhost:5173.

## API endpoints
- `GET /api/health` — check API status
- `GET /api/tasks` — list tasks
- `POST /api/tasks` — add a task (`{ "title": "Learn React", "priority": "High" }`)
- `PATCH /api/tasks/:id` — update completion (`{ "completed": true }`)
- `DELETE /api/tasks/:id` — delete a task
- `GET /api/summary` — productivity counts
- `POST /api/focus-sessions` — record a completed focus session

## Notes
Tasks are saved in `server/data/tasks.json`, so task changes survive a backend restart. Focus-session count is held in backend memory and resets when the backend restarts. This is a learning/demo project, not a production system.

## GitHub upload
Create a new empty repository on GitHub, then run these commands from the project root:
```bash
git init
git add .
git commit -m "Build FocusFlow full-stack productivity dashboard"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```
Replace `YOUR_GITHUB_REPOSITORY_URL` with the URL of your own repository.
