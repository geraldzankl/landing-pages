# Kickscale Proposal Resource Hub

Static bilingual companion website for Kickscale proposals.

## Structure
- `/`, `/en/`, `/de/`: resource overview
- `/en/onboarding/`, `/de/onboarding/`: 90-day implementation
- `/en/support/`, `/de/support/`: Business Support & Customer Success
- `/onboarding/`, `/support/`: English redirects
- Customer stories, legal/trust and Help Center link to their existing Kickscale properties.

## Hosting and custom domain
This repository is intended to publish via GitHub Pages with custom domain `kickscale.si` (see `CNAME`). The repo alone does **not** configure the domain DNS or automatically activate GitHub Pages. In GitHub repository Settings > Pages, set **Build and deployment: GitHub Actions**. Point the apex domain's DNS at GitHub Pages and verify the domain per GitHub's documentation; enable HTTPS. The deploy workflow is in `.github/workflows/deploy.yml`. Do not send proposal links until live URLs return HTTP 200.

## Search engine exclusion
Every HTML page includes `<meta name="robots" content="noindex, nofollow, noarchive, nosnippet">`. `_headers` provides an X-Robots-Tag directive on hosts supporting that file. The `robots.txt` intentionally **allows crawlers** so they can see the HTML noindex directive; using Disallow can prevent noindex discovery. No sitemap is published. Search-engine exclusion is not password protection and cannot guarantee that URLs or repository files remain private. For sensitive proposals, configure HTTP authentication / access control in front of the website and consider a private repository.

## Commercial accuracy
Support response times shown are **proposed** Business Support SLA targets, not a statement that a standard Kickscale contract currently guarantees them. Customer-specific signed SLA/order form controls. Phone number is the company contact listed on the public Kickscale website; verify it routes to the appropriate support team before promising phone incident response. The included onboarding quantities and custom work must be agreed in the Order Form / SOW.

## Maintenance
Plain static HTML/CSS. Pages can be edited directly; no build dependencies.