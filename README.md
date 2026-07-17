# OMFS Residency site

A minimal **Jekyll** site (which GitHub Pages builds for you automatically — no build step on your end).
All the shared HTML lives in one layout, and the content pages are Markdown.

## How it fits together

```
_config.yml              # site settings (title, footer, domain)
_layouts/
  default.html           # THE WRAPPER — <head>, nav bar, footer live here once
_includes/
  figure.html            # reusable figure+caption snippet
index.html               # the map (front matter + the map markup/JS)
analysis.md              # ← edit this in Markdown
about.md                 # ← edit this in Markdown
assets/
  css/site.css           # shared styles (nav, article, palette)
  css/map.css            # map-only styles
  img/f1…f7.png          # figures used by analysis.md
  omfs_all.csv           # dataset (linked for download)
Gemfile, .gitignore      # only for optional local preview
```

**The wrapper.** Every page is rendered inside `_layouts/default.html`, which holds the
`<head>`, the navigation bar, and the footer. A page never repeats that boilerplate — it just
starts with a little front-matter header saying "use the default layout":

```yaml
---
layout: default
title: About
nav: about        # highlights the right nav link (map | analysis | about)
container: page   # gives it the narrow reading column (omit for full-width like the map)
---
```

Change the nav bar, fonts, or footer **once** in `_layouts/default.html` / `assets/css/site.css`
and it updates everywhere.

## Editing content (the Markdown part)

`analysis.md` and `about.md` are plain Markdown — headings with `#`, **bold**, lists, links.
You can edit them straight in GitHub's web editor.

To drop in a figure, use the one-line include (no HTML needed):

```liquid
{% include figure.html num="2" src="f3_cbse_conv.png"
   caption="What this figure shows." %}
```

Add `wide="true"` for a wide two-panel figure. New image? Put the PNG in `assets/img/`
and reference it by filename.

A few spots (the coloured "callout" boxes and the stat tiles) are small raw-HTML blocks inside
the Markdown — they're labelled and you can edit the text inside them freely.

## Deploy on GitHub Pages

1. Put everything in a repo (root level). Commit and push.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch **main** / **/(root)**.
3. GitHub detects Jekyll and builds it automatically. Your site is live in a minute or two.

> Do **not** add a `.nojekyll` file — that would turn the Jekyll build off.

## Custom domain

1. Add a file named **`CNAME`** (no extension) at the repo root containing just your domain:
   ```
   www.yourdomain.com
   ```
2. DNS at your registrar:
   - `www` → **CNAME** record → `<username>.github.io`
   - apex `yourdomain.com` → four **A** records → `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
3. Settings → Pages → set the custom domain and enable **Enforce HTTPS**.

Keep `baseurl: ""` in `_config.yml` for a custom domain. (Only set `baseurl: "/repo-name"`
if you serve from `username.github.io/repo-name/` instead.)

## Optional: preview locally

Not required, but if you want to see changes before pushing:

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```
