# Naming & Blurbs — Research Results

2026-06-12. From a 35-agent research workflow: product deep-reads (FoldSpace, codesnip-vault, Castle-Wars, memory repo), market/ASO research, 26 name candidates generated from 3 angles, every candidate screened for Play/App Store collisions + trademark + domains, then ranked by a 3-lens judge panel (consumer clarity, brand fit, practical/ASO). A second 8-agent screen covered the user's proposed names + kitchen-register candidates + the Castle Wars working title.

## ⭐ FINAL DECISIONS (2026-06-12)

- **App (ex-FoldSpace/CodeSnip Vault): "AppLadle" — FINAL (chosen by owner 2026-06-13)** — Play title "AppLadle: your little apps" (26 chars), marketing tagline "spoon out your own little apps", package `com.synapsingravy.appladle`, **buy appladle.com ($11.25) + appladle.app ($9.99)**. It is the owner's own "Synapsin: Ladling your own mini-apps" idea minus the studio word, with "App" baked in for clarity. ROUND 4 (single-word kitchen names) scored Crockle (24.7) and Jiggery (23.1) above AppLadle (21) on brand-feel, but both derive from deception idioms ("that's a crock"/"jiggery-pokery") — wrong for a privacy/trust app — and lack the bare .com; owner picked AppLadle as the trust-safe, clean-domain choice. Round-4 owner-floated words all retired: Sauceboat/Sauciere (= the studio gravy-boat logo), Stewpot/Cauldron (2nd pot beside Stockpot; Cauldron has pending software TM), Spork (live Spork apps + TM + domains gone), Tongs (reads as bare noun, domains gone). Earlier rounds also rejected: Apps & Gravy (too studio-matching), My Little Apps, Your Little APPlesauce, Ramekin, Snack Drawer, Simmerkit, Mini App Workshop, Synapsin, Gravy Boat, Saucepot Apps, IdeaBroth, Biscuit Tin, Pantry, Spice Rack. Handoff: `FoldSpace/IDENTITY-HANDOFF.md`. Homepage copy + glyph: `HOMEPAGE-COPY-AND-IMAGES.md`.
- **Game (ex-Castle Wars): working title "Keepfall"** — "Marching Order" screened HIGH (SFB Games' live exact-name game on Play+App Store since ~2016; Crumbling Keep's tabletop line already uses "Marching Order: <Subtitle>"); "Keepfall" alone screened LOW (clean everywhere, keepfall.app free). Handoff: `Castle-Wars/IDENTITY-HANDOFF.md`.
- **Memory system (repo obsidian-memory): public name "Stockpot"** — beat Preserves (transformation vs. storage; stock→gravy feeds the workshop); "preserves" reserved as the backup/export layer name. Handoff: `STOCKPOT-IDENTITY-HANDOFF.md`.
- **Domains — buy:** synapsingravyworkshop.com ($11.25, protects the Play publisher name) + appsandgravy.app ($9.99); **watch** appsandgravy.com (parked, expires 2026-07-26). **Keep:** gravyworkshop.com, synapsin.dev (in active use), synapsinai.com/.dev, curiousintersect.com/.blog. **Let go:** aggregatedreviews.com, curated.review, synapsinpce.com/.dev, codesnipvault.com, iqcodevault.

---

## 1. The mini-app workspace (working name "FoldSpace")

### What it actually is (per code, not aspiration)

Audience is **the tinkerer, not the developer**: a privacy-minded person who's always wanted a little app of their own (expense tracker, habit streaks, flashcards) without a dev environment or a cloud service. Pitch: *describe the tiny personal app you wish existed and have it running as a tile on your grid a minute later — private, offline, no account, no ads, exportable as a plain file.* The differentiator is the combination: AI-built personal mini-apps (user's own Gemini key, no telemetry) running sandboxed/offline/on-device with provable data ownership. Built-in tools/games are the friendly on-ramp.

### Both incumbent names lost on the merits

