# Julian Nicholls — Personal Site

Personal portfolio and resume site focused on geospatial systems, wildfire science, scientific software, simulation, and operational decision support.

## Stack

- Astro + TypeScript
- Static output by default
- Cloudflare Workers static assets for production
- Cloudflare Tunnel optional for live local-device previews

## Local development

```bash
npm install
npm run dev
```

Astro serves the site on `http://localhost:4321`.

## Build

```bash
npm run build
```

The deployable static site is written to `dist/`.

## Cloudflare Workers

Authenticate Wrangler once:

```bash
npx wrangler login
```

Then deploy manually with:

```bash
npm run deploy
```

`wrangler.jsonc` deploys the `dist/` directory as static assets. No Worker runtime code or Astro SSR adapter is required.

For production CI/CD, connect this repository to Cloudflare Workers Builds and use `main` as the production branch. The repository intentionally remains static-first; server-side Worker code can be introduced later only if a real feature needs it.

## Local Cloudflare Tunnel preview

With the Astro dev server running:

```bash
cloudflared tunnel --url http://localhost:4321
```

A named tunnel/custom development hostname can be wired later once the desired domain is chosen.

## Content status

The current copy establishes the narrative and information architecture. Before public launch, add verified screenshots/visuals, final contact links, a downloadable resume, domain metadata, and any sensitive-employer review needed for project material.
