# Belle Lumière — Bridal Photography Booking Website

A single-page bridal photography studio website built with pure HTML, CSS, and JavaScript (no frameworks, no build step).

## Live Preview

Open `index.html` directly in a browser, or serve it locally:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080/index.html`.

## Features

- **Hero** — Full-viewport banner with blush & gold overlay and a call-to-action
- **About** — Two-column photographer bio section
- **Packages** — Three tiers (Elopement · Full Day · Premium Collection) with one-click booking pre-fill
- **Gallery** — CSS Grid mosaic of six Unsplash bridal images with hover effects
- **Booking Form** — Full Name, Email, Phone, Date, Time, Package, Location, Guests, Message — posts as JSON to [FormSubmit](https://formsubmit.co/) and shows an inline success message
- **Contact** — Email, phone, Instagram, and Google Maps placeholder
- **Responsive** — Breakpoints at 600 px and 980 px; hamburger menu on mobile

## Tech Stack

| Layer | Details |
|---|---|
| Markup | Semantic HTML5 |
| Styling | CSS custom properties, Grid, Flexbox |
| Scripting | Vanilla JS (`fetch`, `scrollIntoView`) |
| Fonts | Google Fonts — Playfair Display + Lato |
| Images | Unsplash CDN |
| Form backend | FormSubmit AJAX (JSON POST) |

## Project Structure

```
index.html   ← entire site (HTML + CSS + JS inline)
CLAUDE.md    ← guidance for Claude Code AI assistant
README.md    ← this file
```

## Colour Palette

| Token | Hex |
|---|---|
| Blush light | `#fce8ed` |
| Blush mid | `#e8a0ae` |
| Blush dark | `#c07688` |
| Gold | `#c9a84c` |
| White | `#fffaf9` |
| Text dark | `#3a2e2e` |

## Form Setup

The booking form posts to `https://formsubmit.co/ajax/linzhihong77@gmail.com`. The first submission triggers a one-time activation email — click the link in that email to start receiving bookings.
