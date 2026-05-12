# TubeStats

A YouTube analytics dashboard inspired by Social Blade.

## Deploy to GitHub + Vercel

### Step 1 — Push to GitHub

```bash
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/tubestats.git
git push -u origin main
```

### Step 2 — Deploy to Vercel

**Option A — Vercel dashboard (easiest)**
1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **Add New → Project**
3. Import your `tubestats` repo
4. Leave all defaults → click **Deploy**
5. Done — live URL in ~30 seconds

**Option B — Vercel CLI**
```bash
npm i -g vercel
vercel
```
Follow the prompts. Your site goes live instantly.

---

## Connect Real YouTube Data (optional)

1. Get a free API key at [console.cloud.google.com](https://console.cloud.google.com)
2. Enable **YouTube Data API v3**
3. Replace the `handleSearch()` function in `index.html` with a fetch to:
   ```
   https://www.googleapis.com/youtube/v3/channels?part=statistics,snippet&forHandle=@HANDLE&key=YOUR_KEY
   ```
4. Map the response fields to the stat cards

---

Built with plain HTML, CSS, and Chart.js — no build step needed.
