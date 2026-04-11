# StreamVault — VidSrc Streaming Site

A free movie & TV streaming site powered by **VidSrc.to** API, deployable on **Cloudflare Pages**.

---

## 🚀 Deploy to Cloudflare Pages (Free)

### Option A — Direct Upload (Easiest)
1. Go to [https://pages.cloudflare.com](https://pages.cloudflare.com)
2. Click **"Create a project"** → **"Direct Upload"**
3. Upload the 3 files: `index.html`, `_headers`, `_redirects`
4. Click **Deploy** — you'll get a free `.pages.dev` URL instantly!

### Option B — GitHub (Auto-deploys on every push)
1. Push these files to a GitHub repo
2. Go to Cloudflare Pages → **"Connect to Git"**
3. Select your repo, leave Build command blank, set Output dir to `/`
4. Click **Save and Deploy**

---

## ⚙️ Optional: Add TMDB API Key (for Search + Posters)

1. Sign up free at [https://www.themoviedb.org/settings/api](https://www.themoviedb.org/settings/api)
2. Open `index.html`, find line:
   ```js
   const TMDB_KEY = ''; // Optional
   ```
3. Paste your key:
   ```js
   const TMDB_KEY = 'your_api_key_here';
   ```

Without a TMDB key the site still works — it fetches posters directly from VidSrc when available.

---

## 📡 VidSrc API Endpoints Used

| Endpoint | Description |
|---|---|
| `vidsrc.to/vapi/movie/new` | Latest new movies |
| `vidsrc.to/vapi/movie/add` | Recently added movies |
| `vidsrc.to/vapi/tv/new` | Latest new TV shows |
| `vidsrc.to/vapi/tv/add` | Recently added TV shows |
| `vidsrc.to/embed/movie/{imdb_id}` | Movie player embed |
| `vidsrc.to/embed/tv/{imdb_id}/{season}/{ep}` | TV episode player embed |

---

## ✨ Features
- 🎬 Movies & TV Shows from VidSrc.to
- 🔍 TMDB-powered search (with API key)
- 📺 Inline iframe player with season/episode selector
- 🌑 Cinematic dark UI — mobile responsive
- ⚡ Zero backend — pure static files, no server needed
- 🟠 Cloudflare Pages ready (free tier)