- **FoldSpace** — eliminated by all three lenses. Reads as a foldable-phone utility (which the code can't back up — no hinge awareness) or sci-fi (Dune). Says nothing about mini-apps, making things, or privacy. `foldspace.ai` is an active SaaS occupying the exact "AI operates your apps" territory; foldspace.com long-held; foldspace.app registered three weeks ago. Practical judge: "rename is cheap now and expensive after Play publish — spend it."
- **CodeSnip Vault** — never published (sideloaded QA APKs only, no Play listing), names a developer-only niche that caps the audience, sits in a noisy CodeVault/SnipVault namespace, codesnipvault.com taken by a third party. **Note: the remembered "simple logo" is not in the repo** — all four image assets are the stock Expo placeholder. A new logo is needed regardless of name.

**Rename cost is LOW pre-launch** but four internals must keep legacy ids forever or user data breaks: prefs files `foldspace_prefs`/`foldspace_secrets`, DB file `foldspace_secure_container.db`, WebView origins `https://module-<id>.foldspace.local/`, and the `.fsapp`/`.fsbak` formats. Change the `applicationId` (`com.aistudio.foldspace.wsrjty`) before first Play publish — it's permanent after. CodeSnip's import schema (`z.literal('CodeSnip Vault')`) should keep an alias if any beta exports survive.

### Panel results

| Name | Votes | Score | Risk | Domains | Note |
|---|---|---|---|---|---|
| **Mini App Workshop** | 2/3 | 16.5 | low | **.com AND .app free** | Clarity 9/10; echoes studio name; generic = unprotectable mark |
| **Your Little Apps** | 2/3 | 14 | medium | **.com AND .app free** | Warm, human; doesn't signal "make your own" |
| Tilery | 1/3 | 9 | medium | both taken | Brand-fit favorite (real word: place where tiles are made; UI is a tile grid); "Tiler" app one letter away |
| Toybench | 1/3 | 8.5 | **low** | .app free, .com broker-held | Cleanest screen of any coined name; most trademark-registrable; "toy" tips toward novelty |
| Make Me an App | 1/3 | 8.5 | — | — | Best "why I want it" but welded to the 2025-26 AI moment |
| Smallware | 1/3 | 8.5 | high | — | "Small batch software" made literal, but smallware.app is a live same-concept product |
| Breadbox, Homemade Apps, Whittle, Pegboard… | 1 | ≤8 | mixed | — | Whittle/Homemade Apps/Tinkertray/Mini App Maker all high-risk (live collisions) |

### Recommendation

**Mini App Workshop** — the panel consensus and the direct answer to the stated goal (a stranger understands what it does and why they'd want it in half a second). "Mini apps" is the exact term Google's own Opal marketing is teaching consumers. Both domains free — register immediately if chosen. The honest costs: as a generic phrase you'll never own it as a mark, and "Mini App Workshop by Synapsin Gravy Workshop" repeats "Workshop" on your own site (the brand-fit judge's main objection).

**Runner-up (warmth): Your Little Apps.** **Runner-ups (ownable brand): Toybench** (cleanest legal/ASO position of any coined name; "Toybench: mini apps & games" = 27/30 chars) or **Tilery** (best craft-register fit; accepts a confusable neighbor).

ASO strategy either way: Play title = name + descriptor (30-char cap), e.g. "Mini App Workshop" alone or "Toybench: mini apps & games"; the 80-char short description and fully-indexed long description carry the keyword tail (offline, no account, make your own app, AI).

### Coming-soon card blurb (winning seed, fits any of the top names)

> a small grid of tools and games on your phone, plus a bench for making your own — offline, no account, no ads.

### App logo generation prompt

> Minimal flat line-art app mark for a small craft software studio. A small, sturdy wooden workbench seen straight on; on its top, a tidy 2×3 grid of square tiles like little app icons — four tiles filled with simple glyphs (a calculator sign, a pencil, a game diamond, a leaf), one tile half-assembled with a tiny hammer resting beside it, one tile empty. Single consistent stroke weight, hand-drawn but precise, warm dark-brown ink (#3E2B22) on warm gray paper (#D6D1C8), strictly two colors, no gradients, no text, no gloss. Generous negative space, square composition. Same visual family as a companion logo of a gravy boat with circuit-board steam. Must stay legible at 48 px as an Android launcher icon.

---

## 2. Castle Wars

### Name reality check: treat "Castle Wars" as a working title

The phrase is heavily occupied: Jagex's RuneScape *Castle Wars* minigame owns the search results with 20+ years of wiki SEO; Google Play has exact-name collisions today (`zogr.castle.wars`, "Castle Wars: Legacy", "Castle Wars Online"); Steam has several more; and the classic XGen Flash *Castle Wars* makes the name evoke the wrong genre (turn-based cards). No single blocking trademark — the problem is discoverability, not legality.

Unscreened alternates from the design's own vocabulary (each needs its own collision check before adoption): **One Lane Kingdom**, **Single File**, **Keepfall**, **Marching Order**, The Narrow Road. (Pre-checked: "Gatefall" is taken.)

### Site card blurbs

One-liners:
1. *one lane, two castles, about two minutes to capture a princess.*
2. *real-time lane combat for android. the AI plays by the same rules you do — twelve personalities, no cheating.*
3. *fully playable, currently drawn in labeled rectangles. the rectangles are surprisingly tense.*

Longer:
> castle wars (working title) is a real-time lane combat game: breach the gate, get past the king, capture the princess before they capture yours. matches run 90 seconds to 3 minutes against twelve AI personalities that play under exactly the same rules you do. it's fully playable now — in placeholder rectangles — while we make the AI good enough to beat us.

### Image direction

Don't fake polished screenshots — none exist (units are literally labeled rectangles). Either (a) own the placeholder: a tidy side-view diagram of the real game state restyled into the studio palette, or (b) a flat game mark at the same visual weight as the gravy boat. Generation prompt:

> Minimal flat game mark for an in-development indie strategy game, in the style of a small craft software studio. A medieval castle gate with a portcullis, seen straight on, with a single straight road running through it toward a second, smaller gate on the horizon; on the road, a single-file row of small plain rectangles marching toward the gate, the front two rectangles meeting head-to-head; a tiny crown floating above the far gate. Warm dark-brown and warm-gray palette on an off-white cream background, with one muted blue rectangle and one muted red rectangle as the only accent colors. Hand-drawn but tidy linework, somewhere between woodcut and technical diagram; generous negative space; flat color only — no text, no gradients, no gloss, no 3D, no photorealism. Composition balanced to sit beside a small logo of a gravy boat with a circuit-board brain steaming out of it.

---

## 3. The memory system (private repo "obsidian-memory")

### Public naming: the current name cannot ship

"Obsidian" is Dynalist Inc.'s trademark for the Obsidian note app — and this project is literally an "Obsidian-compatible markdown store" per its own README, so a public "obsidian-memory" reads as an official Obsidian product: textbook likelihood-of-confusion (Microsoft's Obsidian Entertainment also holds software marks). Fine as a private repo name; rename for the site. Also keep "second brain" out of names and copy — Tiago Forte's BASB is enforced trademark territory.

Screened candidates (web-checked), front-runners first:
- **stockpot** — everything goes in the pot and simmers overnight; the longer it runs, the richer it gets — and stock is what gravy is made from. Sits perfectly inside the Gravy Workshop register. Only collision: an iOS recipe-manager app, different category. *(Considered and dropped: "marrow" — the Indian medical-ed app Marrow actively litigates its mark.)*
- **commonplace** — the commonplace book is the centuries-old original personal memory system; this is one that keeps itself. Clean lane, historically exact.
- **preserves** — small-batch preserving; memory put up in jars for years. Rhymes with "small batch software."
- roux (Scandy 3D SDK collision, different field), loam (Loam Bio, low practical risk), heartwood (multiple software shops — weakest clearance).

### Site card blurbs

One-liners:
1. *a permanent memory for one life: journals and reading go in, a self-tending personal wikipedia comes out.*
2. *notes go in the inbox; overnight they become atomic claims, links, and wiki pages. it remembers so we don't have to.*
3. *a personal wikipedia that tends itself while we sleep. the memory works; the part that does research overnight is still learning.*

Longer:
> a permanent memory system for one life. journal entries, articles, and conversations land in an inbox; overnight jobs break them into atomic notes, link what belongs together, and grow a personal wikipedia that gets deeper the more goes in. the memory layer is solid and in daily use — the part that's meant to run research and builds while we sleep hasn't earned its keep yet.

### Image direction + prompt (pairs beautifully with the name "stockpot")

> Minimal flat line-art logo glyph for a small craft software studio. A lidded cast-iron stockpot simmering on a low flame; steam rises from under the lid and resolves into a small constellation of linked dots — five to seven nodes connected by thin lines, like a tiny mind map forming in the steam. Single consistent stroke weight, hand-drawn but precise, warm dark-brown ink (#3E2B22) on a warm gray paper background (#D6D1C8), strictly two colors, no gradients, no shading, no text. Generous negative space, square composition, centered. Same visual family as a companion mark of a gravy boat with circuit-board steam. Must stay legible scaled down to a 64 px inline icon.

---

## 4. Immediate actions

1. **Register domains for the chosen app name now** — `miniappworkshop.com`/`.app` and `yourlittleapps.com`/`.app` all showed RDAP 404 (likely unregistered) on 2026-06-12; `toybench.app` also free. Cheap insurance even before deciding.
2. Change the Android `applicationId` before first Play publish (permanent after); keep the four legacy internal ids listed in §1 to avoid breaking user data.
3. A new app logo is needed in every scenario — the CodeSnip "simple logo" isn't in the repo (stock Expo placeholders only).
4. If an alternate Castle Wars name appeals, run it through the same screen (Play/Steam/trademark/domains) before attaching it to anything.
