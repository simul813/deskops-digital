# DeskOps Digital — static mini-site

Static HTML/CSS site for the Freelance Ops Kit landing page and SEO pillar guide. Ready for **GitHub Pages**.

**Brand:** DeskOps Digital only (no fiction bleed).  
**Product CTA:** [Freelance Ops Kit — $19](https://vancesterling.gumroad.com/l/ddcdbx)

## Contents

| Path | Purpose |
|------|---------|
| `index.html` | Product landing |
| `guides/freelance-invoice-tracker-spreadsheet.html` | Pillar SEO article |
| `guides/index.html` | Guides index |
| `styles.css` | Shared styles |
| `robots.txt` / `sitemap.xml` | Crawl helpers |
| `404.html` | GitHub Pages 404 |

Canonical URLs in meta/sitemap assume `https://simul813.github.io/deskops-digital/`. Update them if you launch on a `username.github.io` path first.

## Publish to GitHub Pages

### Option A — Project site (fastest)

1. Create a public repo (e.g. `deskops-digital-site`).
2. Push the contents of **this `site/` folder** to the repo root (or push this folder as a `/docs` directory).
3. GitHub → **Settings → Pages**:
   - Source: **Deploy from a branch**
   - Branch: `main` (or `master`), folder `/` (or `/docs` if you used that)
4. Wait for the green check. Site URL will be `https://<user>.github.io/<repo>/`.
5. If using a project path, update `canonical`, `sitemap.xml`, and `robots.txt` Sitemap URL to match (include the repo path).

### Option B — Custom domain (`simul813.github.io/deskops-digital`)

1. Complete Option A.
2. In Pages settings, add custom domain `simul813.github.io/deskops-digital`.
3. At your DNS provider, add the records GitHub shows (usually `A`/`AAAA` for apex or `CNAME` for `www`).
4. Enable **Enforce HTTPS** once DNS propagates.
5. Keep canonicals as `https://simul813.github.io/deskops-digital/...` (already set).

### Clean URLs for the guide (optional)

GitHub Pages serves `guides/freelance-invoice-tracker-spreadsheet.html` as that path. For `/guides/freelance-invoice-tracker-spreadsheet/` without `.html`:

- Rename to `guides/freelance-invoice-tracker-spreadsheet/index.html`, **or**
- Add a simple Jekyll/`_config.yml` with `permalink` rules if you prefer.

Sitemap already uses the trailing-slash form for the article; align the live file path when you deploy.

## After go-live checklist

- [ ] Open landing + article on mobile; click Gumroad CTA (new tab)
- [ ] Confirm UTMs on outbound links
- [ ] Submit `sitemap.xml` in Google Search Console
- [ ] Replace screenshot placeholders with real Dashboard / Invoices / Clients captures when ready
- [ ] Pin first batch from `../seo/pinterest-pins.md` → article URL

## Local preview

```bash
cd site
python3 -m http.server 8080
# open http://localhost:8080
```

## Constraints

- Soft CTAs only
- Tax field language = **planning placeholder** only — no tax advice
- No Vance Sterling fiction voice on these pages

---

DeskOps Digital · Sep 2026
