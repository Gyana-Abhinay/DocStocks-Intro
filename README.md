# Docstocks — Stealth Landing Page

The coming-soon / stealth landing page for **[docstocks.in](https://docstocks.in)** — the first digital ecosystem engineered for the Indian medical community. *By Medicos. For Medicos.*

A single, self-contained static page (no build step, no backend). Contact is via social links only.

## Structure

```
index.html                 # the whole site (inline CSS + JS)
intro-loading-video.mp4     # brand intro clip (plays first)
assets/
  logo.png                 # favicon
  logo-correct.png         # header / signoff / footer logo
  img/                     # product photography (hero, pillars, showcase)
```

## Run locally

Any static server works, e.g.:

```bash
python -m http.server 5050
# then open http://localhost:5050
```

## Deploy on Vercel

This is a plain static site, so no framework or build is needed:

1. Import the repo in Vercel.
2. **Framework Preset:** `Other`
3. **Build Command:** *(leave empty)*
4. **Output Directory:** `.` (root)
5. Deploy, then add the custom domain (`docstocks.in`) under Project → Settings → Domains.

## Notes

- The page currently carries a `robots: noindex` tag (stealth). Remove it from `index.html` when you want search engines to index the site.
- After the domain is live, update the `og:image` meta tag in `index.html` to an absolute URL (e.g. `https://docstocks.in/assets/img/scrubs.jpeg`) so link previews work on WhatsApp/LinkedIn.
