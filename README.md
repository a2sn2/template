
```markdown
# 🔮 Templates Hub — Leon & Kasper

One repo. Two live sites. Zero build tools. Pure HTML/CSS/JS with a sleek neon-glass hub.

- **Hub:** https://a2sn2.github.io/template/
- **Leon (One):** https://a2sn2.github.io/template/one/
- **Kasper (Two):** https://a2sn2.github.io/template/two/

---

## TL;DR

- 🚀 **Multi-site from one repo** via GitHub Pages subpaths (`/one/`, `/two/`)
- 🪟 **Zero dependencies** — no bundlers, no frameworks, just clean assets
- 🌌 **Fancy Hub**: typewriter title, starfield canvas, 3D tilt cards, copy-URL & keyboard shortcuts
- 🗂️ **All relative paths** so assets work under subfolders
- 🧠 **Large media** served from **GitHub Releases** (beats the 100MB git limit)

---

## What’s inside

```

/
├─ one/                # Leon site
│  ├─ index.html
│  ├─ css/ (leon.css, normalize.css, all.min.css)
│  ├─ images/ (landing.jpg, logo.png, ...)
│  └─ webfonts/ (Font Awesome)
├─ two/                # Kasper site
│  ├─ index.html
│  ├─ css/ (kasper.css, normalize.css, all.min.css)
│  ├─ images/ (landing.jpg, ...)
│  └─ webfonts/
└─ index.html          # Neon Hub (the page you land on)

````

**Hub features (no libraries):**
- Gradient neon background + glassmorphism
- Typewriter headline with shimmer
- Canvas starfield (tiny, performant)
- Tilt-on-hover cards (pure JS)
- Buttons: **Launch**, **Download video**, **Copy URL**
- Shortcuts: **1** → `/one/`, **2** → `/two/`, **C** → copy URL

---

## Live media (big files)

Full-HD videos are hosted as **Release assets**:

- `intro-1.webm` → https://github.com/a2sn2/template/releases/download/media-v1/intro-1.webm  
- `intro-2.mp4` → https://github.com/a2sn2/template/releases/download/media-v1/intro-2.mp4

This avoids the 100MB git file limit and keeps Pages fast.  
Update later? Publish `media-v2` and swap the URLs in `one/` and `two/`.

> Tip: guard against accidental commits by ignoring the files:
> ```
> one/intro-1.webm
> two/intro-2.mp4
> ```

---

## Run locally

Open the HTML files directly or spin a tiny server:

```bash
python -m http.server 8000
# visit http://localhost:8000/
````

---

## Deploy (GitHub Pages)

1. **Settings → Pages** → *Deploy from a branch*
2. **Branch:** `main`  •  **Folder:** `/ (root)`
3. Push to `main` → Pages auto-builds → links above go live

---

## Customize like a boss

### Colors & glow (Hub)

Edit CSS variables at the top of `index.html`:

```css
:root{
  --bg-1:#0b0f17; --bg-2:#111827;
  --neon:#7c3aed; --neon2:#22d3ee; --accent:#10b981;
}
```

### Card thumbnails

Change the background image per card:

```html
<div class="bg" style="background-image:url('one/images/landing.jpg')"></div>
```

### Add a third site

1. Create `three/` with `index.html`, `css/`, `images/`, `webfonts/`
2. Add another card in the Hub linking to `./three/`
3. Push → `https://a2sn2.github.io/template/three/` is live

### Download buttons inside sites

Each site can have a simple button:

```html
<a href="https://github.com/a2sn2/template/releases/download/media-v1/intro-1.webm" download>
  ⬇️ Download Full-HD
</a>
```

---

## Accessibility & performance

* High-contrast text, focus styles, and semantic HTML
* No external libraries → minimal payload
* Prefer WebP/AVIF images where possible

---

## License

MIT (feel free to adapt, remix, and ship).

---

### Credits

Built by **Mr. Eng** — future-friendly, glitch-free, and slightly obsessed with neon.

```

Want a dual-language version (English + Arabic) or an OG image for prettier link previews? I can generate both in the same style.
```
