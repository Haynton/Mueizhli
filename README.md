# Mueizhli

A lightweight, branded landing page that keeps former customers from hitting an error page after the closure of Mueizhli, an artisanal granola and spread brand based in Nantes, France.

**Live:** [www.mueizhli.com](https://www.mueizhli.com)

> The page itself is written in French, since it addresses the brand's former French-speaking customers.

## Context

Mueizhli made organic granola and chocolate-hazelnut spreads for seven years, sold through its own Shopify e-shop. The business and the shop closed in January 2026. Customers with old links, bookmarks or search results would have landed on a broken page, so I built this temporary page to thank them, announce the end of the adventure, and keep the brand image consistent.

## What it does

- Announces the closure with a short, personal message to former customers
- Keeps the original brand identity (palette, logo, product photography)
- Replaces the error page visitors would otherwise see
- Provides a custom 404 page for any other broken URL

## Technical details

- **Stack:** plain HTML and CSS, no framework, no build step
- **Logo:** inline SVG, so it stays sharp at any size and needs no extra request
- **Performance:** WebP images, the hero image preloaded with high fetch priority, the rest lazy loaded
- **SEO and sharing:** meta description, Open Graph and Twitter Card tags so links display properly when shared
- **Accessibility:** `lang` attribute, descriptive `alt` text on images, `aria-label` on the logo link
- **Icons:** full favicon set (16, 32, 192, 512 px, Apple touch icon) and a web app manifest
- **Hosting:** Vercel, with automatic deployment on every push to `main`

## Project structure

```
.
├── assets/
│   ├── css/                  # stylesheet
│   ├── favicon/              # favicons and touch icons
│   └── images/               # product images (WebP)
├── index.html                # landing page
├── 404.html                  # custom error page
├── manifest.webmanifest      # web app manifest
└── .gitignore
```

## Run locally

No installation needed. Clone the repo and open the page in a browser:

```bash
git clone https://github.com/Haynton/Mueizhli.git
cd Mueizhli
open index.html
```

## Deployment

Each push to `main` triggers a new production deployment on Vercel automatically.

## What I learned

- Handling the end of a product's life cycle from the user's side, not only the technical side
- Cleaning up DNS records and reassigning a domain after canceling a Shopify subscription
- Shipping a small, focused static site quickly and keeping it maintainable

## Author

Built by [Anthony Quenet](https://www.anthonyquenet.com) ([@Haynton](https://github.com/Haynton)).
