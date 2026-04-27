# Personal site

Two static files: `index.html` and `style.css`. No build step. No JavaScript framework. The only script is a 10-line click-to-reveal email handler.

## What you need to fill in

Search the file for `example.com`, the `TODO` comments, and the `<em>...</em>` italic placeholders inside `index.html`. Specifically:

1. **Photo.** Add `assets/portrait.jpg` (square, ~400x400 minimum). Then in `index.html`, replace the placeholder SVG inside `<div class="portrait">` with `<img src="assets/portrait.jpg" alt="Ted Ma">`.
2. **Domain.** Replace `https://example.com/` in the `og:url`, `og:image`, and `<link rel="canonical">` tags.
3. **Email.** Update `data-user="ted"` and `data-domain="example.com"` on the `button.email`.
4. **Social links.** Replace the bare `https://github.com/` etc. with your actual handles.
5. **Education and prior work.** Fill in the third timeline entry.
6. **Writing / projects.** Replace the italic placeholders with real content as you produce it.
7. **Favicon.** Drop a small `favicon.svg` (or `.png`) into `assets/`.

## Local preview

```
cd site
python3 -m http.server 8000
```

Open http://localhost:8000.

## Deployment options

| Option | Cost | Effort | DNS |
| --- | --- | --- | --- |
| GitHub Pages | Free | Push repo, enable Pages | CNAME to `<user>.github.io` |
| Cloudflare Pages | Free | Connect repo, deploy | Built in if domain on Cloudflare |
| Netlify | Free | Drag and drop or git connect | CNAME |
| Vercel | Free | Git connect | CNAME |

For a minimum-friction setup: register the domain at Cloudflare Registrar (at-cost pricing, no markup), host the site on Cloudflare Pages, point the apex record at the Pages project. Done.

## Color customization

All theming lives in CSS variables at the top of `style.css`. The accent (`--accent`) is the only color that touches links, hover states, and selection. Change it in one place to retheme.

## Dark mode

Automatic via `prefers-color-scheme: dark`. Visitors see whichever matches their OS setting. No toggle.
