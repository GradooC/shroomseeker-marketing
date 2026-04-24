# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

Static, single-file marketing site for the ShroomSeeker iOS app. No build system, no package manager, no tests. Everything ships as-is from this directory.

- [index.html](index.html) — the entire landing page (~850 lines): markup, inline Tailwind config, inline styles, and any inline JS.
- [assets/markers/](assets/markers/) — PNG mushroom marker icons used on the page.
- [favicon.svg](favicon.svg) — site favicon.
- Tailwind is loaded via the CDN (`https://cdn.tailwindcss.com`), so utility classes work without a build. The custom theme (brand colors, etc.) is configured inline in `index.html` via `tailwind.config = {...}`.
- Fonts (`Inter`, `Instrument Serif`) come from Google Fonts.

## Local preview

```bash
open index.html
```

No build, no dev server, no install step. Edits to `index.html` are visible on reload.

Note: the README refers to a `landing/` subfolder, but the site currently lives at the repo root — deploy/serve this directory directly.

## Deploy

Any static host (Vercel, Netlify, GitHub Pages) pointed at the repo root with no build command and output dir `.`.

## Editing conventions

- When adding Tailwind classes, keep in mind the brand palette and theme extensions are defined inline near the top of `index.html` — extend them there rather than hardcoding hex values.
- Keep the site single-file; don't introduce a build step, bundler, or framework unless explicitly requested.

## Outstanding launch TODOs (from README)

- Replace the placeholder App Store link (`href="#"`) with the real URL.
- Add `assets/og-image.png` (1200×630) for social previews (already referenced in the `<meta og:image>` tag).
- Swap the CSS phone mockup in the hero for real app screenshots when available.
- Wire up real Privacy / Terms pages.
