# Ganesh Bharate — Portfolio Site

A static HTML/CSS/JS portfolio built from your résumé. No build tools,
no frameworks, no server required — it runs by opening a file.

## Folder structure

```
portfolio/
├── index.html              → the whole site (one page)
├── css/
│   └── style.css
├── js/
│   └── script.js
├── assets/
│   ├── images/
│   │   └── profile.png     → your photo
│   └── docs/
│       └── Ganesh_Bharate_Resume.pdf   → downloadable from the Contact section
└── README.md
```

## Run it locally (offline)

Just double-click `index.html` — it opens in your default browser and
works fully offline. The only thing that needs the internet is the
Google Fonts link in `<head>`; without a connection it silently falls
back to system fonts, so the page still works, just with a slightly
different typeface.

If you want to preview it exactly like a real web server (optional),
from inside the `portfolio` folder run:

```
python3 -m http.server 8000
```

then open `http://localhost:8000` in a browser.

## Editing content

- Text, experience bullets, certifications: edit directly in `index.html`.
- Colors, fonts, spacing: edit the variables at the top of `css/style.css`
  (the `:root { ... }` block).
- Swap the photo: replace `assets/images/profile.png` with a new image
  of the same filename, or update the `src` in the `<img>` tag in
  `index.html`.

## Putting it on a domain

This site is pure static files, so it runs on **any** web host or
static-site platform. Three common paths:

**1. Shared hosting / cPanel (GoDaddy, Hostinger, Namecheap, etc.)**
Upload the entire contents of the `portfolio` folder into `public_html`
(or your domain's document root) via the File Manager or FTP. Make
sure `index.html` sits at the root of that folder, not nested inside
another `portfolio/` subfolder.

**2. Netlify or Vercel**
Drag and drop the `portfolio` folder onto their dashboard (or connect
a Git repo). Then add your custom domain in the site's Domain
settings and follow their DNS instructions (usually a CNAME or A
record at your registrar).

**3. GitHub Pages**
Push the contents of `portfolio` to a repository, enable Pages in the
repo settings, and point it at the branch/folder. For a custom domain,
add a file named `CNAME` at the root containing just your domain
(e.g. `ganeshbharate.com`), then set a CNAME record at your domain
registrar pointing to `<username>.github.io`.

In all three cases, no code changes are needed — the domain
connection happens at the hosting/DNS level, not in the site files.
