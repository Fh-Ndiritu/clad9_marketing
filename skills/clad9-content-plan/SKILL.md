---
name: clad9-content-plan
description: Produce a rolling content plan for the Clad9 Facebook and LinkedIn Pages — which angle, which source page, which platform, which image, in what order. Use when the user says "content plan", "what should we post this week", "plan the content", "build a schedule", "what's next for Clad9 social", or invokes /clad9-content-plan. Run this first when starting a posting cycle; the individual post skills execute against it.
---

# Build the Clad9 content plan

Decide *what* to say. `clad9-fb-post` and `clad9-li-post` execute it.

Everything needed is in this file. Longer-form versions of the same material sit beside it in this skill's own folder (`references/angle-bank.md`, `references/brand-context.md`) — read them for extra depth if they're there, but never wait on them and never refuse to run because they aren't.

## Accounts

- **Facebook Page:** `facebook.com/clad9` · **LinkedIn Page:** `linkedin.com/company/clad9`
- **Site:** clad9.com — every CTA lands on `/users/sign_up`
- Both Pages were created in September 2026 and started from **zero followers**

## The content map — 708 URLs across five factories

| Source | URLs | Pattern |
|---|---|---|
| Colours × occasion | 241 | `/colors/{color}` → `/colors/{color}/{occasion}` |
| Garment × occasion | 250 | `/style/{garment}` → `/style/{garment}/{occasion}` |
| Occasion × audience | 61 | `/what-to-wear/{occasion}/{audience}` |
| Season × audience capsules | 53 | `/capsule/{season}/{audience}` |
| Body shape × garment | 36 | `/body-type/{shape}/{garment}` |
| FAQ | 37 | `/faq/{slug}` |
| Blog | 12 | `/blog/{slug}` |
| Features | 9 | `/features/{feature}` |
| Alternatives | 5 | `/alternatives/{competitor}` |

Occasions everywhere: `casual-weekend`, `first-date`, `job-interview`, `wedding-guest`.
Audiences: big-tall-men, curvy-women, men, men-over-40, non-binary, petite-women, plus-size-women, tall-men, tall-women, teens, women, women-over-50.
Body shapes: pear, apple, hourglass, rectangle, inverted-triangle.

**Exploitable gap:** roughly 36 of ~48 colour pages and ~37 of ~49 garment pages exist but aren't linked from their own hub grids. Posts pointing at those orphans double as internal-linking wins — prefer them.

## The nine angles

1. **The visibility problem** — you don't own too few clothes, you can't see what you have
2. **Correct a standard piece of styling advice** — highest-performing shape in this voice
3. **A specific colour pairing, explained**
4. **One garment styled four ways**
5. **Occasion dressing for a specific audience** — narrow and high-intent
6. **Seasonal capsule**
7. **How the product actually works** — one feature, one mechanism, no adjectives
8. **The methodology / anti-slop post** — `/methodology` says every pairing is hand-curated before AI writes about it, and drafts too similar to existing ones are rewritten. Strongest differentiator Clad9 has; no competitor has an equivalent
9. **Cost-per-wear and wearing what you own** — without guilt

## Seasonal calendar

| Window | Lead with |
|---|---|
| Aug–Sep | Autumn capsule, transitional layering, "shed strategy" |
| Oct–Nov | Occasion dressing — weddings, parties, interviews |
| Dec–Jan | New-year declutter, cost-per-wear, clothing inventory |
| Feb–Apr | Colour analysis, "shop your closet", spring refresh |
| May–Jul | Travel capsules, packing lists, hot-weather occasions |

## Steps

1. **Establish what has already gone out.** Open both Pages and read the last 10 posts on each. This is the only record — there is no state file, deliberately, because a state file drifts and the Pages don't. Note angle, source page and opening construction for each.

2. **Check the season** against today's date. The seasonal angle leads — it's the one with a real reason to run now rather than in March.

3. **Pick the angles.** Default to one week: 3 posts alternating platform, plus one comment run. Never the same angle twice running on one platform, and never the same angle on both platforms in one week.

   If the user wants a different volume, or is scheduling repeated runs, size to what they ask and lean harder on rotation: at twice-daily cadence the nine angles cycle in under a week, so vary the **source page** within an angle rather than repeating the angle wholesale. With 241 colour pages and 250 garment pages the specificity is effectively inexhaustible.

4. **Bind each post to a real source URL** on clad9.com. Prefer the orphan colour and garment pages.

5. **Write the image brief** for each — the prompt shape and the aspect ratio for its platform (Facebook 3:4, LinkedIn 1:1).

6. **Sanity-check against the claim rules.** Any entry that would need a price, a user count or a testimonial to work is not viable — replace it.
   - **Never state a price.** There is no public pricing; `/pricing` 404s. Only "free to start" and "14-day free trial, no credit card required".
   - **Never invent social proof.** The site has no user counts, testimonials or press.
   - **Capture is batch photos, not a video walkthrough** — `/features` carries a stale line saying otherwise.
   - **Never claim it replaces a human stylist**, and never use guilt as a sustainability lever.

## Output

| # | Day | Platform | Angle | Source URL | Hook (one line) | Image brief | Ratio |
|---|---|---|---|---|---|---|---|

Then one short paragraph on why this set, now — the seasonal logic and what it's trying to establish while the Pages are cold.

Don't draft full post copy here; that happens in the posting skills, against the live page and a fresh read of the source.

## Standing priorities while the Pages are new

- **Comments outrank posts.** A post to zero followers reaches zero people. Weight the plan accordingly.
- **Give the methodology angle a slot regularly.** It's the thing competitors can't answer.
- **Specificity beats reach.** "What a petite woman wears to a job interview" will outperform "5 style tips" on a Page nobody follows yet.
