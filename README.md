# World Clock — GitHub Pages (for Notion embed)

This repo is a minimal wrapper around a CommonNinja World Clock widget.
It publishes a simple `index.html` to GitHub Pages so you can embed the page
inside Notion using **/embed**.

## Quick Start
1. Upload these files to your repo (root).
2. In GitHub: **Settings → Pages**
   - Source: *Deploy from a branch*
   - Branch: `main` (or `master`), Folder: `/ (root)`
   - Save → wait for the green check and public URL.
3. In CommonNinja (the widget project):
   - Go to **Project Settings** (or **Domains / Security**)
   - Add **wehinson.github.io** to Allowed Domains (and your custom domain if you use one).
4. In Notion:
   - Type **/embed**
   - Paste your GitHub Pages URL (`https://<username>.github.io/<repo>/`).
   - Resize the block to taste.

## Why `.nojekyll`?
It disables Jekyll processing so the static file serves exactly as-is.

## Troubleshooting
- Blank widget: domain not allowed in CommonNinja → add `wehinson.github.io`.
- 404 or repo README shows instead of widget: ensure the Pages folder is **root** and file is **index.html**.
- Notion shows “refused to connect”: your host or a browser policy is blocking iframes. GitHub Pages generally works; if not, try Netlify.
