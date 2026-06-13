# Identity Handoff: FoldSpace → **AppLadle** (FINAL)

2026-06-13. **Name confirmed FINAL** after a 4th naming round that tested single-word kitchen names (Crockle, Jiggery, Spurtle, Tongs, et al.). Crockle and Jiggery scored higher on pure brand-feel, but both derive from deception idioms ("that's a crock", "jiggery-pokery") — a poor fit for a privacy/trust app with an honest-copy rule. The owner chose AppLadle: no bad-idiom echo, and the only candidate with the clean bare .com + .app. Full data: `~/projects/NAMING-AND-BLURBS.md`.

## Your new name

**AppLadle** — Play title: **"AppLadle: your little apps"** (26 chars of the 30 cap; descriptor swappable for ASO).

Why it won: it is the owner's own brainstorm — "Synapsin: Ladling your own mini-apps" — with the rejected part removed. The ladle keeps his serve-yourself metaphor; deleting the studio word fixes "too exact a match"; and putting "App" inside the name makes the category structurally explicit, so "not clear enough what it does" is impossible. Screened **low risk**: no app, company, product, or trademark named AppLadle anywhere; **both appladle.com ($11.25) and appladle.app ($9.99) were live-verified buyable on 2026-06-13** — grab both before announcing anything. Known cost: occasional "app label" mishearing in fast speech ("ladle, like the soup spoon").

Brand-family note, chosen with eyes open: a ladle is the tool you serve gravy with and dip into a stockpot — the closest of the finalists to the studio's table. The judges read it as a deliberate family joke rather than catalog duplication (it shares no *word* with the studio and isn't a pot or the boat).

**Alternates if the owner balks:** *Ramekin* (best brand-system fit of any name screened in three rounds — Stockpot, Keepfall, Ramekin is a real product family — but the word is opaque to non-cooks and neither ramekin.com nor .app is available) and *Snack Drawer* (the wit IS the clarity: kitchen snack drawer + the Android "app drawer" pun; medium risk — an Australian creative agency holds an AU trademark and the .com; snackdrawer.app is free). *Simmerkit* held both exact domains free with a spotless screen, if a coined neutral name is ever wanted.

Owner-floated names, screened and retired: *Synapsin* (it IS the company's lead word — the Apps & Gravy failure in purer form — and reads as a neuroscience drug, which it literally is: a Synapsin® supplement exists), *Gravy Boat* ("The Gravy Boat" restaurant app is live on Play; it's the studio's logo object — a product wearing the company emblem reads as merch; crude Urban Dictionary baggage), *Saucepot Apps* (clean screen, narrowest miss — but a second pot beside Stockpot collapses the family system), *IdeaBroth* (broth is what comes OUT of a stockpot — it names the sibling's output, and points at brainstorming, not apps).

## Who this app is for (write all copy to this person)

**The tinkerer** — a curious, privacy-minded person who has always wanted a little app of their own (expense tracker, habit streaks, flashcards) without learning a dev environment or trusting a cloud service. Not developers (they have real tooling); not passive consumers (built-ins are the on-ramp, not the product).

**The pitch:** describe the tiny personal app you wish existed and have it running as a tile on your grid a minute later — private, offline, no account, no ads, and it stays yours (exportable as a plain file).

**Site card blurb options:**
> a small grid of tools and games on your phone, plus a bench for making your own — offline, no account, no ads.

> ladle out your own little apps — ours to start, yours from there. offline, no account, no ads.

**Voice:** lowercase confidence, plain and warm, zero hype words ("passionate", "innovative", "revolutionary", "solutions" are banned). The repo's existing "honest copy" rule (claims must match code) is exactly right — keep enforcing it.

## Rename checklist

**Do before first Play publish (permanent afterward):**
- `applicationId` → `com.synapsingravy.appladle`. This also sheds the awkward `com.aistudio.foldspace.wsrjty`.

**Rename freely (user-visible):**
- `app_name` in `app/src/main/res/values/strings.xml`
- ~20 user-visible strings: onboarding "Welcome to FoldSpace", workspace header (`FoldSpaceWorkspace.kt:553`), "Save as FoldSpace app…", share preamble "an app made with FoldSpace" (`ModuleFile.kt`), backup toasts/errors, and the Gemini system prompt "You are FoldSpace's app generator"
- `README.md` / `metadata.json` (note: there's a public AI Studio listing URL referencing the old name)
- Internal class names (`FoldSpace{ViewModel,Repository,Database,Dao,Workspace}`) — optional, invisible to users

**NEVER rename (frozen forever, or user data breaks):**
- Prefs files `foldspace_prefs` / `foldspace_secrets` (the latter wraps the DB encryption key)
- DB file `foldspace_secure_container.db`
- Synthetic WebView origins `https://module-<id>.foldspace.local/` (per-module localStorage is keyed to that domain — renaming wipes data inside users' custom apps)
- The `.fsapp` / `.fsbak` formats ("FSBK" magic)

These are all invisible internals; legacy ids under a new brand are normal and fine.

## Domains & web presence

- **Buy:** `appladle.com` ($11.25) + `appladle.app` ($9.99) — both verified available 2026-06-13; availability decays, don't sit on it.
- Canonical product page: `gravyworkshop.com/appladle` (per the one-domain site strategy); the bought domains redirect there.

## New logo needed (old assets don't carry over)

The FoldSpace blue "stacked layers" icon is tied to the dead fold metaphor and the wrong palette; the CodeSnip Vault repo only ever had stock Expo placeholders. Generation prompt, matched to the studio's gravy-boat mark:

> Minimal flat line-art app icon for a small craft software studio. A kitchen ladle seen in profile, tilted mid-pour over a tidy 2×3 grid of small rounded-square tiles below; a single drop falls from the ladle's bowl toward one empty tile in the grid, the other tiles bearing simple glyphs (a calculator sign, a pencil, a game diamond, a leaf). Single consistent stroke weight, hand-drawn but precise, warm dark-brown ink (#3E2B22) on warm gray paper (#D6D1C8), strictly two colors, no gradients, no text, no gloss. Generous negative space, centered square composition. Same visual family as companion marks of a gravy boat with circuit-board steam and a lidded stockpot. Must stay legible at 48 px as an Android launcher icon.
