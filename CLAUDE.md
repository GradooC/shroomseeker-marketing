# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

Static marketing site for the ShroomSeeker iOS app. No build system, no package manager, no tests. Everything ships as-is from the repo root.

- [index.html](index.html) — the landing page: markup, inline Tailwind config, inline styles, and any inline JS.
- [privacy/index.html](privacy/index.html) — Privacy Policy page.
- [support/index.html](support/index.html) — Support page.
- [assets/markers/](assets/markers/) — PNG mushroom marker icons used on the landing.
- [assets/images/](assets/images/) — app screenshots and other imagery.
- [favicon.svg](favicon.svg) — site favicon.
- [CNAME](CNAME) — custom domain (`shroomseeker.org`) for GitHub Pages.

Tailwind is loaded via the CDN (`https://cdn.tailwindcss.com`), so utility classes work without a build. The custom theme (brand colors, etc.) is configured inline in each HTML file via `tailwind.config = {...}`. Fonts (`Inter`, `Instrument Serif`) come from Google Fonts.

## Local preview

```bash
open index.html
```

No build, no dev server, no install step. Edits to `index.html` are visible on reload.

Note: the README refers to a `landing/` subfolder, but the site currently lives at the repo root — deploy/serve this directory directly.

## Deploy

The site is deployed via **GitHub Pages** with a custom domain (`shroomseeker.org`, see [CNAME](CNAME)). Pushes to `main` go live automatically. Any other static host (Vercel, Netlify) also works pointed at the repo root with no build command.

## Editing conventions

- When adding Tailwind classes, keep in mind the brand palette and theme extensions are defined inline near the top of each HTML file — extend them there rather than hardcoding hex values. If you change the theme on the landing, mirror it in `privacy/` and `support/` so the subpages stay visually consistent.
- Keep the site build-free; don't introduce a bundler or framework unless explicitly requested.

## Outstanding launch TODOs (from README)

- Replace the placeholder App Store link (`href="#"`) with the real URL.
- Add `assets/og-image.png` (1200×630) for social previews (already referenced in the `<meta og:image>` tag).
