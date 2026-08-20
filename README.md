# Setting up GitHub Pages

## 1. Create the repository
1. On GitHub, click **New repository**.
2. Name it `YOUR-USERNAME.github.io` (replace with your actual GitHub username, exactly, including the `.github.io` suffix). This special name makes GitHub serve it as your main personal site at `https://YOUR-USERNAME.github.io`.
   - If you'd rather keep it as a secondary project site instead of your main one, you can name it anything (e.g. `notes`) — it'll then be served at `https://YOUR-USERNAME.github.io/notes/`.
3. Make it **Public** (Pages requires this on free accounts).
4. Don't initialize with a README (you already have one) — or if you do, you'll just overwrite it.

## 2. Add the files
Put these at the **root** of the repo:
```
index.html
README.md
files/
  drp-lie-symmetries-report.pdf   <- your actual DRP report goes here
```
Create the `files/` folder and drop your DRP report PDF in it, named exactly `drp-lie-symmetries-report.pdf` (or update the two links in `index.html` if you name it differently).

You can do this either by dragging files into the GitHub web UI ("Add file" → "Upload files"), or via git:
```bash
git clone https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
cd YOUR-USERNAME.github.io
# copy index.html, README.md, and files/ into this folder
git add .
git commit -m "Initial site"
git push
```

## 3. Turn on Pages
1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` (or `master`) and folder to `/ (root)`. Save.
4. Wait 1–2 minutes, then visit the URL GitHub shows you (or `https://YOUR-USERNAME.github.io`).

## 4. Before you go live
- Replace `YOUR-USERNAME` in the GitHub link inside `index.html` with your real username.
- Add your DRP report PDF to `files/`.
- Double check the report title/description in the "Writing" section matches your actual report.
- Once the review article is finished, add it the same way: copy the DRP `<div class="entry">` block, fill in its own title/date/abstract/link, and paste it above the "More notes will go here" slot.

That's it — no build step, no Jekyll config needed, it's a single static HTML file.
