# Bob Mayer — Personal Site

A static one-page site, styled after the "About Me" reference design.

## What's in here
```
index.html      the page
style.css       all styling
images/         your photos, extracted from the reference PDF
```

## 1. Preview it locally
Just double-click `index.html`, or from a terminal:
```
cd site
python3 -m http.server 8000
```
Then open `http://localhost:8000`.

## 2. Put it on GitHub Pages
1. Create a new repo on GitHub. If you want it at `https://<username>.github.io`, name the repo exactly `<username>.github.io`. Any other name works too — it'll just live at `https://<username>.github.io/<repo-name>`.
2. Push these files to the repo root:
   ```
   git init
   git add .
   git commit -m "Personal site"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source → Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. Give it a minute — your URL will show at the top of that Pages settings screen.

## 3. Make it yours
- **Swap photos**: replace anything in `images/` (keep the same filenames, or update the `src` paths in `index.html`).
- **Edit text**: all copy — name, tagline, career timeline, highlights — lives directly in `index.html`.
- **Colors/fonts**: everything is driven by the CSS variables at the top of `style.css` (`--bg`, `--accent`, `--serif`, etc.) — change those and the whole page updates.
- **Custom domain**: add a `CNAME` file with your domain, or set it under Settings → Pages.

## Notes
- Fonts (Fraunces, IBM Plex Mono, Inter) load from Google Fonts via CDN — no local font files needed, but it does mean the page needs an internet connection to render the intended type (falls back to system serif/sans otherwise).
- The photo grid, circular headshots, globe graphic, and timeline are all pulled straight from your uploaded PDF — swap in higher-res originals any time for a sharper result.
