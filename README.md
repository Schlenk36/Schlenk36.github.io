# Yuhang Zhang — Portfolio Website

A single-page personal portfolio for a synthetic / organometallic chemistry PhD job search,
presenting research, experience, skills, certifications, and downloadable application documents
(CV, Research Summary, Cover Letter). Static HTML/CSS/JS — no build step.

## Structure

- `index.html` — the entire site (embedded CSS + vanilla JS).
- `assets/` — favicon and certification badge image.
- `docs/` — downloadable PDFs (CV, Research Summary, Cover Letter).
- `.nojekyll` — serve files as-is on GitHub Pages.

## Local preview

Open `index.html` in any browser, or serve the folder:

```bash
cd website && python3 -m http.server 8000
# then visit http://localhost:8000
```

## Editing

The editable source lives here (inside the project). The deployed git repo lives outside
OneDrive to avoid sync conflicts.

## Live site

https://schlenk36.github.io/  (repo: `Schlenk36/Schlenk36.github.io`)

## Redeploy after edits

Edit the files in this `website/` folder, then run:

```bash
rsync -a --delete --exclude='.git' "/Users/yuhangzhang/Library/CloudStorage/OneDrive-Personal/UHResearch/Texsyn_CV/website/" ~/Sites/Schlenk36.github.io/
cd ~/Sites/Schlenk36.github.io && git add -A && git commit -m "Update site" && git push
```

GitHub Pages rebuilds within a minute.
