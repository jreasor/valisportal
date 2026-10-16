# valisportal

Source for [valisportal.com](https://valisportal.com) — static site built with [Astro](https://astro.build).

## Structure

- `src/pages/index.astro` — the single home page
- `src/styles/global.css` — styles (plain CSS, no framework)
- `public/valis_logo.svg` — vector wordmark traced from `valis_logo_transparent.png` (pixel-exact vs the PNG at 1:1); the asset the site serves
- `public/valis_logo_transparent.png` — the transparent raster wordmark (trace source for the SVG)
- `public/favicon.svg` — favicon (striped V from the wordmark geometry)

## Commands

| Command           | Action                                   |
| :---------------- | :--------------------------------------- |
| `npm install`     | Install dependencies                     |
| `npm run dev`     | Dev server at `localhost:4321`           |
| `npm run build`   | Build the production site to `./dist/`   |
| `npm run preview` | Preview the production build locally     |

## Deploying to Cloudflare

The repo is wired to Cloudflare (Workers static assets, git-connected). Settings:

- **Build command:** `npm run build`
- **Deploy command:** `npx wrangler deploy`
- `wrangler.jsonc` points the Worker at `dist/`

`.nvmrc` pins Node 22 (Astro requires ≥18.20.8; Cloudflare Pages reads `.nvmrc` automatically).