# Personal site &mdash; Ted (Yufei) Ma

Two static files plus assets. No build step. No framework. Hosted free on GitHub Pages, Cloudflare Pages, Netlify, or Vercel.

## Files

```
site/
├── index.html          # markup
├── style.css           # styling
├── README.md
└── assets/
    ├── portrait.jpeg   # headshot
    ├── favicon.svg     # browser tab icon
    └── Ted-Ma-Resume.docx
```

## Deploy on GitHub Pages

1. Create a public repo named `<your-username>.github.io`.
2. Upload the contents of this `site/` directory to the repo root (so `index.html` sits at the top level, not inside a subfolder).
3. Settings &rarr; Pages &rarr; confirm "Deploy from a branch" / `main` / `/(root)`.
4. Wait one minute. Visit `https://<your-username>.github.io`.

## Local preview

```
cd site
python3 -m http.server 8000
```

Open http://localhost:8000.

## Edits to make before going live

1. Replace `https://example.com/` in the `og:url`, `og:image`, and canonical link tags with your actual URL.
2. Replace `https://github.com/` in the GitHub link with your real GitHub profile (or remove the link entirely if you do not want one yet).
3. Optional: update `assets/favicon.svg` with a different monogram or a small icon you prefer.

## Customizing

All colors, fonts, and spacing live in CSS variables at the top of `style.css`. Change `--accent` once to retheme. The site auto-switches between light and dark modes based on the visitor&rsquo;s OS preference.
