# bicell.ai — Landing Page

Static landing page for **BiCell AI**, deployed on **GitHub Pages** with the `bicell.ai` custom domain.

## Stack
- Pure HTML + CSS, no build step
- Google Fonts: Fraunces, DM Sans, JetBrains Mono
- Vanilla JS only (smooth scroll + reveal-on-load)

## Structure
```
.
├── index.html        # Single page
├── styles.css        # All styling
├── CNAME             # GitHub Pages custom domain (bicell.ai)
├── assets/
│   ├── bicell-ai-logo.png   # Transparent BiCell AI logo
│   ├── hero.png             # Hero background
│   ├── favicon.png          # 256×256 favicon
│   └── favicon-32.png       # 32×32 favicon
└── README.md
```

## Local preview
```bash
# Any static server works, e.g.:
python3 -m http.server 8000
# Then open http://localhost:8000
```

## Editing content
All copy lives in `index.html` — search for the section you want and edit text inline. Colors and fonts are CSS variables at the top of `styles.css`.

## Deployment

See the conversation that produced this site for full step-by-step deployment to GitHub Pages with the `bicell.ai` apex domain via GoDaddy DNS.

Quick recap:
1. Push this folder to a public GitHub repo
2. Repo → **Settings → Pages** → Source: Deploy from branch → `main` / `/ (root)`
3. Custom domain: `bicell.ai` → Save
4. In GoDaddy DNS for `bicell.ai`, add four A records pointing to GitHub Pages IPs:
   - `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
5. Add a CNAME record for `www` → `<your-github-username>.github.io`
6. Wait for DNS to propagate, then enable **Enforce HTTPS** in repo Pages settings
