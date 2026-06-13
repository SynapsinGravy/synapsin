# gravyworkshop.com

The website for **Synapsin Gravy Workshop** — a tiny independent software studio. *Small batch software.*

Static single-page site, deployed to [gravyworkshop.com](https://gravyworkshop.com) by Vercel on every push to `main`.

## What's published

| Path | Purpose |
| --- | --- |
| `index.html` | The homepage (studio + the three projects on the workbench) |
| `privacy.html` | Privacy policy — served at `/privacy` (required for Google Play) |
| `assets/` | Web-sized images: studio mark, project glyphs, favicon |
| `vercel.json` | `cleanUrls` (so `/privacy` works) + long cache on `/assets` |

## What's backed up but NOT published

The `dev/` directory holds all the planning, naming research, and original
full-resolution brand art. It is listed in `.vercelignore`, so it is committed
to git (and thus backed up on GitHub) but never uploaded to Vercel or served on
the site.

| Path | Contents |
| --- | --- |
| `dev/DOMAIN-SITUATION.md` | DNS / domain / registrar handoff |
| `dev/SITE-DESIGN-BRIEF.md` | Design research for this site |
| `dev/NAMING-AND-BLURBS.md` | The full naming decision trail (4 rounds) |
| `dev/HOMEPAGE-COPY-AND-IMAGES.md` | The copy + image plan this site was built from |
| `dev/handoffs/` | Identity docs for AppLadle and Keepfall |
| `dev/STOCKPOT-IDENTITY-HANDOFF.md` | Identity doc for the Stockpot memory system |
| `dev/brand-assets/` | Original full-resolution PNG logos |

## The studio's projects

- **AppLadle** — a personal pocket workspace of little apps (Android, coming soon).
- **Keepfall** — a real-time lane-combat castle game (in development; working title).
- **Stockpot** — a permanent personal-memory system (a tool built in-house).

## Editing images

Web assets in `assets/` are downsized from the originals in `dev/brand-assets/`.
To regenerate, resize an original with any tool to ~512–640px on the long edge
and save as an optimized PNG into `assets/`.

## Contact

hello@gravyworkshop.com · Sacramento, CA
