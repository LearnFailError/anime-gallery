# Anime Gallery

React + Vite + Tailwind CSS v4 gallery of anime (Jikan API) with responsive pagination via `react-responsive-pagination`.

## Run locally
```bash
npm install
npm run dev        # http://localhost:5173
npm run build      # verify the production build
```

## Deploy to Vercel
1. Push to GitHub (`dist` and `node_modules` are git-ignored):
   ```bash
   git init && git add . && git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<you>/anime-gallery.git
   git push -u origin main
   ```
2. In Vercel: **Add New → Project → Import Git Repository**, pick the repo.
3. Vercel detects Vite. Confirm: build command `npm run build`, output directory `dist`. Click **Deploy**.
4. Every push to `main` redeploys automatically.

## Notes
- Jikan allows about 3 requests/second; rapid page jumps may show a retry prompt.
- If a cover image is missing or fails, the card falls back to a random image from waifu.pics.
