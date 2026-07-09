# Guildford Mina Pizzeria — Website

[![Live Demo](https://img.shields.io/badge/live-demo-C1440E?style=flat-square)](https://mina-pizzeria.netlify.app/)
[![Built with GSAP](https://img.shields.io/badge/built%20with-GSAP-88CE02?style=flat-square)](https://gsap.com/)
[![Smooth scroll: Lenis](https://img.shields.io/badge/smooth%20scroll-Lenis-000000?style=flat-square)](https://github.com/darkroomengineering/lenis)

**Live site:** https://mina-pizzeria.netlify.app/

A single-page website for **Guildford Mina Pizzeria**, 316 Railway Terrace, Guildford NSW 2161 — open 24 hours, 7 days a week. Static HTML/CSS/JS (no build step, no framework), with GSAP + Lenis for scroll animations and smooth scrolling.

<!--
  TODO: add a screenshot or short GIF of the site here, e.g.:
  ![Site preview](images/preview.gif)
  A screen recording of the hero entrance + scroll reveals will sell this repo far better than any text description.
-->

---

## Features

- Full menu with tabbed categories (Pizza, Lebanese/Manoush, BBQ Kaak, Burgers, Dessert Pizza, Drinks)
- Special deals section
- Photo gallery of real dishes and the shop interior
- About section
- Real, attributed Google reviews
- Visit/location section with embedded Google Map and opening hours
- Sticky header with mobile hamburger menu
- Animated scroll reveals, parallax, magnetic buttons, animated stat counters
- Fully responsive (mobile breakpoint at 900px)
- Respects `prefers-reduced-motion`
- Real ordering link (NextOrder) and click-to-call phone number

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

## Known Limitations

- The Google review snapshot was pulled at a point in time — refresh periodically so ratings/counts stay accurate
- No contact form or newsletter signup — phone, click-to-call, and the NextOrder link are the only conversion paths by design

## License / Ownership

The **code** (HTML/CSS/JS structure and animation techniques) is free to reference or reuse as inspiration for your own projects. The **content** — copy, photos, and business information (menu, address, phone, reviews) — belongs to Guildford Mina Pizzeria and is not licensed for reuse; swap it out before using this as a template.
