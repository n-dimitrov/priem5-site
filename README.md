# priem5-site

The public site of Прием5: https://priem5.com

Static HTML on GitHub Pages, deployed from `main` (root folder). A push to `main` is live in about a minute. Current state: the landing page with links into the app at app.priem5.com.

## Files

| File | Purpose |
|---|---|
| `index.html` | Landing page with meta description, canonical, Open Graph, Twitter card and JSON-LD (Organization, WebSite). Its „Следващ срок“ card is filled in the browser from the open API `https://app.priem5.com/api/catalog/v1/deadlines?limit=1` and stays hidden if that call fails |
| `qr-survey-past.svg`, `qr-survey-now.svg` | QR codes for the two parent surveys on OurPulse, shown in the landing card on wide screens. The card hides itself after 1 Nov 2026, 23:59 Sofia time; remove it and these files after that |
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
