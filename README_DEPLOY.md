# Deploy this site free on Netlify (no domain purchase, ~3 minutes)

This is a plain static site (HTML/CSS, no build step). It runs anywhere.

## Fastest path — Netlify drag-and-drop (free subdomain, $0)

1. Go to **https://app.netlify.com/drop**
2. Sign up for the free tier (email or GitHub login) if prompted.
3. Drag the **entire folder** `sketchy-survival-101-site` onto the drop zone.
   (Drag the folder itself — the one containing `index.html`, `css/`, `articles/`.)
4. Netlify instantly publishes it and gives you a URL like `random-words-123.netlify.app`.
5. Rename it: **Site configuration → Site details → Change site name** → set something like
   `sketchysurvival101` → your live URL becomes **https://sketchysurvival101.netlify.app**.
6. HTTPS is automatic. You're live.

## Then apply to Home Depot / Impact with that URL
The required pages are already built and linked in the nav + footer:
- About — `/about.html`
- Affiliate Disclosure — `/disclosure.html`
- Privacy Policy — `/privacy.html`
- Contact — `/contact.html`
- 3 original, sourced articles under `/articles/`

## Later (optional) — attach a custom domain for much better approval odds
Hosting stays free; only the domain costs (~$1–12/yr at Porkbun or Cloudflare).
In Netlify: **Domain management → Add a domain** → follow the DNS steps. No re-deploy needed.

## To update the site later
Re-drag the folder onto the same site (Deploys tab → drag to redeploy), or connect a
Git repo for auto-deploys. `netlify.toml` is already configured for a no-build deploy.

## Local preview
From this folder: `python3 -m http.server 8099` then open `http://127.0.0.1:8099`.
