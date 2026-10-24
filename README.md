# Moira Bohley — personal site

Plain HTML/CSS, no build step. GitHub Pages serves it as-is.

## Publish on GitHub Pages (about 5 minutes)

1. On GitHub, create a **public** repo named exactly `YOUR-USERNAME.github.io`.
2. Upload everything in this folder to the repo root (drag and drop on the repo page works), and commit.
3. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io`.

Optional custom domain: buy `moirabohley.com` (or similar), add it under Settings → Pages → Custom domain, follow GitHub's DNS instructions, and tick **Enforce HTTPS**.

## Fill in the draft

Anything highlighted in yellow on the site (`<span class="todo">`) is a placeholder. Search the files for `YOUR-` and `todo` to find them all.

- **Resume:** add `assets/Bohley_Resume.pdf`.
- **Photo:** replace `assets/img/headshot.jpg` with a square photo.
- **Links:** GitHub and LinkedIn URLs in `index.html`; Google Scholar once your profile exists.
- **Videos:** upload each paper video to YouTube (unlisted is fine). Paste the video ID (the part after `watch?v=`) into the `YOUR-VIDEO-ID` spot on each paper page.
- **GIF thumbnails:** make a 5–10 s clip from each video and save it as the matching file in `assets/img/`. Keep each under ~3 MB, e.g.:
  `ffmpeg -ss 00:00:12 -t 8 -i video.mp4 -vf "fps=12,scale=640:-1:flags=lanczos" -loop 0 ct-thumb.gif`
- **Figures:** export Fig. 1 and a key result plot from each paper into `assets/img/`.
- **Author lists:** check both against the arXiv pages.
- **"My contribution" boxes:** these matter most to hiring managers. Make each bullet something you personally owned.
- **More projects:** copy `projects/slam.html` as a template and add a card in the Projects grid in `index.html`.

When nothing is left to fill in, delete the `.todo` rule at the bottom of `assets/style.css`.
