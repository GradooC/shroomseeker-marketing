# ShroomSeeker Landing

Static, single-file marketing site for the ShroomSeeker iOS app.

## Local preview

```bash
open landing/index.html
```

No build step — HTML + Tailwind via CDN + Google Fonts.

## Deploy

- **Vercel / Netlify:** point the project at the `landing/` folder, no build command, output dir `.`.
- **GitHub Pages:** serve `landing/` from a branch.
- **Any static host:** upload the contents of `landing/`.

## TODO before launch

- Replace placeholder App Store link (`href="#"`) with the real URL.
- Add `assets/og-image.png` (1200×630) for social previews.
- Replace the CSS phone mockup in the hero with real app screenshots when available.
- Wire up real Privacy / Terms pages.
