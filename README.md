# Clad9 Marketing

Content strategy and posting automation for **Clad9** (clad9.com), the AI wardrobe app — across its Facebook Page and LinkedIn Page, with marketing images generated in Google Flow.

Built from a full crawl of the live site on 2026-09-10: 708 URLs across five programmatic factories, a 12-post blog, ten named features, and a published methodology page.

## Skills

| Skill | What it does |
|---|---|
| `/clad9-brand-refresh` | Re-crawls clad9.com and rewrites the brand context from the live site. Run it when the site changes — especially if pricing ever appears. |
| `/clad9-content-plan` | Builds the rolling queue: which angle, which source page, which platform, in what order. |
| `/clad9-image-run` | Generates a marketing image in the Clad9 Google Flow project and downloads it. |
| `/clad9-fb-post` | Writes and stages one Facebook Page post, unsubmitted. |
| `/clad9-li-post` | Writes and stages one LinkedIn Page post, unsubmitted. |
| `/clad9-comment-run` | Finds 4–5 worthwhile posts and stages a comment into each, unsubmitted. |

A typical cycle: `/clad9-content-plan` once, then `/clad9-fb-post` and `/clad9-li-post` against it, with `/clad9-comment-run` in between.

## How it behaves

**Nothing publishes itself.** Every skill writes the copy, attaches the image and leaves the composer open. You press Post. That holds for comments too.

**Every post is grounded in a real page.** Copy is composed fresh from the angle bank and the source URL on clad9.com — never pasted from a library. If a claim can't be traced to a page, it gets rewritten.

**De-duplication comes from the Pages themselves.** Before writing, each skill reads the last 10 posts and refuses to repeat an angle or an opening construction. There's no state file to drift out of sync.

## The rules it will not break

- **Never states a price.** Clad9 has no public pricing — `/pricing` 404s. Only "free to start" and "14-day free trial, no credit card required".
- **Never invents social proof.** No user counts, no testimonials, no press. The site has none.
- **Never describes capture as a video walkthrough.** It's batch photo upload; the `/features` page carries a stale line saying otherwise.
- **Never claims to replace a human stylist**, and never uses guilt as a sustainability lever. The site explicitly refuses both.

## How the skills carry their knowledge

**Belt and braces.** Two independent copies, because either one alone has failed:

1. **Inline in each `SKILL.md`** — brand facts, voice rules, claim gate, angle bank, Flow steps. The skill body is the only thing guaranteed to reach the model at runtime, so a skill is fully operable from its body alone.
2. **`skills/<skill>/references/`** — longer-form versions, sitting *inside each skill's own folder*, the same layout `hadaa-marketing` uses. References at the plugin root do **not** travel with a skill; a session that receives only the skill's subtree sees a flat directory.

Skills treat the reference files as optional depth and never block when they're absent.

The trade-off is duplication — `brand-context.md` appears in four skill folders, and the price and voice rules appear in several `SKILL.md` files. `/clad9-brand-refresh` names every file that needs editing when the facts change.

## Setup notes

**Google Flow** — the project is `flow.google.com/project/7d6deb2c-f424-48f2-98d1-c52b13966f6a`. Image generation costs 0 credits on this account and takes about 20 seconds. Check the visible-watermark toggle is off before a batch.

**The image pipeline, end to end** — this is the part that has broken most often, so it's written out precisely in `clad9-image-run`:

Flow ⤓ → **1K / Original size** (the icon alone doesn't download; it opens a resolution menu) → JPEG lands in `~/Downloads` → grant access to `~/Downloads` → **stage the file into the session** → upload the `/mnt/user-data/uploads/...` path, never the `/Users/...` one.

On LinkedIn the file input only exists **after** the Editor modal is open; searching for it earlier returns the wrong element. Alt text goes on before Next. Flow's C2PA provenance badge stays.

**Facebook identity trap** — the Clad9 Page runs under the personal profile that also administers the Hadaa.app Page, and every new browser tab defaults to Hadaa. Each skill switches identity and verifies the C9 avatar before typing. If you ever see Hadaa's avatar in a Clad9 composer, stop.

**Voice** — social copy uses the blog/methodology register, not the homepage sales voice. Dry, corrective, specific. "Most of us don't have a clothing problem — we have a visibility problem."
