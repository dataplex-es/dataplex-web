# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static marketing website for **Dataplex** (dataplex.es), a Spanish data consulting and AI firm. The entire site lives in a single `index.html` file — no build tools, no framework, no package manager.

## Development

**No build step required.** Open `index.html` directly in a browser or use any local HTTP server:

```bash
# Python
python3 -m http.server 8000

# Node (if available)
npx serve .
```

**Deployment:** Push to `main` on GitHub and GitHub Pages auto-deploys to `dataplex.es` (configured via the `CNAME` file).

## Architecture

Everything is self-contained in `index.html` (~1000 lines), structured as:

- **Inline `<style>`** — all CSS, including CSS custom properties (design tokens), responsive breakpoints (`900px`, `600px`), and keyframe animations.
- **Semantic HTML sections** — `#inicio`, `#servicios`, `#enfoque`, `#contacto` — these IDs are referenced by the nav and the Intersection Observer.
- **Inline `<script>`** at the bottom — two behaviours:
  1. Intersection Observer that highlights the active nav link as sections scroll into view and adds a border to the nav on scroll.
  2. Scroll-triggered fade-in for `.fade-in` elements.

### Design tokens (CSS custom properties on `:root`)

| Variable | Value | Role |
|---|---|---|
| `--bg` | `#0a0a0f` | Page background |
| `--accent` | `#00aaff` | Primary accent (cyan) |
| `--text` | `#d6daea` | Body text |
| `--surface` / `--surface-2` | `#0d0d15` / `#111118` | Card backgrounds |

### Fonts (Google Fonts)
- **Syne** — display/headings
- **Space Mono** — monospace labels
- **Barlow Condensed** — condensed headings

## Known Incomplete Item

The contact form posts to Formspree but the form ID is a placeholder:

```html
<form action="https://formspree.io/f/XXXXXXXX" method="POST">
```

Replace `XXXXXXXX` with a real Formspree form ID to make submissions work.
