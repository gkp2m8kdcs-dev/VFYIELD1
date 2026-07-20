# VFYIELD Static Site

This folder holds the four App-Store-required public pages for VFYIELD.

## Files

| File | Used in App Store Connect as |
|---|---|
| `index.html`     | Support URL (and/or the landing page) |
| `privacy.html`   | **Privacy Policy URL** (required) |
| `terms.html`     | Terms of Use URL (optional) |
| `support.html`   | Detailed support FAQ |
| `assets/`        | Shared CSS, no external dependencies |
| `robots.txt`     | SEO crawlers |
| `sitemap.xml`    | SEO sitemap |

## Before you deploy

Open these four files and replace **every** instance of:

- `Butraminamhegqulad@gmail.com`  → keep, this is your contact
- `YOUR-DOMAIN` (in `robots.txt`, `sitemap.xml`) → your real https URL, e.g. `https://vfyield.app`

Use `grep -r "YOUR-DOMAIN" .` to find both occurrences.

## How to host (three free options)

### Option A — GitHub Pages (recommended)

1. Create a repo, e.g. `vfyield-site`.
2. Push this folder to it.
3. In repo Settings → Pages → Source → `main` branch.
4. Your URL will be `https://<user>.github.io/vfyield-site/`.

### Option B — Netlify Drop

1. Go to https://app.netlify.com/drop.
2. Drag the `website/` folder onto the page. Done.
3. Netlify gives you a free `*.netlify.app` URL.

### Option C — Cloudflare Pages

1. Drag the folder onto https://pages.cloudflare.com.
2. Free `*.pages.dev` URL.

## App Store Connect URLs to paste in

Once deployed you will paste the same root URL into:

- **Privacy Policy URL**     → `https://<your-host>/privacy.html`
- **Support URL**            → `https://<your-host>/index.html`
- **Marketing URL** (opt.)   → `https://<your-host>/index.html`

## App Review Notes (paste into App Store Connect)

```
VFYIELD is a fully on-device educational similarity analyzer.
No network calls, no analytics, no third-party SDKs, no ID tracking.
All image and text scoring runs locally. Camera and Photos permissions
are requested only when the user explicitly taps the corresponding button.
In-app privacy notes are under Settings → Privacy & Notices.
Privacy Policy: https://<your-host>/privacy.html
Support: https://<your-host>/index.html
```
