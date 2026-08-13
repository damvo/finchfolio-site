# FinchFolio — showcase site

Static site, ready for GitHub Pages, built for Pinterest Developer app verification.

## Contents
- `index.html` — showcase page (about, what we make, Pinterest, contact)
- `privacy.html` — privacy policy (covers Pinterest API use, required by Pinterest)
- `terms.html` — terms of use & legal notice
- `404.html` — error page
- `assets/style.css`, `assets/logo.png`, `assets/icon.png`, `assets/og-cover.png`
- `robots.txt`, `sitemap.xml`, `.nojekyll`

All URLs already point to `damvo.github.io/finchfolio` (repo `github.com/damvo/finchfolio`, remote already configured). No placeholder to replace unless you rename the repo or change GitHub username — in that case, search/replace `damvo.github.io/finchfolio` across `index.html`, `privacy.html`, `terms.html`, `robots.txt`, `sitemap.xml`.

Etsy shop (`etsy.com/shop/FinchFolio`), Pinterest (`pinterest.com/finchfolio`) and the contact email are already filled in — double check they're exact before publishing.

## Publish to GitHub Pages

### Option A — web UI (no command line)
1. Go to `github.com/damvo/finchfolio` (already exists as your FinchFolio repo remote).
2. Put this site in a `docs/` folder at the repo root, or in a separate `gh-pages` branch — either works.
3. `Settings` > `Pages`. Under *Source*, choose `Deploy from a branch`, pick the branch and folder that contains this site (`main` / `docs` or `gh-pages` / `/ (root)`). Save.
4. Wait 1–2 min. URL: `https://damvo.github.io/finchfolio-site/`.

### Option B — command line
```bash
cd FinchFolio
mkdir -p docs
cp -r /path/to/this/ff-site/* docs/
cp /path/to/this/ff-site/.nojekyll docs/
git add docs
git commit -m "Add showcase site for Pinterest app verification"
git push origin main
```
Then enable Pages via `Settings > Pages`, source = branch `main`, folder `/docs`.

## Pinterest Developer verification
In your Pinterest app configuration:
- **Company website / App URL**: `https://damvo.github.io/finchfolio-site/`
- **Privacy policy URL**: `https://damvo.github.io/finchfolio-site/privacy.html`
- **Terms URL**: `https://damvo.github.io/finchfolio-site/terms.html`

Make sure the site is live (URL reachable) BEFORE submitting the verification.
