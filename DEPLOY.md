# Central Bank Watcher — Deployment Guide

## Deploy to Vercel (fastest, free)

### Option A: Vercel CLI (recommended)
```bash
# 1. Install Vercel CLI (one-time)
npm install -g vercel

# 2. From this folder, deploy
cd web-app
vercel

# Follow prompts → your app will be live at https://your-project.vercel.app
```

### Option B: GitHub + Vercel dashboard
1. Push this `web-app/` folder to a GitHub repo
2. Go to [vercel.com](https://vercel.com) → New Project → Import repo
3. Vercel auto-detects Vite — click Deploy
4. Done. Every push to `main` auto-deploys.

---

## Sharing with users

Once deployed, share the URL (e.g. `https://central-bank-watcher.vercel.app`).

Each user will need their own **Anthropic API key** to use the AI analysis feature:
1. Get a key at [console.anthropic.com](https://console.anthropic.com)
2. Click **⚙ SET API KEY** in the top-right of the app
3. Paste the key — it stays in their browser, never on a server

The tracker data (entries) is also stored per-browser in localStorage, so each user has their own private workspace.

---

## Run locally
```bash
npm install
npm run dev
# → http://localhost:5173
```
