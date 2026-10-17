# priem5-site

The public site of Прием5: https://priem5.com

Static HTML on GitHub Pages, deployed from `main` (root folder). A push to `main` is live in about a minute. Current state: the coming-soon page.

## Files

| File | Purpose |
|---|---|
| `index.html` | Coming-soon page with meta description, canonical, Open Graph, Twitter card and JSON-LD (Organization, WebSite) |
| `og-image.png` | 1200×630 social preview |
| `favicon.ico`, `favicon.svg`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `logo-512.png` | Icons; `logo-512.png` is referenced by the JSON-LD |
| `site.webmanifest`, `robots.txt`, `sitemap.xml` | Manifest and crawler files |
| `CNAME` | Custom domain `priem5.com` |
| `.nojekyll` | Serve files as-is |

## Domain

priem5.com is registered at Namecheap and uses Cloudflare nameservers. Cloudflare proxies to GitHub Pages with SSL mode Full and Always Use HTTPS. "Enforce HTTPS" in Pages settings stays off, because TLS is handled by Cloudflare.


## Adding a page

1. Add the HTML file with its own `<title>`, description, canonical link and OG tags.
2. Add its URL to `sitemap.xml` and update `lastmod`.
3. After deploy, request indexing in Google Search Console.
