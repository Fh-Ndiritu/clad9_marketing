---
name: clad9-brand-refresh
description: Re-crawl clad9.com and rewrite the Clad9 brand context from the live site — sitemap, blog, features, methodology, pricing and voice. Use when the user says "refresh the brand context", "re-research the site", "the site has changed", "update Clad9 facts", "check what's new on clad9", or invokes /clad9-brand-refresh. Run this before a posting session if the context file is more than a few weeks old.
---

# Refresh the Clad9 brand context

> Paths here are relative to this skill's own folder — the base directory announced when the skill loads. If a path doesn't resolve, locate the plugin directory (the one containing `.claude-plugin/plugin.json`) and read `references/` from there. Never proceed on remembered facts if these files can't be read — say so and stop.

Rebuild `../../references/brand-context.md` and the content map in `angle-bank.md` from what clad9.com actually says today. Everything else in this plugin depends on those two files being true.

## Why this exists

Clad9's programmatic factories regenerate continuously — the colours and style sitemaps changed the day before this plugin was built while everything else sat static. Feature copy drifts. Pricing may appear. Claims written from a stale context file are the main way this plugin can embarrass the user.

## Steps

1. **Enumerate.** Fetch `https://clad9.com/robots.txt` then `https://clad9.com/sitemap.xml`. It is a sitemap index — fetch each sub-sitemap and count URLs per factory. Record the `lastmod` on each; a moving date means that factory is live, a stale one means it is frozen.

2. **Diff the map** against the table in `angle-bank.md`. Report any factory that has appeared, disappeared, or changed size by more than ~10%.

3. **Check for pricing.** Fetch `/pricing`, `/about`, `/how-it-works`. As of the last crawl all three 404. **If `/pricing` now returns a real page, that is the single most important finding** — read it, record the exact tiers and figures, and update the hard rule in `brand-context.md`, which currently forbids stating any price.

4. **Re-read the core pages:** `/`, `/features` and each `/features/*`, `/methodology`, `/blog` and the newest 3 posts, `/users/sign_up` for the trial terms, `/terms` §7 for payment language.

5. **Check the known inconsistency.** `/features` has historically claimed "one video walkthrough of your closet" while the homepage says batch photo upload. Check whether it is fixed. Whichever way it resolves, the rule stands: describe capture the way the homepage and `/features/wardrobe-capture` describe it.

6. **Re-check claims.** Have user counts, testimonials, press mentions or hard numbers appeared? The prohibition on inventing them only holds while there genuinely are none.

7. **Blog cadence.** Count posts, note the newest date and the categories in use. New posts are new post angles — add them to the angle bank.

8. **Voice.** Pull 5–8 fresh verbatim sentences from the blog and hubs. If the register has shifted, say so rather than quietly rewriting the voice rules.

## Output

Rewrite both reference files in place, then report to the user as a short diff in plain language: what changed, what is new, and anything that invalidates a rule they have been posting under. Lead with anything that affects what may be claimed — pricing above all.

If nothing material changed, say so in one line. Do not manufacture findings.
