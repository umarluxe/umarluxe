# Deployment: Quick steps

## Option A — Full (frontend + backend) on Render
1. Create a new Web Service on Render for the backend: connect your GitHub, point to /backend, set start command `node server.js`, set environment variable OPENAI_API_KEY to your key.
2. Create a Static Site on Render for frontend: point to /frontend, build command `npm run build`, publish directory `dist`. Set the frontend to call backend API URL (or use a proxy).

## Option B — Frontend on Vercel, Backend on Render
1. Push frontend to GitHub and import to Vercel. In Vercel set `REWRITE` or proxy /api to backend domain OR configure frontend to call full backend URL (eg. https://your-backend.onrender.com/api...)
2. Backend as above on Render.

## After deploy
- Verify your domain (buy domain and attach on hosting dashboard)
- Submit sitemap to Google Search Console
- Add social links and privacy/disclaimer pages
