# Zixuan (Vicky) Lu — Personal Homepage

Static site with a clean modern design inspired by [ruixu.me](https://ruixu.me/).
Pure HTML/CSS — no Jekyll, no Next.js, no build step. Single stylesheet.

## Folder layout

```
new/
├── index.html          # single-page site
├── css/main.css        # single custom stylesheet (uses Inter from Google Fonts)
├── images/             # profile + publication thumbnails
└── files/              # CV, papers, posters, demo video
```

## Run locally (debug)

The site is plain static files. Open `index.html` directly works, but a local
HTTP server is recommended (relative paths, fonts, PDFs all behave better).

Pick any one:

### Python (built-in, easiest)

```bash
cd new
python -m http.server 8000
```

Then open http://localhost:8000 in your browser.

### Node (if installed)

```bash
cd new
npx serve .
# or
npx http-server -p 8000
```

### VS Code

Install the "Live Server" extension, right-click `index.html` → *Open with Live Server*.

## Deploy to GitHub Pages

1. Create a repository named `<your-username>.github.io` (e.g. `ZiXuanVickyLu.github.io`).
2. Copy the **contents** of this `new/` folder into the repo root (not the `new` folder itself — `index.html` must be at the repo root).
3. Commit & push to the `main` branch.
4. In the GitHub repo settings → Pages → Source = `main` / `/ (root)`.
5. Your site will be live at `https://<your-username>.github.io/`.

## Customization notes

- **Profile photo**: replace `images/profile.png`.
- **CV**: replace `files/cv_en_2025_7.pdf` (and update the link in `index.html` if you rename it).
- **Experience logos**: the "Experience" section uses text placeholders in the
  `.logo-grid`. Drop real logo PNGs into `images/` (e.g. `images/logo_utah.png`)
  and replace the text inside each `<div class="logo">...</div>` with
  `<img src="images/logo_utah.png">`.
- **Profile card icons**: inline SVGs inside the `.profile-card` — edit the
  text next to each icon. Social link row at the bottom also uses inline SVG.
- **Gradient**: the "Hi, there!" gradient and the bar under the profile card
  come from `--gradient` in `css/main.css`. Change it in one place.
- **News / publications**: edit the corresponding `<ul>` blocks in `index.html`.
