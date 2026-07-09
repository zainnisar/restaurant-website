# Guildford Mina Pizzeria — Website

**Live site:** https://mina-pizzeria.netlify.app/

A single-page marketing site for **Guildford Mina Pizzeria**, 316 Railway Terrace, Guildford NSW 2161 — open 24 hours, 7 days a week.

Built as a static HTML/CSS/JS site (no build step, no framework) with a premium, "Awwwards-style" motion layer on top: a branded preloader, GSAP-driven scroll reveals, split-text headline animation, subtle parallax, magnetic buttons, and buttery-smooth scrolling via Lenis.

---

## Features

- Full menu with tabbed categories (Pizza, Lebanese/Manoush, BBQ Kaak, Burgers, Dessert Pizza, Drinks)
- Special deals section
- Photo gallery of real dishes and the shop interior
- About section
- Real, attributed Google reviews (sourced from the business's actual Google listing)
- Visit/location section with embedded Google Map and opening hours
- Sticky header with mobile hamburger menu
- Animated preloader, scroll-triggered reveals, parallax, magnetic buttons, animated stat counters
- Fully responsive (mobile breakpoint at 900px)
- Respects `prefers-reduced-motion` — all animation is skipped/instant for users who request reduced motion
- Real ordering link (NextOrder) and click-to-call phone number

## Tech Stack

- **HTML5 / CSS3** — no preprocessor, no build step, everything in `index.html`
- **Vanilla JavaScript** — mobile menu, tab switching, GSAP orchestration
- **[GSAP](https://gsap.com/) + ScrollTrigger** — all entrance/scroll animation timelines
- **[Lenis](https://github.com/darkroomengineering/lenis)** — smooth scrolling
- **[SplitType](https://github.com/lukePeavey/SplitType)** — splits headings into words/lines for the mask-reveal effect
- Libraries are loaded from CDN (cdnjs / jsDelivr) — **an internet connection is required** for the motion layer, fonts, and the Google Maps embed. The page still renders and is fully readable/usable without JS or without internet (progressive enhancement — everything defaults to visible/static).

## File Structure

```
guildford-mina-pizzeria-website/
├── index.html          # the entire site — markup, CSS, and JS
├── images/
│   ├── hero-banner.jpg       # hero background photo
│   ├── logo-icon.png         # chef-hat logo mark (header + preloader)
│   ├── about-photo.jpg       # About section photo
│   └── gallery-*.jpg         # 7 gallery photos
├── robots.txt
├── sitemap.xml
├── .gitignore
└── README.md
```

## Running Locally

No build step required. Either:

- Double-click `index.html` to open it directly in a browser, **or**
- Serve it with any static server for a more production-like experience (recommended, since some browsers restrict certain features on `file://` URLs):

  ```bash
  npx serve .
  # or
  python -m http.server 8080
  ```

  then visit `http://localhost:8080`.

## Deployment

### Option A — GitHub Pages

1. Push this folder to a GitHub repository (see [Uploading to GitHub](#uploading-to-github) below).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save. Your site will be live at `https://<username>.github.io/<repo-name>/`.
5. **Custom domain:** in the same Pages settings, enter your domain under **Custom domain** — this creates a `CNAME` file in the repo automatically. Then add the DNS records GitHub shows you (an `A`/`ALIAS` record at your registrar pointing to GitHub's IPs, or a `CNAME` record if using a subdomain).

### Option B — Netlify / Vercel / Cloudflare Pages

Drag-and-drop the whole folder onto Netlify, or connect the GitHub repo — no build command needed, publish directory is the repo root.

### Before going live, update these placeholders

Search the project for `YOUR-DOMAIN-HERE.com` and replace every instance with the real domain once you know it:

- `index.html` — `<link rel="canonical">`, `og:url`, `og:image`, and the JSON-LD `Restaurant` schema block near the top of `<head>`
- `robots.txt` — the `Sitemap:` line
- `sitemap.xml` — the `<loc>` value

## Uploading to GitHub

This folder is ready to become a repo. From inside `guildford-mina-pizzeria-website/`:

```bash
git init
git add .
git commit -m "Initial commit: Guildford Mina Pizzeria website"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

> This project was prepared with the structure ready to commit, but no `git init` or push has been run automatically — run the commands above yourself when you're ready.

## Updating Content

Everything lives in `index.html`. No CMS, no data files — content is plain HTML you edit directly:

| To change...              | Look for...                                            |
|----------------------------|---------------------------------------------------------|
| Menu items / prices        | `<!-- MENU -->` section, `.menu-card` blocks             |
| Special deals               | `<!-- DEALS -->` section, `.deal-card` blocks            |
| Opening hours                | `<!-- VISIT -->` section, `.hours-table`, and the `.top-bar` banner at the top of `<body>` |
| Phone number / address     | Search for `+61298921448` and `316 Railway Terrace` — used in several places (header, footer, Visit section, JSON-LD) |
| Gallery photos                | `<!-- GALLERY -->` section — swap the `images/gallery-*.jpg` files and update `alt` text |
| Reviews                        | `<!-- REVIEWS -->` section, `.t-card` blocks                |
| Ordering link               | Search for `nextorder.com` — appears on the "Order Now"/"Order Online" buttons |

## Content & Data Sources

- Menu, address, phone, logo, and several photos were sourced from the business's previous Squarespace website.
- Reviews are real, attributed Google reviews (mirrored via restaurantguru.com, which displays actual Google-sourced reviews with reviewer names and ratings) — chosen for having concrete, specific details rather than generic praise.
- Additional food photography sourced from the business's Uber Eats listing.
- Opening hours (24/7) were confirmed as current and intentionally kept, overriding the shorter hours shown on the old website.

## Known Limitations / TODO

- [x] Replace `YOUR-DOMAIN-HERE.com` placeholders — now live at `mina-pizzeria.netlify.app`
- [ ] The Google review snapshot was pulled at a point in time — refresh periodically so ratings/counts stay accurate
- [ ] GSAP, Lenis, SplitType, and Google Fonts load from CDN — if offline-first support is ever needed, these would need to be self-hosted
- [ ] No contact form or newsletter signup — phone, WhatsApp-free click-to-call, and the NextOrder link are the only conversion paths by design

## License / Ownership

All content (copy, photos, business information) belongs to Guildford Mina Pizzeria. This repository contains the website source only — it is not licensed for reuse as a template without permission.

## Contact

**Guildford Mina Pizzeria**
316 Railway Terrace, Guildford NSW 2161
(02) 9892 1448
[Facebook](https://www.facebook.com/guildford.mina/) · [Instagram](https://www.instagram.com/guildford_mina/)
