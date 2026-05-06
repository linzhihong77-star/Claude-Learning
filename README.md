# Belle Lumière — Bridal Photography Booking Website

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Google Fonts](https://img.shields.io/badge/Google%20Fonts-4285F4?style=for-the-badge&logo=google&logoColor=white)
![FormSubmit](https://img.shields.io/badge/FormSubmit-FF6B6B?style=for-the-badge&logo=gmail&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=for-the-badge&logo=github&logoColor=white)

## About the Project

Belle Lumière is a single-page bridal photography studio website that lets couples discover packages, browse a curated gallery, and submit a booking enquiry — all without leaving the page. Built with zero dependencies (pure HTML, CSS, and vanilla JavaScript), it is fast, lightweight, and trivial to deploy anywhere.

The booking form posts as JSON to [FormSubmit](https://formsubmit.co/) and reveals an inline success message on submission, giving visitors a smooth, app-like experience with no backend code required.

## Screenshot

![Site Screenshot](screenshot.png)

## Live Site

[https://linzhihong77-star.github.io/Claude-Learning/](https://linzhihong77-star.github.io/Claude-Learning/)

## File Structure

```
Claude-Learning/
├── index.html                   # Entire site — HTML, CSS, and JS inline
├── screenshot.png               # Full-page site screenshot
├── README.md                    # This file
├── CLAUDE.md                    # Guidance for Claude Code AI assistant
├── .nojekyll                    # Bypasses Jekyll on GitHub Pages
└── .github/
    └── workflows/
        └── deploy.yml           # GitHub Actions workflow → GitHub Pages
```

## Tech Stack

| Layer | Details |
|---|---|
| Markup | Semantic HTML5 |
| Styling | CSS custom properties, Grid, Flexbox, `@media` breakpoints at 600 px & 980 px |
| Scripting | Vanilla JS (`fetch`, `scrollIntoView`, scroll listener) |
| Fonts | Google Fonts — Playfair Display + Lato |
| Images | Unsplash CDN |
| Form backend | FormSubmit AJAX (JSON POST) |
| Hosting | GitHub Pages via GitHub Actions |

## Features

- **Hero** — Full-viewport banner with blush & gold overlay and a call-to-action
- **About** — Two-column photographer bio section
- **Packages** — Three tiers (Elopement · Full Day · Premium Collection) with one-click booking pre-fill
- **Gallery** — CSS Grid mosaic of six Unsplash bridal images with hover effects
- **Booking Form** — Posts as JSON to FormSubmit; hides form and reveals success message on submit
- **Contact** — Email, phone, Instagram, and Google Maps placeholder
- **Responsive** — Hamburger menu on mobile, fluid typography with `clamp()`

## How to Use

### View the live site

[https://linzhihong77-star.github.io/Claude-Learning/](https://linzhihong77-star.github.io/Claude-Learning/)

### Run locally

No install or build step needed:

```bash
python -m http.server 8080
```

Then open [http://localhost:8080/index.html](http://localhost:8080/index.html).

### Booking form setup

The form posts to `https://formsubmit.co/ajax/linzhihong77@gmail.com`. The **first** submission triggers a one-time activation email — click the link in that email before any bookings will be delivered.

## Colour Palette

| Token | Hex | Usage |
|---|---|---|
| Blush light | `#fce8ed` | Background tints |
| Blush mid | `#e8a0ae` | Borders, hover states |
| Blush dark | `#c07688` | Darker accents |
| Gold | `#c9a84c` | CTAs, dividers, icons |
| White | `#fffaf9` | Page background |
| Text dark | `#3a2e2e` | Body copy |
