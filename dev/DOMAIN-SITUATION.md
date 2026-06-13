# gravyworkshop.com — Domain Situation Handoff

Prepared 2026-06-12 from external DNS probes, the Vercel API (team `mrmatthewpohls-projects`), and the GitHub repo. For an agent with access to the registrar, DNS, and Vercel dashboard.

## TL;DR

The domain works today: `gravyworkshop.com` serves the static site from GitHub repo `mr-matthew-pohl/synapsin` via Vercel, `www` redirects to apex, and `dailymovement.gravyworkshop.com` serves a second Vercel project. DNS for the whole zone is hosted on Vercel nameservers, so almost all routing changes happen inside the Vercel dashboard, not at the registrar. There are two anomalies to resolve (below) but nothing is broken for visitors.

## The layers

| Layer | Who/where | Details |
|---|---|---|
| Registrar | Name.com, Inc. | Registered 2025-01-15, **expires 2027-01-15**, last changed 2026-04-24 (likely the nameserver switch) |
| Nameservers | Vercel (`ns1`/`ns2.vercel-dns.com`) | Entire DNS zone is managed in a Vercel account's Domains tab — registrar is only used for renewal and NS delegation |
| Hosting | Vercel team `mrmatthewpohls-projects` (`team_B8YbwInlOu84VZznnc5kcAA6`), owner login `mr-matthew-pohl` (mr.matthew.pohl@gmail.com) | Five projects; relevant ones below |
| Email | ForwardEmail.net | MX `mx1`/`mx2.forwardemail.net`, SPF `include:spf.forwardemail.net -all`. `hello@gravyworkshop.com` (used on the site) is forwarded mail, not a hosted mailbox |
| Source | GitHub `mr-matthew-pohl/synapsin` (public) | Static: just `index.html` + `README.md`. Push to `main` → Vercel auto-deploys production |

## What resolves where (verified 2026-06-12)

- `gravyworkshop.com` → Vercel apex A records (216.198.79.1, 64.29.17.1) → **HTTP 200**, serving `index.html` from the synapsin repo (confirmed byte-for-byte: live etag `627be757…` = md5 of the repo file).
- `www.gravyworkshop.com` → **307 redirect to apex**. Correct, no action needed.
- `dailymovement.gravyworkshop.com` → `cname.vercel-dns.com` → **HTTP 200**, attached to Vercel project `physical-activity-advisor` (a Next.js app).
- Vercel **Deployment Protection is enabled** on the synapsin project: `synapsin-mrmatthewpohls-projects.vercel.app` returns 401 (auth wall). This is "Standard Protection" behavior — custom domains stay public, vercel.app URLs require login. Working as intended; don't "fix" the 401.

## Anomalies to resolve

1. **The apex domain isn't visible on any project via the Vercel API.** `gravyworkshop.com` serves the synapsin project's content, but the API's domain list for project `synapsin` (`prj_fmr0WDVAtUCk0gEwuUKsP5jo6Mjt`) shows only vercel.app aliases — no custom domain. Meanwhile the subdomain `dailymovement` IS properly attached to `physical-activity-advisor`. Likely either (a) the apex is routed by raw A/ALIAS records in the Vercel DNS zone rather than a proper project-domain attachment, or (b) it's attached in a scope the API token doesn't surface. **Action:** in the Vercel dashboard check Team → Domains → gravyworkshop.com, and Project synapsin → Settings → Domains. If the apex isn't formally attached to the synapsin project, attach it (and `www` with redirect-to-apex) so future deploys, SSL renewals, and the dashboard all behave predictably.
2. **`synapsin.vercel.app` returns 404 DEPLOYMENT_NOT_FOUND** even though the API lists it as a project domain. Cosmetic (nothing links to it), but check Project → Settings → Domains and remove or re-point the stale alias.

## Watch-outs for any DNS work

- Don't change nameservers at Name.com unless deliberately moving DNS off Vercel — that would silently drop the `dailymovement` record, the ForwardEmail MX/SPF records, and apex routing all at once. Any record edits belong in Vercel → Domains → gravyworkshop.com → DNS Records.
- The ForwardEmail records (MX + 2 TXT) keep `hello@gravyworkshop.com` alive; the site and Google Play contact use that address. Preserve them in any zone changes.
- Renewal: domain expires **2027-01-15** at Name.com — confirm auto-renew is on.
- There is no `google-site-verification` TXT record on the apex yet. If/when Google Play Console asks to verify the publisher website, add it as a TXT record in the Vercel DNS zone (or use the HTML-tag method in the site head).

## Desired end state (so the agent knows what "done" looks like)

- `gravyworkshop.com` + `www` formally attached to the `synapsin` Vercel project (www → apex redirect), apex serving production deploys of `mr-matthew-pohl/synapsin@main`.
- `dailymovement.gravyworkshop.com` untouched.
- ForwardEmail MX/TXT untouched.
- Stale `synapsin.vercel.app` alias cleaned up or working.
- Auto-renew confirmed at Name.com.
