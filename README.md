# React Simple App

A minimal React + Vite project, ready to push to GitHub and host on GitHub Pages.

## Run locally

```bash
npm install
npm run dev
```

## Deploy to GitHub Pages (Option A — GitHub Actions, recommended)

1. Create a new repo on GitHub, e.g. `react-simple-app`.
2. In `vite.config.js`, set `base: '/react-simple-app/'` to match your repo name (already set — just rename if your repo has a different name).
3. Push this project:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
4. In your GitHub repo: **Settings → Pages → Source → GitHub Actions**.
5. The included workflow (`.github/workflows/deploy.yml`) will build and deploy automatically on every push to `main`.
6. Your site will be live at `https://<your-username>.github.io/<your-repo>/`.

## Deploy to GitHub Pages (Option B — manual, via gh-pages package)

```bash
npm install
npm run deploy
```

This builds the app and pushes the `dist` folder to a `gh-pages` branch. Then in **Settings → Pages**, set the source branch to `gh-pages`.

## Notes

- If you deploy to a custom domain or a `<username>.github.io` root/user page, change `base` back to `'/'` in `vite.config.js`.
