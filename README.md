# Infinity Gamers Admin: Frontend (Vercel)

Static site. No build step, no server. Backend lives in its own repo on Render.

## Deploy on Vercel
1. Push this `frontend/` folder as its own repo (or keep it in a monorepo and set Root Directory = `frontend`).
2. Vercel -> Add New -> Project -> import the repo.
3. Framework Preset: **Other**. Build Command: empty. Output Directory: empty (root).
4. Deploy.

## Backend URL
Edit `config.js` -> `window.INFINITY_API_URL`.

## Required on the Render backend
Allow your Vercel domain in CORS, e.g. in the Express backend:
    cors({ origin: ["https://YOUR-APP.vercel.app"] })
Keep Authorization header and GET/POST/PUT/PATCH/DELETE allowed.
