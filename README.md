# Modern Renaissance — modernrenaissance.xyz

Personal site for **Jacob Luke Griles** (bio, consulting services, blog, and photo galleries). Static HTML/CSS/JS, no build step. Live at https://modernrenaissance.xyz. Repo: `jlgriles/modern-renaissance-website`.

## Pages

### Core
- **`index.html`** — Homepage. Bio (Who I Am / What I Do / Favourite Resources) and contact links.
- **`services/get-started.html`** — Fractional CMO / consulting services page: pricing packages, service list (SEO, Google Ads, web dev, IT, AI, hosting), Calendly + Airtable booking links.
- **`services/ai-audit.html`** — "Code Review for AI-Shipped Work" — a standalone landing page for the AI-audit service offering, linked from the services page.
- **`portfolio/index.html`** — Project list: Veivos, Hoogah Coffee, ecoloop, Baseman Bros, SNAP Roofing, Property Results, MyNomadCompanion, DJ Lonely Wolf, Farm App.

### Insights (blog)
- **`insights/overview.html`** — Index/landing page for the blog.
- **`insights/motivation/`** — 8 posts (e.g. `4-ways-to-start-today.html`, `finding-your-place.html`, `valuing-contention.html`). Note: contains a duplicate — `what-s-the-value-of-a-new-year copy.html` alongside `what-s-the-value-of-a-new-year.html`.
- **`insights/cob-house/`** — 5 posts on building a cob house.
- **`insights/self-reliance/`** — 3 posts (minimalism, growing food, "the new economy").
- **`insights/general/`** — 2 posts (`hello-world.html`, `understanding-energy.html`).
- **`insights/avocations/`** — 1 post (figure drawing).

### Galleries & standalone pages
- **`cob-house/gallery.html`** — Photo gallery of the cob house build.
- **`travels/photo-map.html`** — Interactive travel map; photos in `travels/photo-locations/` (~50 location images, one per place visited).
- **`artwork/gallery.html`** — Art gallery.
- **`quote-wall.html`** — Collected favorite quotes.
- **`global-information-network.html`** — Standalone project page, largest file in the repo (~1,800 lines).

## Stack & structure

- Static HTML/CSS/JS — no framework, no build tooling (no `package.json`/bundler). Edit HTML/CSS/JS directly.
- Based on the **Photon** template by HTML5 UP (credited in page source comments).
- `assets/sass/` contains the Sass source; `assets/css/` contains the compiled output actually referenced by the HTML pages. There's no visible build script in the repo — if Sass is edited, the compiled CSS needs to be regenerated and committed separately (check for a local Sass compiler/watch setup outside the repo, since none is checked in).
- Multiple `main-style-*.css`/`.js` variants exist for different page layouts (e.g. `main-style-two` for the homepage, `main-blog-general` for services/insights pages) — check which `<link>`/`<script>` tags a given page uses before assuming a shared stylesheet.
- `assets/mini-earth/` — a third-party JS library (with its own `copyright.txt`) that powers the interactive globe on `travels/photo-map.html`.
- Google Analytics (gtag.js) is embedded directly in each page's `<head>` rather than centralized — a sitewide GA change means editing every page.
- `sitemap.xml` is manually maintained (generated via a third-party tool per its header comment) — not auto-generated, so new pages won't appear in it automatically.