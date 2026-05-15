# FlowDesk — Landing Page

A fully responsive, single-page marketing site for **FlowDesk**, a fictional SaaS productivity tool. Built with Bootstrap 5 and custom CSS, no frameworks or build tools required.

---

## Live Preview

Open (https://ezran4545.github.io/Landing-page/) directly in any modern browser — no server needed.

---

## Project Structure

```
flowdesk/
├── landing-page.html   # All-in-one HTML, CSS, and JS
└── README.md
```

Everything lives in a single file. Styles are in a `<style>` block in `<head>`, scripts are at the bottom of `<body>`.

---

## Tech Stack

| Layer      | Technology                        |
|------------|-----------------------------------|
| Framework  | Bootstrap 5.3.3 (CDN)             |
| Fonts      | Google Fonts — inter + DM Sans     |
| JavaScript | Vanilla JS (no jQuery)            |
| Hosting    | Any static host or open locally   |

No npm, no bundler, no build step.

---

## Sections

| Section        | Description                                              |
|----------------|----------------------------------------------------------|
| **Navbar**     | Sticky top bar with logo, nav links, CTA; mobile-ready  |
| **Hero**       | Headline, subtext, dual CTAs, fake dashboard mockup      |
| **Logos**      | Social proof strip with trusted brand names              |
| **Features**   | 6-card grid covering core product capabilities           |
| **Stats**      | Dark band with 4 key metrics                             |
| **Pricing**    | 3-tier cards — Starter (free), Pro (featured), Enterprise|
| **Testimonials** | 3 customer quotes with avatars                         |
| **CTA**        | Email capture form with dark branded box                 |
| **Footer**     | 4-column links + brand tagline                           |

---

## Bootstrap 5 Features Used

- **Responsive grid** — `col-md-6 col-lg-4` for adaptive layouts at every breakpoint
- **Navbar collapse** — mobile hamburger menu via `data-bs-toggle="collapse"`
- **Utility classes** — `d-flex`, `gap-*`, `text-center`, `align-items-center`, `ms-auto`, etc.
- **Breakpoint helpers** — `col-6 col-lg-3` for the stats section, `offset-lg-*` for spacing
- **Bootstrap JS bundle** — included via CDN for the mobile menu toggle

---

## Custom Design System

Defined as CSS variables at the top of the `<style>` block:

```css
:root {
  --brand:     #0A2342;   /* Deep navy — primary color          */
  --accent:    #F4572D;   /* Burnt orange — CTAs, highlights    */
  --accent2:   #FFD166;   /* Warm yellow — stat numbers         */
  --light-bg:  #F8F5F0;   /* Off-white — page background        */
  --text-muted:#5a6a82;   /* Muted navy — body/secondary text   */
  --border:    #e4ddd4;   /* Warm gray — card borders           */
}
```

To retheme the page, update these six values.

---

## Typography

Two fonts loaded from Google Fonts:

- **inter** (weights 400–800) — headings, logo, buttons; tight tracked display style
- **DM Sans** (300/400/500) — body text; clean and readable at small sizes

---

## JavaScript Behaviour

Two lightweight scripts at the bottom of `<body>`:

**Smooth scroll** — all `<a href="#...">` anchor links scroll smoothly to their target section.

**Scroll-triggered fade-in** — feature cards, pricing cards, and testimonials animate in (`opacity` + `translateY`) as they enter the viewport, using `IntersectionObserver`.

No external JS libraries beyond the Bootstrap bundle.

---

## Customisation Guide

### Change the brand name
Search and replace `FlowDesk` throughout the file.

### Change colours
Edit the CSS variables in `:root` — the entire page will update.

### Add or remove a pricing tier
Copy one `.pricing-card` block inside the pricing section. Adjust the `.col-*` classes on all three cards to maintain balance (e.g. switch to `col-lg-3` for four tiers).

### Replace the hero mockup
The dashboard inside `.hero-dashboard` is built with plain `div`s and inline styles. Replace or restyle it, or swap it for a real screenshot using an `<img>` tag inside `.hero-img-card`.

### Wire up the email form
The CTA email input is plain HTML with no backend. To make it functional, wrap it in a form and point it at any form service (Formspree, Mailchimp embed, etc.).

---

## Deployment

The file is self-contained and has no build step.

**Netlify / Vercel drop** — drag the file (or the folder) into the Netlify dashboard or `vercel --prod`.

**GitHub Pages** — push to a repo, enable Pages from the root, and it serves immediately.

**Any static CDN** — upload `landing-page.html` to S3, Cloudflare Pages, or similar.

---

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Bootstrap 5 does not support IE 11.

---

## License

This project is a demo template. Free to use and adapt for any purpose.
