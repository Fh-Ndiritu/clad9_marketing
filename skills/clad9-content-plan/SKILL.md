---
name: clad9-content-plan
description: Produce a rolling content plan for the Clad9 Facebook and LinkedIn Pages — which angle, which source page, which platform, which image, in what order. Use when the user says "content plan", "what should we post this week", "plan the content", "build a schedule", "what's next for Clad9 social", or invokes /clad9-content-plan. Run this first when starting a posting cycle; the individual post skills execute against it.
---

# Build the Clad9 content plan

Turn the angle bank into a concrete, ordered queue of specific posts. This skill decides *what* to say; `clad9-fb-post` and `clad9-li-post` execute it.

## Read first

> Paths here are relative to this skill's own folder — the base directory announced when the skill loads. If a path doesn't resolve, locate the plugin directory (the one containing `.claude-plugin/plugin.json`) and read `references/` from there. Never proceed on remembered facts if these files can't be read — say so and stop.

- `../../references/brand-context.md`
- `../../references/angle-bank.md`

## Steps

1. **Establish what has already gone out.** Open both Pages and read the last 10 posts on each. This is the only reliable record — there is no state file, deliberately, because a state file drifts and the Pages don't. Note angle, source page and opening construction for each.

2. **Check the season.** Use the seasonal calendar in the angle bank against today's date. The seasonal angle leads; it is the one with a real reason to be posted now rather than in March.

3. **Pick the angles.** Default to one week: 3 posts, alternating platform, plus one comment run. Rotate through the nine angles — never the same angle twice running on one platform, and never the same angle on both platforms in the same week.

   If the user asks for a different volume, or is scheduling this to run repeatedly, size the queue to what they ask for and lean harder on rotation: at twice-daily cadence the nine angles cycle in under a week, so vary the *source page* within an angle rather than repeating the angle wholesale. There are 241 colour pages and 250 garment pages — the specificity is effectively inexhaustible even when the angle repeats.

4. **Bind each post to a real source URL.** Every entry names the exact clad9.com page it draws from. Prefer the orphan colour and garment pages that the hubs don't link to — those posts do double duty as internal-linking signals.

5. **Write the image brief** for each post: the prompt shape from `flow-images.md` and the aspect ratio for the destination platform.

6. **Sanity-check the queue** against the claim rules in `brand-context.md`. Any entry that would need a price, a user count or a testimonial to work is not a viable post — replace it.

## Output

A table the user can act on:

| # | Day | Platform | Angle | Source URL | Hook (one line) | Image brief | Ratio |
|---|---|---|---|---|---|---|---|

Then one short paragraph on why this particular set, now — the seasonal logic and what it is trying to establish while the Pages are still cold.

Keep it to the queue and the reasoning. Do not draft the full post copy here; that happens in the posting skills, against the live page and a fresh read of the source.

## Standing priorities while the Pages are new

Both Pages started at zero followers in September 2026. Until there is an audience:
- **Comments outrank posts.** A post to zero followers reaches zero people. Weight the plan accordingly.
- **The methodology angle is the differentiator.** Give it a slot regularly — no competitor has an equivalent to point at.
- **Specificity beats reach.** "What a petite woman wears to a job interview" will outperform "5 style tips" on a Page nobody follows yet.
