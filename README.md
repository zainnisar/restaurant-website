# Guildford Mina Pizzeria — Website

**Live site:** https://mina-pizzeria.netlify.app/

A single-page website for **Guildford Mina Pizzeria**, 316 Railway Terrace, Guildford NSW 2161 — open 24 hours, 7 days a week. Static HTML/CSS/JS (no build step, no framework), with GSAP + Lenis for scroll animations and smooth scrolling.

---

## Running Locally

No build step required. Either:

- Double-click `index.html` to open it directly in a browser, **or**
- Serve it with a static server (some browser features are restricted on `file://` URLs):

  ```bash
  npx serve .
  # or
  python -m http.server 8080
  ```

  then visit `http://localhost:8080`.

## Deployment

Hosted on **Netlify** at the live URL above. Push to `main` on GitHub, then redeploy on Netlify (or connect the repo in Netlify for auto-deploy on every push).

## Updating Content

Everything lives in `index.html`. No CMS, no data files — content is plain HTML you edit directly:

| To change...           | Look for...                                                                         |
|-------------------------|--------------------------------------------------------------------------------------|
| Menu items / prices     | `<!-- MENU -->` section, `.menu-card` blocks                                        |
| Special deals           | `<!-- DEALS -->` section, `.deal-card` blocks                                       |
| Opening hours           | `<!-- VISIT -->` section, `.hours-table`, and the `.top-bar` banner at the top of `<body>` |
| Phone number / address  | Search for `+61298921448` and `316 Railway Terrace` — used in several places (header, footer, Visit section, JSON-LD) |
| Gallery photos           | `<!-- GALLERY -->` section — swap the `images/gallery-*.jpg` files and update `alt` text |
| Reviews                  | `<!-- REVIEWS -->` section, `.t-card` blocks                                        |
| Ordering link            | Search for `nextorder.com` — appears on the "Order Now"/"Order Online" buttons      |

## File Structure

```
guildford-mina-pizzeria-website/
├── index.html          # the entire site — markup, CSS, and JS
├── images/
├── robots.txt
├── sitemap.xml
├── .gitignore
└── README.md
```

## Known Limitations / TODO

- [ ] The Google review snapshot was pulled at a point in time — refresh periodically so ratings/counts stay accurate
- [ ] No contact form or newsletter signup — phone, click-to-call, and the NextOrder link are the only conversion paths by design

## License / Ownership

All content (copy, photos, business information) belongs to Guildford Mina Pizzeria. This repository contains the website source only — it is not licensed for reuse as a template without permission.
