# Project context and continuation notes

This file summarizes the relevant decisions and state from the website conversation so future work can continue in this repository.

## Website

- Public site: https://d-krovos.github.io/sith-empire-launcher-hologram/
- Public source repository: https://github.com/D-Krovos/sith-empire-launcher-hologram
- The site is a separate replacement site; the earlier launcher website was left untouched.
- It uses a black page background with one crisp, spinning Sith crest as a fixed, full-page background layer behind the page content. The emblem is not confined to the hero or screenshot. Translucent panels allow it to remain visible behind lower content.
- Current page has one download CTA labeled “Direct Download,” linking to `downloads/SLauncher.exe` without an operating-system label. The old Linux archive and Windows ZIP remain in `downloads/` but are not linked from the page because the Linux build is outdated and platform-specific options are deferred.

## Repository and publishing

- `main` is the editable source branch; `gh-pages` publishes the repository root through GitHub Pages. Both branches are kept in sync.
- `index.html` contains the page markup/styles. Reusable images and font are under `assets/`; downloadable files are under `downloads/`.
- `README.md` documents the edit and publish commands. After editing and committing `main`, publish with `git push origin main:gh-pages`.
- The original local working copy is in `site-hologram-release/` inside the launcher project folder.

## Earlier launcher context

- The launcher site download currently serves the v0.1.3 Windows executable. Earlier troubleshooting identified TLS certificate trust for JoF downloads and a too-short Sith Cloud endpoint timeout; those were addressed in that launcher version.
- Treat launcher binary updates and website changes as separate tasks. When updating the direct download, replace `downloads/SLauncher.exe` with the intended release and update checksums/version information as appropriate.
