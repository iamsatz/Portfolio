# Sateesh Kumar L — Portfolio

Static, self-contained portfolio site (no build step). Deployed on Vercel from the repo root.

## Stack & structure
- Plain HTML + CSS. No framework, no build, no dependencies. Served as static files.
- `index.html` — home: S1 hero + S2 sections (Case Studies, Selected Projects, Explorations).
- `case-studies/<slug>/index.html` — 3 deep case studies (`assets/styles/case-studies.css`).
- `works/<slug>/index.html` + `works/index.html` — 17 work detail pages + listing (`assets/styles/site.css`).
- `explorations/<slug>/index.html` — 6 explorations incl. Bhor (`assets/styles/site.css`).
- `assets/css/styles.css` — home design system (tokens, BEM). `assets/styles/site.css` + `case-studies.css` — inner pages.

## Conventions
- Typeface: **Proza Libre** everywhere; the "Sateesh" wordmark is **Dancing Script**.
- Palette: warm cream `#F4F1EA` + ink `#211C17` + smartbeans-style pastel accents (coral / yellow / lime / sky).
- **Light mode only** (dark mode removed). **No em dashes** in copy (human tone).
- Inner-page content centered to 1080px to match the home gutters.
- Case studies use a per-study accent: Aampe = coral, Rhythm = sky, First Responder = lime.
- Local preview: `.claude/launch.json` → `portfolio` serves the root on :4000.

## Active Work
- [x] Rebuild the portfolio from the Sketch design (home, case studies, works, explorations).
- [x] Integrate 6 explorations (incl. Bhor weather macOS app) with category tags.
- [x] Promote the new site to the repo root and deploy on Vercel.
- [x] Footer social links (LinkedIn, X, HueGrid); removed empty Dribbble.

## Decisions Log
- 2026-06-02 · Source design is **Sketch**, read via the browser (no Sketch MCP) · can't read the file directly like Figma.
- 2026-06-03 · New site promoted to **repo root** (was `sateesh-portfolio-claude/`) · Vercel serves it with default settings.
- 2026-06-03 · **Proza Libre** site-wide + **Dancing Script** wordmark · matches the Sketch.
- 2026-06-03 · **Removed dark mode** and **all em dashes** · consistency + human tone (user preference).
- 2026-06-03 · **Per-case-study accent** + tinted section bands + left section rail · colorful editorial case studies (refs: smartbeans, yashbanka, ccunpacked).
- 2026-06-03 · Explorations are **boxed 2-col cards with category tags** · signal domain (incl. Hyperlocal Commerce).
- 2026-06-03 · Headless preview screenshots **blank when scrolled** on heavy-image pages · verify deep sections by DOM, not screenshot.
