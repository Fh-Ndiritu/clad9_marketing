---
name: clad9-li-post
description: Write one original LinkedIn Page post for Clad9 and leave it staged in the composer, unsubmitted, with the image attached. Use when the user says "linkedin post", "post to Clad9 linkedin", "li post", "do a Clad9 LinkedIn run", or invokes /clad9-li-post. Composes fresh copy from the brand rules and angle bank below — never by pasting stored text.
---

# Stage one LinkedIn post for Clad9

Everything needed is in this file. Longer-form versions of the same material sit beside it in this skill's own folder (`references/angle-bank.md`, `references/brand-context.md`, `references/platform-playbooks.md`) — read them for extra depth if they're there, but never wait on them and never refuse to run because they aren't.

## Accounts

- **Page:** `linkedin.com/company/clad9` — the Page name is plain **Clad9** here (the Facebook Page uses the longer "Clad9 - AI Wardrobe App" form)
- **Site:** clad9.com — every CTA lands on `clad9.com/users/sign_up`
- Operated by Hadaa, Inc., the same company behind hadaa.app

**Post as the Page, not as Francis.** LinkedIn defaults to the personal profile. Confirm the identity selector at the top of the composer reads **Clad9** before typing. Francis also runs his own personal LinkedIn presence — this skill never posts there, and Page copy should not be cross-posted to it, since the two want different voices.

## What Clad9 is

An AI wardrobe app and digital closet. Batch-upload photos of your clothes; AI catalogs, background-removes and tags every garment. Upload a photo of yourself for body-shape and skin-tone analysis. Connect your calendar. It hands you a finished outfit each morning built from clothes you already own, matched to your body, colouring, the live weather and the event on your schedule.

Named features: Color Combinations for Clothes · How to Style Your Clothes · AI Wardrobe Capture · Daily AI Outfit Recommendations · Calendar-Aware Dressing · AI Personal Color Analysis · Body-Aware Styling · Virtual Try-On · AI Capsule Wardrobe Builder · Instant AI Outfit Feedback. Also: harmony scoring, weather "shed strategy", lookbooks, visual search, Style DNA, week planning, travel packing lists, cost-per-wear, gap analysis, resale estimates, a Chrome extension.

## The claim gate — reject the draft if it breaks any of these

1. **Never state a price.** There is no public pricing; `/pricing` 404s. Only "free to start" and "14-day free trial, no credit card required".
2. **Never invent social proof.** No user counts, no testimonials, no press. The site has none.
3. **Capture is batch photos, not a video walkthrough.** The `/features` page carries a stale line saying otherwise.
4. **Never claim to replace a human stylist.**
5. **Never use guilt as a sustainability lever.**
6. The "20% of your wardrobe 80% of the time" stat is uncited — attribute it softly, never as Clad9 data.

LinkedIn's audience is the likelier of the two to check a claim, and not overclaiming is Clad9's whole differentiator. Rewrite rather than soften.

## Voice — the blog register, not the homepage register

**Not this:** "the world's most complete AI wardrobe app", "the last wardrobe app you'll ever need."

**This:** dry, corrective, mechanical. Name the conventional advice, say why it fails, give the mechanism:

- "Most of us don't have a clothing problem — we have a visibility problem."
- "'Flattering' isn't a vague compliment — it's a specific, mechanical thing: creating visual balance between shoulders, waist, and hips."
- "A capsule built on paper is only as accurate as your memory of your own wardrobe — and nobody's memory of forty-plus items is that good."

Mechanics: em-dash for the correction move. Second person. Negation-then-substitution. Owned vocabulary: decision fatigue, visibility problem, cost-per-wear, gap analysis, undertone, seasonal palette, neutral-anchored, harmony score, capsule, Style DNA, shed strategy. Short declaratives, no exclamation marks. Polite about competitors.

## Angle bank — rotate, never repeat consecutively

1. **The visibility problem** · 2. **Correct a standard piece of styling advice** · 3. **A specific colour pairing, explained** · 4. **One garment styled four ways** · 5. **Occasion dressing for a specific audience** · 6. **Seasonal capsule** · 7. **How the product actually works** · 8. **The methodology / anti-slop post** · 9. **Cost-per-wear and wearing what you own**

Angle 8 is the strongest on LinkedIn specifically. `/methodology` states that every colour pairing and fit relationship is hand-curated *before* any AI writes about it, and that new explanations are checked against every existing one by embedding similarity and rewritten if too close. In a feed full of AI-slop complaints, no competitor has an equivalent to point at.

**Source pages** (708 URLs): `/colors/{color}[/{occasion}]` (241) · `/style/{garment}[/{occasion}]` (250) · `/what-to-wear/{occasion}/{audience}` (61) · `/capsule/{season}/{audience}` (53) · `/body-type/{shape}/{garment}` (36) · `/faq/{slug}` (37) · `/blog/{slug}` (12) · `/features/{feature}` (9) · `/alternatives/{competitor}` (5). Occasions: casual-weekend, first-date, job-interview, wedding-guest.

Seasonal lead: Aug–Sep autumn capsule and transitional layering · Oct–Nov occasion dressing · Dec–Jan declutter and cost-per-wear · Feb–Apr colour analysis and "shop your closet" · May–Jul travel capsules and packing.

## Steps

1. Open the Page. **Confirm the composer identity reads Clad9.**
2. **Read the last 10 posts.** Repeat neither angle nor opening construction. Also check what went out on Facebook recently — the same angle should not run on both platforms in one week.
3. **Pick the angle.**
4. **Fetch the source page on clad9.com and read it.** Write from what it says.
5. **Write the copy.** **The first two lines carry the post** — LinkedIn truncates at "…see more" around 200 characters, so the correction goes in line one, not line four. 120–200 words. One or two sentences per paragraph, blank line between. At most three hashtags at the end, varied between runs. No "Thoughts?", no "Agree?", no engagement bait.
6. **Run the claim gate** above.
7. **Generate the image** — invoke `clad9-image-run` with a **1:1** brief.
8. **Stage it.** Type the copy, attach the image. **Stop. Do not click Post.**
9. **Prepare the first comment** with the source link — LinkedIn suppresses outbound links in the body too.

## Hand over

One line: the angle, the source page, that it's staged. Plus the first-comment text.
