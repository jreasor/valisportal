# valisportal

Source for [valisportal.com](https://valisportal.com) — static site built with [Astro](https://astro.build).

## Structure

- `src/pages/index.astro` — the single home page
- `src/styles/global.css` — styles (plain CSS, no framework)
- `public/valis_logo.svg` — hand-coded vector recreation of the wordmark (`valis_logo.png` is the original raster, kept for reference)
- `public/favicon.svg` — favicon (striped V from the wordmark geometry)

## Commands

| Command           | Action                                   |
| :---------------- | :--------------------------------------- |
| `npm install`     | Install dependencies                     |
| `npm run dev`     | Dev server at `localhost:4321`           |
| `npm run build`   | Build the production site to `./dist/`   |
| `npm run preview` | Preview the production build locally     |

## Deploying to Cloudflare Pages

The repo is wired to Cloudflare Pages. Settings:

- **Framework preset:** Astro (sets the commands below automatically)
- **Build command:** `npm run build`
- **Build output directory:** `dist`

`.nvmrc` pins Node 22 (Astro requires ≥18.20.8; Cloudflare Pages reads `.nvmrc` automatically).