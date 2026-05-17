# Ammar Hannun — Portfolio

Personal portfolio site for AI / ML / CS internship applications.

**Live:** [ammarhannun.github.io](https://ammarhannun.github.io) *(once deployed)*

## Stack

- Plain **HTML / CSS / vanilla JS** — no build step, no dependencies
- Inter + JetBrains Mono via Google Fonts
- Dark mode (system-aware, with manual toggle)
- Fully responsive, accessible, < 100KB total

## Project structure

```
portfolio/
├── index.html              # Single-page site (Hero / About / Skills / Projects / Experience / Contact)
├── styles.css              # All styling, theme tokens, responsive rules
├── script.js               # Theme toggle, mobile nav, scroll reveal
├── assets/
│   ├── headshot.jpg        # ← drop your photo here (see below)
│   └── Ammar_Hannun_Resume.pdf
└── README.md
```

## 1. Add your headshot

Save the photo you sent as **`assets/headshot.jpg`**. That's it — the site will pick it up automatically. If the file is missing, the hero falls back to your initials on a gradient.

> Tip: square-ish or portrait orientation works best (currently displayed as a 320×400 frame with subtle rotation).

## 2. Preview locally

Open `index.html` directly in your browser — it works with no server. Or, for a cleaner local URL:

```bash
cd ~/portfolio
python3 -m http.server 8000
# then open http://localhost:8000
```

## 3. Deploy to GitHub Pages (free, your own URL)

This setup deploys to `https://ammarhannun.github.io` — the special "user site" URL tied to your GitHub username.

```bash
cd ~/portfolio
git init -b main
git add .
git commit -m "Initial portfolio site"

# Create the repo on GitHub first — it MUST be named exactly:
#   ammarhannun.github.io
# (lowercase, matches your username)
# Then connect and push:

git remote add origin https://github.com/Ammarhannun/ammarhannun.github.io.git
git push -u origin main
```

Then on GitHub:

1. Go to **Settings → Pages**
2. Under **Source**, choose **Deploy from a branch**
3. Pick branch **`main`** and folder **`/ (root)`**
4. Save. Within ~1 minute, your site is live at **https://ammarhannun.github.io**

## 4. Future tweaks

All copy lives in `index.html`. Things you'll likely update over time:

- **Hero tagline** — change in `<section id="home">`
- **Project cards** — each `<article class="project-card">` is self-contained. Add a new one anytime you ship something.
- **Project GitHub links** — currently point to your profile root. Once you have public repo URLs per project, swap them in.
- **Resume** — replace `assets/Ammar_Hannun_Resume.pdf` whenever you update it (keep the filename so the download button still works).
- **Accent colour** — tweak `--accent` in `styles.css` (currently `#2563eb`).

## Notes for recruiters reading the source

Yes, this site is hand-written. No framework, no bundler, ~600 lines of CSS, one small JS file. The point of a portfolio is signal, not stack — but I'll happily talk about why a static site is the right call for this content.
