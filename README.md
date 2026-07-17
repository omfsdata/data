# OMFS Residency site

A minimal three-page static site:

| Page | File | What it is |
|------|------|-----------|
| Map (home) | `index.html` | Interactive D3 map + table of accredited OMFS programs |
| SDN Match Analysis | `analysis.html` | Blog-style write-up of the 2020–2026 match-results analysis |
| About | `about.html` | Placeholder text for you to edit |

Shared styling lives in `site.css`. All figures and the dataset live in `assets/`.
There is no build step — it's plain HTML/CSS/JS.

## Files
```
index.html         # map (loads site.css + inline D3)
analysis.html      # analysis post
about.html         # about (edit the [Filler] text)
site.css           # shared nav + page styles
assets/
  f1_cbse_length.png … f7_funnel.png   # figures embedded in analysis.html
  omfs_all.csv                          # coded dataset (linked for download)
```

## Deploy on GitHub Pages
1. Create a repo and put **all of these files at the repo root** (keep the `assets/` folder).
2. Commit and push.
3. Repo → **Settings → Pages** → *Build and deployment* → Source: **Deploy from a branch**,
   Branch: **main** / **/ (root)** → Save.
4. Your site appears at `https://<username>.github.io/<repo>/` within a minute or two.
   Because the homepage is `index.html`, the map loads by default.

## Custom domain
You already own a domain, so:
1. Create a file named **`CNAME`** (no extension) at the repo root containing just your domain, e.g.
   ```
   www.yourdomain.com
   ```
2. At your DNS registrar, point the domain at GitHub Pages:
   - For `www`: a **CNAME** record → `<username>.github.io`
   - For the apex/root (`yourdomain.com`): four **A** records →
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. Settings → Pages → **Custom domain** → enter your domain → Save, and tick
   **Enforce HTTPS** once the certificate is issued.

All links between pages are relative, so they work the same on `github.io` or your custom domain.

## Editing later
- **About text:** open `about.html`, replace the `[Filler]` paragraphs.
- **Refresh a figure:** drop a new PNG into `assets/` with the same filename.
- **Colors/nav:** everything visual is in `site.css` (`:root` at the top holds the palette).
