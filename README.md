# strangehumaan.github.io

Personal site of Mohammad Saad Nathani. Live at https://strangehumaan.github.io

Plain static files. No build step, no framework, no JavaScript. Follows the system light/dark setting.

```
index.html    the whole page
style.css     all styling (colours are variables at the top)
favicon.svg   tab icon
photo.jpg     profile photo, shown as a circle (square image works best)
resume.pdf    linked from the contact buttons at the top
```

## Add a project

Open `index.html`, find `<section id="projects">`, and copy one `<article>` block:

```html
<article class="item">
  <h3><a href="https://github.com/Strangehumaan/REPO">REPO</a></h3>
  <p>One plain sentence on what it does.</p>
  <p class="links"><a href="https://...">Live demo</a></p>
  <ul class="tags"><li>Python</li><li>PyTorch</li></ul>
</article>
```

- No public repo: write the name without the `<a>`.
- No demo or extra links: delete the `<p class="links">` line.
- Award or status label: add `<span class="badge">1st place</span>` (or `class="badge muted"`) inside the `<h3>`.
- Order: most important first.

## Edit other sections

Contact buttons and the quick-facts strip are at the top of `index.html`. Each section below is a `<section id="...">`: `about`, `projects`, `experience`, `awards`, `education`, `skills`. Experience, awards and education entries use a `<div class="row">` with the title on the left and `<span class="date">` on the right. Change the "Last updated" line in the footer when you edit.

## Update the resume

Replace `resume.pdf` with the new file, keeping the same name.

## Preview locally

Open `index.html` in a browser, or run `python -m http.server` in this folder and open http://localhost:8000.

## Deploy

This folder is already linked to `github.com/Strangehumaan/strangehumaan.github.io`. To publish changes:

```bash
git add .
git commit -m "Update site"
git push origin main
```

The site updates within a minute or two.

### First-time setup (already done for this repo)

1. On GitHub, create a **public** repository named exactly `strangehumaan.github.io`.
2. Clone it, add `index.html`, `style.css`, `favicon.svg`, `photo.jpg` and `resume.pdf` at the root, then commit and push to `main`.
3. In the repository, go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and click Save.
4. Wait about a minute, then open https://strangehumaan.github.io.
