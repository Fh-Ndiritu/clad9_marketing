---
name: clad9-brand-refresh
description: Re-crawl clad9.com and report what changed about the Clad9 brand facts — sitemap, blog, features, methodology, pricing and voice. Use when the user says "refresh the brand context", "re-research the site", "the site has changed", "update Clad9 facts", "check what's new on clad9", or invokes /clad9-brand-refresh. Run this before a posting session if the facts baked into the other skills look stale.
---

# Refresh the Clad9 brand facts

Everything needed is in this file. Longer-form versions of the same material sit beside it in this skill's own folder (`references/angle-bank.md`, `references/brand-context.md`) — read them for extra depth if they're there, but never wait on them and never refuse to run because they aren't.

The other Clad9 skills carry their brand facts **inline**, in their own SKILL.md files. This skill checks those facts against the live site and reports drift, so the user can update the plugin.

It does **not** silently rewrite anything the other skills read at runtime — they don't read files, they carry their own copy. Producing a report the user can act on is the whole job.

## Why this exists

Clad9's programmatic factories regenerate continuously — the colours and style sitemaps moved the day before this plugin was built while everything else sat static. Feature copy drifts. Pricing may appear. Facts baked in months ago are the main way these skills can embarrass the user.

## The baseline, as of 2026-09-10

Compare what you find against this.

- **708 URLs** in the sitemap index across ten sub-sitemaps: marketing 3 · colors 241 · style 250 · features 9 · alternatives 5 · what-to-wear 61 · body-type 36 · faq 37 · capsule 53 · blog 13
- **`/pricing`, `/about` and `/how-it-works` all 404.** Nav "About" and "How It Works" are homepage anchors, not pages
- **No public price anywhere.** `/users/sign_up` promises "14-day free trial / No credit card required". Terms §7 confirms paid auto-renewing plans exist but names no figure
- **No social proof of any kind** — no user counts, testimonials, press, or ratings. Footer badges are directory listings (SaaSCity, Smol Launch) plus "From the makers of Hadaa"
- **12 blog posts**, newest 2026-09-03, attributed to "Clad9 Team", 6–7 min reads
- **10 named features** at `/features/*`
- **Known inconsistency:** `/features` says capture is "one video walkthrough of your closet"; the homepage and `/features/wardrobe-capture` say batch photo upload
- Operated by **Hadaa, Inc.** Contact addresses in use: clad9@hadaa.app, hello@clad9.com, privacy@clad9.com

## Steps

1. **Enumerate.** Fetch `https://clad9.com/robots.txt`, then `https://clad9.com/sitemap.xml` — it's an index. Fetch each sub-sitemap, count URLs, and record the `lastmod` on each. A moving date means that factory is live; a stale one means it's frozen.

2. **Diff against the baseline above.** Report any factory that appeared, disappeared, or changed size by more than ~10%.

3. **Check for pricing.** Fetch `/pricing`, `/about`, `/how-it-works`. **If `/pricing` now returns a real page, that is the single most important finding** — read it, record the exact tiers and figures, and say clearly that the "never state a price" rule baked into the other skills now needs changing.

4. **Re-read the core pages:** `/`, `/features` and each `/features/*`, `/methodology`, `/blog` plus the newest 3 posts, `/users/sign_up` for trial terms, `/terms` §7 for payment language.

5. **Check the video-vs-batch-photos inconsistency.** Report whichever way it resolves. Until the homepage says otherwise, the rule stands: describe capture as batch photos.

6. **Re-check claims.** Have user counts, testimonials, press mentions or hard numbers appeared? The prohibition on inventing them only holds while there genuinely are none.

7. **Blog cadence.** Count posts, note the newest date and the categories in use. New posts are new post angles.

8. **Voice.** Pull 5–8 fresh verbatim sentences from the blog and hubs. If the register has shifted away from the dry, corrective blog voice, say so rather than quietly assuming it hasn't.

## Output

A short plain-language report: what changed, what's new, and — first, always — anything that invalidates a rule the other skills are posting under. Pricing above all.

Then, for anything that did change, give the user the **exact replacement text** for the affected block in the affected SKILL.md files, so updating the plugin is a copy-paste rather than a rewrite. Name the files.

If nothing material changed, say so in one line. Do not manufacture findings.

## Keeping the plugin in sync

The skills live in `github.com/Fh-Ndiritu/clad9_marketing`. Changes made to an installed copy don't flow back — they must reach the repo or they're lost at the next sync. If the user wants the changes applied, offer to edit the repo working copy and commit.
