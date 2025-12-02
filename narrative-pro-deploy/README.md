# Narrative Pro — Deploy Starter (Static)

This package gives you a **ready-made static site** that satisfies Shopify Partner "App setup" requirements:
- `index.html` — iframe‑friendly placeholder for the embedded app UI
- `auth/callback/index.html` — visible OAuth callback page that **echoes query params**
- `200.html` — SPA fallback for static hosts (e.g., Netlify)
- No build step required — just host these files

## Quick Deploy

### Option A — Netlify Drop (drag & drop)
1. Search for **Netlify Drop** and open it.
2. Drag the folder or ZIP into the page.
3. Netlify replies with a public URL like `https://narrative-pro-live.netlify.app`.

### Option B — Vercel (no build)
1. Create a new project → **Import → Deploy**.
2. Upload this folder/ZIP or connect a repo that contains these files.
3. Set output to the root (no build command required) → Deploy to get a public URL.

> You can connect a custom domain later. Not required for Shopify setup.

## Shopify Partner Dashboard — Required Fields
- **App URL**: your public URL, e.g. `https://YOUR-SITE.netlify.app/`
- **Allowed redirection URL(s)**: `https://YOUR-SITE.netlify.app/auth/callback`
- **Embed app in Shopify admin**: enabled (done in dashboard)

This static callback lets Shopify “return” from OAuth. Later, a developer will replace it with a server handler that exchanges the `code` for tokens and redirects back to your embedded UI.

## Next Steps (when you add development)
- Keep the **same public URL** (no dashboard changes).
- Build your React/JSX (`app.ai_writer.jsx`) into a `bundle.js` and mount into `#root` in `index.html`.
- Implement `/auth` + `/auth/callback` on a server for real OAuth.
- Use App Bridge + session tokens for Admin API calls.

