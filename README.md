# Alok Deo Singh — Personal Résumé Website

A single-page personal website with two views of the same career data:

- **Timeline mode** (default) — an editorial, year-by-year milestone story modeled on the
  UNC Kenan-Flagler "Our History" page: a vertical spine with year markers, milestone cards,
  and scroll-reveal, running from 1996 → 2026.
- **Résumé mode** — a compact, reverse-chronological structured view.

Built as a single, self-contained `index.html` (HTML + CSS + JS, no build step), so it deploys
to GitHub Pages by simply committing the files. There is **no blog page**.

## Files

```
index.html                          The whole site (markup, styles, script, data)
assets/Alok-Deo-Singh-Resume.docx   Downloadable detailed résumé (linked from the page)
assets/Alok-Deo-Singh-Pitch.pdf     Downloadable one-page pitch (linked from the page)
.nojekyll                            Tells GitHub Pages to serve files as-is
README.md                           This file
```

## Publish on GitHub Pages

1. Create a new repository on GitHub. For a personal site at
   `https://<username>.github.io`, name it exactly `<username>.github.io`.
   (Any other repo name works too — it will live at `https://<username>.github.io/<repo>/`.)
2. Upload these files to the repository — keep `index.html` at the repository root and the
   `assets/` folder alongside it. You can drag-and-drop via **Add file → Upload files**, or push with git:
   ```bash
   git init
   git add .
   git commit -m "Add personal résumé website"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set branch to **main** and folder to **/ (root)**, then **Save**.
6. Wait ~1 minute, then open the published URL shown on that Pages screen.

## Things to personalize

- **LinkedIn link** — in `index.html`, the Contact section has a LinkedIn button pointing to
  `https://www.linkedin.com/`. Replace it with your profile URL (e.g.
  `https://www.linkedin.com/in/your-handle`).
- **Content** — every role, school, and credential lives in the `MILESTONES` array near the
  bottom of `index.html`. Edit text there and both the timeline and résumé views update
  automatically. `CORE` and `TECH` hold the skill chips.
- **Résumé download** — replace `assets/Alok-Deo-Singh-Resume.docx` with an updated file
  (keep the same filename, or update the two links in `index.html`).

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```
