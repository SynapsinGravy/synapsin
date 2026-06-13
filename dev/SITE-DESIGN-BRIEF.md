# Synapsin Gravy Workshop — Site Design Brief

Research-backed brief for rebuilding gravyworkshop.com. Prepared 2026-06-12. Sources: simogo.com, shinyfrog.net, tapbots.com, panic.com, Game Developer indie-site structure guidance, Google Play Console publisher requirements.

## What the site is for

Proof the studio exists (Google Play publisher website, link target from store listings), an honest statement of the ethos, and a design foundation that can grow. It is NOT a marketing funnel, blog, or press hub yet.

## Recommended structure: one page, one domain, five sections

Every well-regarded tiny studio site (Simogo, Shiny Frog, Tapbots, Panic) is a single scrolling typographic column. Keep studio + future app pages on one domain — future apps become `/foldspace`, `/castle-wars` paths so press links and SEO accrue to the studio.

1. **Hero** — wordmark/logo + one-line self-description. Smallness stated as fact, not apology (cf. Tapbots' "We are 3 humans"). No hero image needed.
2. **Apps ("Things we're making")** — one card per app, honest states:
   - **FoldSpace** — name, one-sentence hook, "coming soon." (Android personal mini-app workspace: built-in tools/games plus mini-apps you create yourself or generate with Gemini; dual-pane layout for large/foldable screens. v1.0, early.)
   - **Castle Wars** — name + "an Android game, in development." (Godot 4 real-time lane-combat castle siege; 90–180s matches; playable MVP as of May 2026.)
   - Two honest entries read better than one inflated one. Decide whether CodeSnip Vault (currently on the page as "Coming Soon" beta) stays, moves to a "past/paused" mention, or is dropped.
3. **Ethos** — 2–4 sentences max, first person plural. No "Our Story."
4. **Contact** — `hello@gravyworkshop.com` with one warm line. Doubles as Play Store support contact.
5. **Footer** — copyright, link to `/privacy`, location (Sacramento, CA — legitimacy signals live in the footer).

## Google Play publisher-site checklist

- Verify the **Domain property in Google Search Console** (DNS TXT in the Vercel zone) with the same Google account as the Play Console login, so Play's website verification auto-approves. No google-site-verification TXT exists yet.
- **Privacy policy at a stable URL** (`/privacy`), public HTML (no PDF), never moved. Required per app before publishing.
- **Support email on a domain address** (hello@ via ForwardEmail already exists).
- 2025–26 developer-verification wave: identity verification required; from Sept 2026 only verified-developer apps install on certified devices in initial regions. A real site + matching domain email smooths this.

## Design direction (ages well, not template-y)

- **Typography-first**: one good typeface used boldly, generous whitespace, plain sections separated by rules. The proven pattern across every reference site for a decade, and the current (2025–26) showcase trend.
- **One ownable motif**: the gravy-boat-with-circuit-brain logo is distinctive — let it be the single visual anchor (cf. Tapbots' robots). Logo files: `~/projects/SynapsinGravy-final.png` (with wordmark), `SynapsinGravy-final-wordless.png`. The dark-brown/warm-gray logo palette suggests a warm, craft-kitchen accent rather than the current cold slate-blue dev-tools palette.
- **Light background** default (dark mode optional later); at most one accent color.
- Micro-interactions only where they signal care (a hover, a subtle reveal).
- **Avoid**: illustration-heavy heroes, parallax, 3D blobs, gradient-hero-plus-three-feature-cards Tailwind-template look, multi-page nav bars (anchor links at most).

## Reference sites

- **simogo.com** — closest model. Two people, one-sentence self-description, plain chronological project list, minimal footer. Confidence through restraint.
- **shinyfrog.net** — exactly how to present ONE flagship app + personality: "We are an artisanal app crafting team," one app as a linked headline, human details, hello@ footer.
- **tapbots.com** — app cards with icon + one line; one motif carries the identity.
- **panic.com** — verb-led copy ("We code apps, publish games…"); real address in footer.

## Tagline

Current "We build practical tools." doesn't capture the real ethos: *we make things WE enjoy making, that we feel OTHERS can get value from using.*

Pattern from the greats: short, declarative, first-person plural, present tense; names the craft, the output, or the motivation. Never "passionate," "innovative," or "solutions."

Candidates:
1. "We make things we love making — and that we hope you'll love using." (most direct)
2. "A tiny workshop building apps and games we actually want to exist."
3. "Two people. A workshop. Things worth making."
4. "Made for the joy of making it. Shared because it's useful."
5. "Small batch software." (shortest; craft-kitchen energy; pairs well as footer/meta-description with a longer hero sub-line)

Recommendation: #1 or #2 as the hero sub-line; #5 as footer flourish.

## What NOT to include at this stage

- No blog/news (a stale blog is the biggest legitimacy-killer). The current page's "Blog (currently inactive)" link should go.
- No press kit (belongs on the Castle Wars page near launch).
- No team bios/headshots, careers, testimonials, newsletter popups, cookie banners.
- No fake-it content: no placeholder screenshots, "trusted by" logos, or dated roadmap promises. "In development," stated plainly, IS the indie credibility move.
- Probably no "Tech Stack" section (current page has one) — none of the reference studios list their stack; it reads agency/portfolio, not workshop.
