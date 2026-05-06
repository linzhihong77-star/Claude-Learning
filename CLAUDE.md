# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Local Development

Serve the site with Python's built-in HTTP server (Python 3 is available):

```bash
python -m http.server 8080
```

Then open http://localhost:8080/index.html. No build step or install is required — the project is a single self-contained file.

## Project Structure

Everything lives in **`index.html`** — HTML, CSS (`<style>`), and JS (`<script>`) are all inline. There is no bundler, framework, or external dependency beyond two Google Fonts families loaded via CDN.

## Architecture Overview

### Styling
CSS custom properties (defined in `:root`) drive the entire color palette and spacing. All responsive breakpoints are handled with `@media` queries inside the same `<style>` block (breakpoints at 600 px and 980 px).

| Token | Purpose |
|---|---|
| `--blush-light/mid/dark` | Background tints, borders, hover states |
| `--gold / --gold-dark` | Accent color for CTAs, dividers, icons |
| `--section-pad` | Uniform vertical/horizontal padding across sections |

### JavaScript (inline `<script>`)
Four independent behaviors, no framework:
- **Sticky nav**: `scroll` listener toggles `.scrolled` class on `<nav>` past 80 px
- **Hamburger menu**: toggles `.open` class on `<ul.nav-links>` for mobile drawer
- **Package pre-select**: `selectPackage(name)` sets `<select#f-package>` value and smooth-scrolls to `#booking`
- **Form submit**: `fetch` POST to `https://formsubmit.co/ajax/linzhihong77@gmail.com` with `Content-Type: application/json`; on success hides the form and reveals `#booking-success`

### Form / FormSubmit Integration
- Endpoint: `https://formsubmit.co/ajax/linzhihong77@gmail.com`
- Payload is plain JSON (not `FormData`). The `_subject` key sets the email subject line.
- **First submission** triggers a one-time activation email to the recipient address — that email must be clicked before any subsequent submissions are delivered.

### Images
All images are sourced from Unsplash (`images.unsplash.com`). They require an internet connection and are not bundled locally.
