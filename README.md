# ShelfHog-Site (public)

Static marketing + legal pages for ShelfHog. **No app or backend code**—safe to stay public.

Canonical copy edits happen in the private **`ShelfHog/ShelfHog`** repo under `docs/`, then sync here (rsync or manual copy).

## GitHub Pages

1. **Settings → Pages**
2. **Source:** Deploy from branch **`main`**
3. **Folder:** **`/` (root)** — not `/docs` (this repo is already “flat”)

Live URL:

`https://shelfhog.github.io/ShelfHog-Site/`

Legal pages:

- `/legal/privacy.html`
- `/legal/terms.html`
- `/legal/support.html`

## Custom domain (`shelfhog.com`)

In Pages settings, set **Custom domain** (e.g. `www.shelfhog.com`) and add a **`CNAME`** file in this repo with one hostname line if GitHub asks for it.

## Sync from private monorepo

From your machine (parent directory of both clones):

```bash
rsync -a --delete ShelfHog/docs/ ShelfHog-Site/
cd ShelfHog-Site
git add -A && git status
git commit -m "Sync site from private repo docs/" && git push
```

Use `--delete` only if you want the public repo to drop files removed from `docs/`.
