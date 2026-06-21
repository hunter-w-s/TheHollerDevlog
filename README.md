# The Holler — Devlog Site

A plain static devlog. No Jekyll, no build step, no framework. Two pages:
**Log** (`index.html`) and **Plates** (`gallery.html`), sharing `style.css`.

---

## Publish on GitHub Pages (one time, ~5 minutes)

1. Make a new GitHub repo (e.g. `holler-devlog`). Public is required for free Pages.
2. Put these files in the repo root: `index.html`, `gallery.html`, `style.css`, and the `images/` folder.
3. Push them up.
4. On GitHub: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**, pick your branch (usually `main`) and folder `/ (root)`. Save.
5. Wait ~1 minute. Your site is live at `https://<your-username>.github.io/holler-devlog/`.

That's it. Every time you push a change, the live site updates automatically.

---

## Add a new log entry

Open `index.html`. Find the comment `NEWEST ENTRY ON TOP`. Copy one `<article class="entry">...</article>` block and paste it **above** the others (newest first). Edit:

- the `<time datetime="YYYY-MM-DD">` and the displayed date
- the `LOG 00X` number
- the title and the paragraphs

Save, commit, push. Done.

---

## Add a picture (Plate)

1. Drop the image file into the `images/` folder (e.g. `images/greenbrier-hillshade.png`).
2. Open `gallery.html`. There's a commented-out **real plate example** near the bottom — copy it, uncomment it, and point `src` at your image, write the `alt` text and caption.
3. Delete or keep the placeholder plates as you like.
4. Commit, push.

Images look best at 16:9 (they're cropped to fill that frame). Any size works.

---

## Notes

- Fonts (Space Mono + Spectral) load from Google Fonts; needs internet to render as designed, falls back to system fonts offline.
- Everything is hand-editable HTML/CSS. No tooling required.
- If you later want automatic dated posts from markdown files, that's when Jekyll
  becomes worth it — but this stays simple until you want that.
