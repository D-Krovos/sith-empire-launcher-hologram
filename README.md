# Sith Empire Launcher website

Public website: https://d-krovos.github.io/sith-empire-launcher-hologram/

This repository contains the complete editable website and the files it serves. Keep using this repository for future changes; a new site is not needed.

## Source and publishing

- `main` is the editable source branch.
- `gh-pages` is the GitHub Pages publishing branch. Both branches currently contain the full site.
- GitHub Pages is configured to publish the repository root from `gh-pages`.
- The website source is `index.html`; images and font are in `assets/`.
- Download files are in `downloads/`. The page currently exposes only `downloads/SLauncher.exe` as its Direct Download. The other archives are retained for later updates.

To make a future website change, clone this repository, edit the source/assets/downloads, then publish the updated tree from `main` to `gh-pages`:

```powershell
git clone https://github.com/D-Krovos/sith-empire-launcher-hologram.git
cd sith-empire-launcher-hologram
# Edit index.html or files under assets/ and downloads/
git add .
git commit -m "Describe the website update"
git push origin main
git push origin main:gh-pages
```

The deployed page updates after GitHub Pages finishes its build. The local working copy used for the latest edits is `site-hologram-release/` inside the launcher project folder.
