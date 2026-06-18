# Akma — Cybersecurity E-Portfolio (Multi-Page)

A multi-page portfolio website — each navbar item links to its own HTML page instead of scrolling
down one long page. Built with plain HTML, CSS, and JavaScript (no frameworks, no build step).

## Structure

```
.
├── index.html           # Home — intro + quick links to other pages
├── about.html
├── education.html
├── projects.html
├── certificates.html
├── skills.html
├── experience.html
├── contact.html
├── style.css             # Shared design system (colors, type, layout)
├── script.js              # Mobile nav toggle (hamburger menu)
└── assets/
    ├── resume.pdf         # ← add your resume here
    └── images/
        └── profile.jpg    # ← add your photo here (falls back to "AKMA" placeholder if missing)
```

Every page shares the same navbar and footer, and highlights the current page in the menu
(e.g. on `projects.html`, "Projects" is shown in green/underlined).

## Before you publish — things to personalize

1. **Photo**: drop a photo into `assets/images/profile.jpg`.
2. **Resume**: drop your PDF into `assets/resume.pdf`.
3. **Contact links** (`contact.html`): replace the placeholder email, LinkedIn, and GitHub links.
4. **Certificates** (`certificates.html`): replace the 3 placeholder cards with your real certificates.
5. **Experience** (`experience.html`): replace the "Internship / Industrial Training" placeholder.
6. Double check facts in `about.html` and `education.html` match your latest details.

## Adding a new page

1. Copy any existing page (e.g. `about.html`) as a starting point.
2. Update the `<title>`, the `page-hero` text, and the main content.
3. Add a link to it in the `<nav class="nav-links">` block of **every** HTML file (so it shows
   up consistently across the whole site).

## Running locally

No build tools needed — just open `index.html` in a browser. Or run a local server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `e-portfolio`).
2. Push these files:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. On GitHub: go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", branch `main`,
   folder `/ (root)`.
5. Save. Your site goes live at:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO/
   ```
   (takes 1–2 minutes after the first deploy)

## Notes

- Fully responsive — collapses to a mobile hamburger menu under 768px.
- Respects `prefers-reduced-motion`.
- No external dependencies besides Google Fonts (JetBrains Mono + Inter).
