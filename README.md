<div align="center">

# Patsa Lohith — Developer Portfolio

An editorial, single-page portfolio for a Computer Science student: three switchable visual themes,
project case studies with image previews, and direct contact channels — built in one HTML document
with no framework and no build step.

[**Live site**](https://portfolio-lohith-1e2a.vercel.app) &nbsp;·&nbsp; [Report an issue](https://github.com/lohith-hash/portfolio/issues)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![No dependencies](https://img.shields.io/badge/dependencies-0-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

</div>

---

## Overview

A single `index.html` holds the markup, the styles and the content model for the whole site. Projects
are defined as a JavaScript data array, so adding a case study means adding one object — not copying
a block of markup. Project images open in a keyboard-accessible lightbox with a thumbnail strip.

## Features

- **Three visual themes** — Atelier, Noir and Cobalt, switched from the header, applied through CSS custom properties and remembered in `localStorage`.
- **Project case studies** — three projects, each with a summary, technology list, headline stats, a feature breakdown, key facts and an image preview set.
- **Image lightbox** — full-screen preview with previous/next navigation, thumbnail strip, `Esc` to close and focus handling.
- **Scroll experience** — reading-progress bar, scroll-triggered reveals, an active-section navigation indicator and a word marquee.
- **Live IST clock** in the header, formatted with `Intl.DateTimeFormat` for `Asia/Kolkata`.
- **Contact channels** — email, WhatsApp (with a pre-written formal message), Instagram and LinkedIn, all configured in one `CONTACT` object.
- **Copy profile summary** — one-click copy of a short recruiter-friendly bio.
- **Responsive and accessible** — mobile drawer navigation, skip-to-content link, `aria` state on toggles, reduced-motion friendly reveals.
- **Optimised assets** — preview images are stored as separate files under `assets/projects/` and lazy-loaded, instead of being embedded in the document.

## Tech stack

HTML5 · CSS3 (custom properties, grid, clamp-based fluid type) · vanilla JavaScript · zero runtime dependencies. Fonts are loaded from jsDelivr (Fraunces, Inter, JetBrains Mono via Fontsource).

## Project structure

```
portfolio/
├── index.html            # markup + styles + content model for the whole site
└── assets/
    └── projects/         # project preview images (referenced from the PROJECTS array)
```

## Run locally

```bash
python3 -m http.server 5500
# then open http://localhost:5500
```

Any static file server works; there is nothing to install or compile.

## Customisation

| What | Where |
|------|-------|
| Email, WhatsApp number, Instagram, LinkedIn | `const CONTACT = { … }` near the top of the script in `index.html` |
| Pre-written WhatsApp / email messages | `const MSG = { … }` directly below `CONTACT` |
| Projects (summary, stack, stats, features, images) | `const PROJECTS = [ … ]` |
| Themes and colours | `const THEMES` plus the `[data-theme]` custom-property blocks |
| Marquee keywords | `const MARQUEE_WORDS` |

## Notes

- Project preview images live in `assets/projects/` and are referenced by relative path, so keep the folder structure when deploying.
- Fonts are fetched from a public CDN; offline or air-gapped hosting needs the fonts vendored locally.

## License

Released under the [MIT License](LICENSE) © 2026 Patsa Lohith.
