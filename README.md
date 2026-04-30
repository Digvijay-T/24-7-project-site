# 24/7 PROJECT — Web Presence

Static site for [24-7-project.com](https://24-7-project.com).

---

## Structure

```
/
├── index.html              # Main landing page
├── starter.html            # Starter plan product page
├── professional.html       # Professional plan product page
├── enterprise.html         # Enterprise plan product page
├── receptionist.html       # Receptionist add-on page
├── topup-1000.html         # 1,000 minute top-up page
├── topup-5000.html         # 5,000 minute top-up page
├── impressum.html          # Legal notice (Impressum)
├── datenschutz.html        # Privacy policy (DSGVO)
├── eu-ai-act.html          # EU AI Act compliance page
├── ki-kaltakquise.html     # SEO: KI Kaltakquise guide
├── ai-vertrieb-kosten.html # SEO: Cost comparison human vs. AI
├── ki-telefonagent.html    # SEO: How AI voice agents work
├── voice-ai-dsgvo.html     # SEO: Voice AI & DSGVO
├── demo-sales.html         # 3-persona interactive sales demo
├── demo_interactive_nodes.html  # Workflow architecture visualiser
├── integration-matrix.html # Integration tier comparison
├── robots.txt              # Crawler directives — AI bots explicitly allowed
├── sitemap.xml             # 8 indexed URLs submitted to Search Console
├── favicon.svg             # Brand favicon
├── _redirects              # www → non-www redirect rules
└── LICENSE                 # All rights reserved — FSJH LTD
```

---

## Deployment

Pushes to `main` deploy automatically via GitHub Pages. DNS is managed in Cloudflare; the apex CNAME points to `digvijay-t.github.io`.

Custom domain: `24-7-project.com`  
HTTPS: enforced via GitHub Pages  
Build time: ~60 seconds after push

---

## SEO

- Sitemap submitted to Google Search Console
- All pages have canonical tags, meta descriptions, OG/Twitter cards
- SEO content pages have Article schema + FAQ schema where applicable
- Product/checkout pages are `noindex, follow` — excluded from sitemap
- AI crawlers (GPTBot, ClaudeBot, PerplexityBot, Google-Extended) explicitly allowed in robots.txt

---

## Infrastructure (separate from this repo)

| Service | Purpose | Host |
|---|---|---|
| n8n | Automation (12 workflows) | Hetzner VPS |
| Supabase | Database | Ireland (EU) |
| Retell AI | Voice agent engine | EU via API |
| api.24-7-project.com | Webhook endpoint | Hetzner VPS |
| dashboard.24-7-project.com | Client dashboard | Hetzner VPS |
| Stripe | Payments | — |

---

## Legal

© 2026 FSJH LTD. All rights reserved. See [LICENSE](./LICENSE).
