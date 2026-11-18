# mymyo.info — My Myo

Source for **[mymyo.info](https://mymyo.info)**, the professional site of James Maddock —
Clinical Myotherapist (BHSc, Clinical Myotherapy) and Remedial Massage Therapist,
practising at The Urban Alchemist, Carlton North, Melbourne.

Built on the Cloudflare "Astro Blog" starter template, now substantially customised.

## Stack

- [Astro](https://astro.build) (fully prerendered static output)
- Cloudflare Workers (static assets, `astro-blog-starter-template` worker)
- Wrangler for deploys

## Structure

- `src/pages/` — Home, About, Services, Blog, Contact
- `src/content/blog/` — blog posts (Markdown/MDX)
- `src/styles/global.css` — design tokens ("Morning bush light" palette, light + dark
  themes via `.dark` class on `<html>`, `?theme=dark|light` URL param, localStorage,
  `prefers-color-scheme` fallback)
- `src/consts.ts` — site title/description and `BOOKING_URL` (Cliniko online booking
  at The Urban Alchemist)

## Commands

| Command           | Action                                    |
| :---------------- | :---------------------------------------- |
| `npm install`    | Installs dependencies                     |
| `npm run dev`    | Local dev server                          |
| `npm run build`  | Production build to `./dist/`              |
| `npm run preview`| Preview the production build locally      |
| `npm run deploy` | Deploy to Cloudflare (wrangler)           |

## Notes

- Production deploy: pushes to `main` (and manual `npm run deploy` from a machine
  with `CLOUDFLARE_API_TOKEN` set — the dev machine "newbruce" is set up for this).
- Started from
  [cloudflare/templates/astro-blog-starter-template](https://github.com/cloudflare/templates/tree/main/astro-blog-starter-template);
  theme lineage: [Bear Blog](https://github.com/HermanMartinus/bearblog/).
