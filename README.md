# strangehumaan.github.io

Personal site of Mohammad Saad Nathani. Live at https://strangehumaan.github.io

Plain static files. No build step, no framework, no JavaScript.

```
index.html    the whole page
style.css     about 25 lines of CSS
favicon.svg   tab icon
resume.pdf    linked from the Contact section
```

## Add a project

Open `index.html`, find `<section id="projects">`, and copy one `<li>` block:

```html
<li><a href="https://github.com/Strangehumaan/REPO">REPO</a>: One plain sentence on what it does.<br>
<span class="meta">Language, main libraries</span></li>
```

- Projects without a public repo: drop the `<a>` and write the name as plain text.
- Live demo: add `<a href="https://...">Live demo</a>.` after the description.
- Order: most important first.

## Edit other sections

Each section is a `<section id="...">` in `index.html`: `about`, `projects`, `experience`, `awards`, `education`, `skills`, `contact`. Edit the text directly. Change the "Last updated" line in the footer when you do.

## Update the resume

Replace `resume.pdf` with the new file, keeping the same name.

## Preview locally

Open `index.html` in a browser. Nothing else is needed.

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
2. Clone it, add `index.html`, `style.css`, `favicon.svg` and `resume.pdf` at the root, then commit and push to `main`.
3. In the repository, go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and click Save.
4. Wait about a minute, then open https://strangehumaan.github.io.
