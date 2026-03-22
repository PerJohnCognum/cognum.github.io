# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static GitHub Pages site for Cognum AS (Norwegian VC/investment firm). Pure HTML5 + embedded CSS — no build tools, no framework, no dependencies.

## Development

**Run locally**: Open `index.html` in a browser directly, or use any static file server:
```
python3 -m http.server 8000
```

**Deploy**: Push to `main` branch — GitHub Pages serves automatically. `.nojekyll` disables Jekyll processing so HTML is served as-is.

## Architecture

Single file: `index.html` contains all markup and styles inline. `assets/` holds images (logo, hero, favicons).

Structure within `index.html`:
- Header: logo overlaid on hero image (`assets/hero.jpg`)
- Main content: investment focus text + founder bio, centered at max-width 680px
- Portfolio grid: responsive `auto-fit` CSS grid of 12 company links
- Footer: copyright + org number

Mobile breakpoint at 600px. No JavaScript.

## Content Updates

- Portfolio companies: edit the grid section in `index.html`; each item is an `<a>` tag with company name and URL
- Bio/text: edit directly in the `<main>` section
- Hero image: replace `assets/hero.jpg`
- Logo: replace `assets/cognum-logo.png`
