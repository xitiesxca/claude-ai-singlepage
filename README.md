# Xities.com

Static site for Xities (by XCA Ltd), hosted on Vercel from this GitHub repository.
No build step: Vercel serves the files as they are.

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | The whole home page: layout, styles, and the `CONFIG` / `BANNER` / `VIBE_PHOTOS` blocks for quick edits |
| `assets/img/` | All photos (hero, fleet, destinations, experience tiles, closing photos) |
| `assets/fonts/` | Licensed web fonts: Geomatik, HEROES, ASFALLT Sans, Benzin, Denim |
| `404.html` | Page shown for any address that doesn't exist |
| `favicon.svg` | Browser tab icon |
| `robots.txt`, `sitemap.xml` | For search engines |
| `vercel.json` | Clean URLs, caching for images and fonts, security headers |

## Quick edits

- **Text, timing, prices in the banner:** search `index.html` for `CONFIG`, `BANNER` or `VIBE_PHOTOS`.
- **Swap a photo:** upload a new file with the **same name** into `assets/img/` (replace the old one). Images are cached for up to a week in returning visitors' browsers; to show a new photo immediately, give it a new file name and update that name in `index.html`.
- **Online booking:** in `CONFIG`, set `apiBase` to the backend URL and `bookByPhone` to `false` when the backend is ready.

## Publish

Every commit to the `main` branch deploys to production automatically. Other branches get a preview link.

First-time setup in Vercel: **Add New → Project → import this repo**, Framework Preset **Other**, leave Build Command and Output Directory empty, **Deploy**. Then add `xities.com` and `www.xities.com` under **Settings → Domains** and update DNS as Vercel shows.
