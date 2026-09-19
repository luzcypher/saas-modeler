# SaaS Pricing & Revenue Modeler

Vanilla HTML app. Host on GitHub Pages so phones can **Install app**.

## Publish on GitHub Pages

1. On GitHub click **New repository**. Name it something like `saas-modeler`. Keep it public if you want a free Pages URL.
2. Upload everything in this folder to the repo root:
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `icons/` (keep the folder)
3. Repo **Settings → Pages**.
4. Source: **Deploy from a branch**.
5. Branch: `main` (or `master`), folder: `/ (root)`. Save.
6. Wait a minute. Open:
   `https://YOUR-USERNAME.github.io/saas-modeler/`

Replace `YOUR-USERNAME` and the repo name.

## Install as an app

Open that https link in Chrome or Samsung Internet.

- Phone: menu → **Install app** / **Add to Home screen**.
- Laptop: install icon in the address bar.

## Updates after people install it

Push a new `index.html` (or other files) to the same repo.

- They do **not** reinstall.
- Next time they open the app **while online**, the service worker fetches the new files.
- Close and reopen once if the old screen is still showing.

If an update seems stuck, bump the `CACHE` string in `sw.js` (for example `saas-model-v2` → `saas-model-v3`) and push that file too.

## Change only the icon later

Replace these two files. Keep the same names and sizes:

- `icons/icon-192.png` (192×192)
- `icons/icon-512.png` (512×512)

Then bump `CACHE` in `sw.js` and push. The tab icon updates quickly. The Home screen / app-drawer icon is cached by Android and can take a while, or need uninstall + install again, to refresh.
