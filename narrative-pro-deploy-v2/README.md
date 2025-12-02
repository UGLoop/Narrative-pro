# Narrative Pro — Static Deploy (V2)

Includes hosting configs for both Vercel and Netlify so `/auth/callback` works.

## Files
- `index.html` — app placeholder (iframe-safe)
- `auth/callback/index.html` — OAuth echo page
- `200.html` + `_redirects` — Netlify SPA fallback
- `vercel.json` — Vercel routes so `/auth/callback` resolves and SPA fallback works

## Deploy
### Netlify Drop
Drag-and-drop this folder/zip. Netlify URL is returned immediately.

### Vercel
Import → Deploy. Framework: **Other** (or None). Build command: **None**. Output directory: **.** (root).

## Shopify Partner
- App URL: `https://YOUR_HOST/`
- Allowed redirection URL(s): `https://YOUR_HOST/auth/callback`
