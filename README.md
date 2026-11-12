# Alejandro Mosquera García: personal research page

A plain, single-page academic site in the style economists at top departments use for their homepages:
photo and contact block at the top, a short bio, then papers listed by status with bracketed [Abstract] toggles.
No frameworks, no build step, no JavaScript. One HTML file.

## Publish on GitHub Pages (about 5 minutes)

1. On GitHub, create a new **public** repository named exactly `YOUR-USERNAME.github.io`.
2. Upload everything in this folder (`index.html`, `.nojekyll`, `README.md`, and the `files/` folder).
   Easiest route: on the new repo's page, click **uploading an existing file** and drag the files in, then **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io`.

From the command line instead:

```bash
cd site
git init && git add . && git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git push -u origin main
```

## Files to add

- `files/photo.jpg`: a headshot (roughly 3:4, at least 300 px wide). The page hides the image slot until this exists.
- `files/Mosquera_Garcia_CV.pdf`: your CV. The "CV" link in the header points here.
- Paper PDFs, if you want to post them: put them in `files/` and add a link inside the paper's `links` span, e.g.
  `<a href="files/rerouting_under_threat.pdf">Paper</a>`. The brackets are added automatically.

## Editing

- Each paper is one `<div class="paper">` block. Copy a block to add a paper; move blocks between
  *Working Papers*, *Theses*, and *Work in Progress* as their status changes.
- For a coauthored paper, add `<span class="meta">(with First Last)</span>` under the title.
- Update the "Last updated" line at the bottom when you change the page.
