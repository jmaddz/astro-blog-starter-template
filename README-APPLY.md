# mymyo.info first-pass build (My Myo)

These files replace or add to the Astro Blog starter in
github.com/jmaddz/astro-blog-starter-template.

## Files (repo-relative paths)

- `astro.config.mjs` — replaces existing; sets site URL to https://mymyo.info
- `src/consts.ts` — replaces existing; My Myo title/description, BOOKING_URL
- `src/styles/global.css` — replaces existing; "Morning bush light" design tokens,
  light + dark themes (.dark class on <html>, ?theme=dark|light URL param)
- `src/components/BaseHead.astro` — replaces existing; adds anti-flash theme script
- `src/components/Header.astro` — replaces existing; nav (Home/About/Services/Blog/Contact),
  theme toggle, "Book now" link
- `src/components/Footer.astro` — replaces existing
- `src/pages/index.astro` — replaces existing; positioning-led homepage
- `src/pages/about.astro` — replaces existing; story + philosophy
- `src/pages/services.astro` — NEW page
- `src/pages/contact.astro` — NEW page

## Apply (from your local clone)

    # copy the files over, then:
    npm install
    npm run build      # verify it builds
    git add -A && git commit -m "My Myo first-pass build: identity, palette, pages"
    git push
    npm run deploy     # wrangler deploy to the Cloudflare Worker

## Notes

- Booking links point to https://massage.melbourne (homepage); swap
  BOOKING_URL in src/consts.ts if you want the direct booking path instead.
- Theme system matches massage.melbourne: .dark class + ?theme= URL param,
  stored in localStorage, falls back to prefers-color-scheme.
- Dark-mode contrast spot-check URLs after deploy:
  https://mymyo.info/?theme=light and https://mymyo.info/?theme=dark
