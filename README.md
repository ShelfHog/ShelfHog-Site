# Public site (`docs/`)

This folder should contain **only** marketing + legal HTML (and `.nojekyll`). Internal notes (`branding`, eBay OAuth checklist, API samples) live in **`developer-docs/`** at repo root so they are not published if you use GitHub Pages from `/docs`.

## Enable GitHub Pages

1. GitHub repo **Settings → Pages**.
2. **Build and deployment → Source:** “Deploy from a branch”.
3. **Branch:** `main`, folder **`/docs`**, Save.

After a minute, the site is live at:

`https://<username-or-org>.github.io/<repo>/`

Example: links become

- `…/legal/privacy.html`
- `…/legal/terms.html`
- `…/legal/support.html`

## Private repo + free GitHub account

GitHub may require **GitHub Pro** (or higher) to publish Pages from a **private** repository. If Pages is disabled for that reason, either:

- Create a **separate public** repo that contains **only** this `docs/` tree, or  
- Host these files on Namecheap static hosting / Cloudflare Pages / Netlify.

## Custom domain (`shelfhog.com`)

In Pages settings, set **Custom domain** to e.g. `www.shelfhog.com` and follow GitHub’s DNS instructions.  
You can add a `CNAME` file in `docs/` with one line: `www.shelfhog.com` (after you own that hostname).

## App Store URLs

Use your final HTTPS URLs, for example:

- Privacy Policy: `https://www.shelfhog.com/legal/privacy.html` (or your GitHub Pages equivalent)
- Support: `https://www.shelfhog.com/legal/support.html`
