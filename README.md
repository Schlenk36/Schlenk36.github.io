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

## Redeploy after edits

Replace `USERNAME` with your GitHub username:

```bash
rsync -a --delete --exclude='.git' "<this website folder>/" ~/Sites/USERNAME.github.io/
cd ~/Sites/USERNAME.github.io && git add -A && git commit -m "Update site" && git push
```

GitHub Pages will rebuild within a minute.
