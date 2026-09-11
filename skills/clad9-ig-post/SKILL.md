---
name: clad9-ig-post
description: Write one original Instagram post for Clad9 - AI Wardrobe App and leave it staged in the composer, unsubmitted, with the image or carousel attached. Use when the user says "instagram post", "post to Clad9 instagram", "ig post", "do a Clad9 IG run", "make a carousel", or invokes /clad9-ig-post. Composes fresh copy from the brand rules and angle bank below — never by pasting stored text.
---

# Stage one Instagram post for Clad9

Everything needed is in this file. Longer-form versions of the same material sit beside it in this skill's own folder (`references/angle-bank.md`, `references/brand-context.md`, `references/platform-playbooks.md`) — read them for extra depth if they're there, but never wait on them and never refuse to run because they aren't.

## Accounts

- **Instagram:** `@clad9app` — display name **Clad9 — AI Wardrobe App**, matching the Facebook Page. Verify the handle on the first run of a session; `@clad9` is a different, unrelated account (Brazil, joined January 2023, dormant) and is **not** ours.
- **Site:** clad9.com — the bio link is `clad9.com/users/sign_up`
- Operated by Hadaa, Inc., the same company behind hadaa.app

## The identity trap — check every single time

Two traps stack here, and this is the worst failure this skill has.

1. **The browser is signed in to a Hadaa-associated Instagram.** Instagram's account switcher is the small avatar at the bottom of the left rail. Switch to Clad9 and confirm the composer shows the **C9 monogram** (cream ground, maroon and gold) before typing a single character.
2. **`@clad9` is not us.** If you ever find yourself on a profile with 0 posts and no bio, you are on the wrong account entirely — stop.

Verify visually. Posting Clad9 copy from Hadaa's Instagram, or into a stranger's account, is unrecoverable in a way a bad caption is not.

## What Clad9 is

An AI wardrobe app and digital closet. Batch-upload photos of your clothes; AI catalogs, background-removes and tags every garment. Upload a photo of yourself for body-shape and skin-tone analysis. Connect your calendar. It hands you a finished outfit each morning built from clothes you already own, matched to your body, colouring, the live weather and the event on your schedule.

Named features: Color Combinations for Clothes · How to Style Your Clothes · AI Wardrobe Capture · Daily AI Outfit Recommendations · Calendar-Aware Dressing · AI Personal Color Analysis · Body-Aware Styling · Virtual Try-On · AI Capsule Wardrobe Builder · Instant AI Outfit Feedback. Also: harmony scoring, weather "shed strategy", outfit collages and lookbooks, visual search, Style DNA, week planning, travel packing lists, cost-per-wear, gap analysis, resale estimates, a Chrome extension.

## The claim gate — reject the draft if it breaks any of these

1. **Never state a price.** There is no public pricing; `/pricing` 404s. You may say "free to start" and "14-day free trial, no credit card required" — nothing more, and never a figure.
2. **Never invent social proof.** No user counts, no testimonials, no press, no "join thousands". The site has none, and Instagram is where this temptation is strongest.
3. **Capture is batch photos, not a video walkthrough.** The `/features` page carries a stale line saying otherwise. Ignore it.
4. **Never claim to replace a human stylist.** The site explicitly refuses this.
5. **Never use guilt as a sustainability lever.** The site's own line: "no guilt, no lectures, no sacrifice to how good you look."
6. The "20% of your wardrobe 80% of the time" stat is uncited — attribute it softly ("studies suggest"), never as Clad9 data.

Rewrite rather than soften. If a claim can't be traced to a page on clad9.com, it isn't grounded.

## Voice — same brain, different mouth

The LinkedIn register does **not** transfer. There, the correction *is* the post. Here, the image is the post and the caption explains it. Same honesty, same specificity, less lecture.

**Keep:** negation-then-substitution, the em-dash correction move, concrete mechanisms, second person, owned vocabulary (visibility problem, cost-per-wear, undertone, neutral-anchored, harmony score, capsule, Style DNA, shed strategy).

**Drop:** the essay shape. Long stacked paragraphs get truncated at "… more" after roughly two lines and nobody expands them.

**Caption shape:**
- **Line 1 is the whole game** — under 125 characters, because that is what shows before the fold. Make it the correction or the concrete claim, never a preamble or a question.
- One blank line, then 2–4 short lines of substance.
- A soft close. "Link in bio" is fine here — unlike Facebook and LinkedIn, it is the native convention and costs no reach.
- **3–5 hashtags**, at the end of the caption. Instagram is the one platform of the three where hashtags belong in the body. Mix one broad (#CapsuleWardrobe), one specific (#ColourAnalysis), one branded (#Clad9). Vary them every run; an identical block every time reads as automation.
- At most one emoji. Usually none. No exclamation marks.

## Format — this is where Instagram actually differs

**Carousels are the default.** A single flat-lay is a weak Instagram post; a 4–6 card carousel that teaches something is the format that earns saves, and saves are what the algorithm rewards. Reach for a single image only when one picture genuinely makes the whole point.

Carousel shapes that fit the angle bank:

| Angle | Carousel |
|---|---|
| Colour pairing | Card 1 the two colours together · 2–4 one outfit each · last card the why |
| One garment four ways | Card 1 the garment alone · 2–5 one styling each |
| Seasonal capsule | Card 1 the full flat-lay · 2–N individual pieces with what each pairs with |
| Correct an advice cliché | Card 1 the cliché in plain type · 2 why it fails · 3–4 the mechanism |
| Cost-per-wear | Card 1 a sparse rail · 2–3 the arithmetic, honestly |

**Aspect ratio: 3:4.** Instagram's ideal feed portrait is 4:5, and **Flow does not offer 4:5** — its options are 16:9, 4:3, 1:1, 3:4, 9:16. 3:4 is the closest and Instagram accepts it without cropping the subject. Never generate 1:1 for feed unless the post is a carousel of square cards; square wastes vertical space in the feed.

**Every card must be legible at thumbnail size.** If the garments in a flat-lay are small enough to become mush at 160px, re-prompt closer.

**Reels** are outside this skill. Say so if asked rather than staging a bad one.

## Angle bank — rotate, never repeat consecutively

1. **The visibility problem** · 2. **Correct a standard piece of styling advice** · 3. **A specific colour pairing, explained** · 4. **One garment styled four ways** · 5. **Occasion dressing for a specific audience** · 6. **Seasonal capsule** · 7. **How the product actually works** · 8. **The methodology / anti-slop post** · 9. **Cost-per-wear and wearing what you own**

Angles **3, 4 and 6** are the strongest on Instagram — they are inherently visual and carousel-shaped. Angle 8 is the weakest here; it is an argument, and arguments belong on LinkedIn.

**Source pages** (708 URLs): `/colors/{color}[/{occasion}]` (241) · `/style/{garment}[/{occasion}]` (250) · `/what-to-wear/{occasion}/{audience}` (61) · `/capsule/{season}/{audience}` (53) · `/body-type/{shape}/{garment}` (36) · `/faq/{slug}` (37) · `/blog/{slug}` (12) · `/features/{feature}` (9) · `/alternatives/{competitor}` (5). Occasions: casual-weekend, first-date, job-interview, wedding-guest.

Seasonal lead: Aug–Sep autumn capsule and transitional layering · Oct–Nov occasion dressing · Dec–Jan declutter and cost-per-wear · Feb–Apr colour analysis and "shop your closet" · May–Jul travel capsules and packing.

## Steps

1. Open Instagram. **Switch identity and verify the C9 avatar and the `@clad9app` handle.**
2. **Read the last 10 posts.** Note angles, opening lines and hashtag sets — this is the de-duplication mechanism. Repeat none of the three. Also check what went out on Facebook and LinkedIn this week; the same angle should not run on all three in one week, though a *different cut* of the same source page is fine.
3. **Pick the angle** — from the content plan if one exists, otherwise seasonally appropriate and not recently used.
4. **Fetch the source page on clad9.com and read it.** Write from what it says, not from memory of the product.
5. **Decide single or carousel**, and write the card-by-card brief before generating anything.
6. **Write the caption.** Front-load line 1. Run the claim gate.
7. **Generate the images** — invoke `clad9-image-run` with a **3:4** brief per card. A post without images is not a post.
8. **Stage it** by the sequence below. **Stop. Do not publish.**

## Staging it — read this before touching the composer

**This flow has not been walked end to end yet.** Facebook's and LinkedIn's have, and they are documented precisely in `clad9-fb-post` and `clad9-li-post`. What follows is the shape those two share plus what is known about Instagram; **trust the screen over this section, and correct it afterwards** rather than forcing another platform's shape onto it.

What carries over and is not in doubt:

- **Stage the files into the session first.** `file_upload` rejects a path on the user's machine outright — *"only files this session is allowed to read can be uploaded"* — even for a granted folder. Run `device_stage_files` on the downloaded images and upload the `/mnt/user-data/uploads/...` paths it returns. This is the single most common failure.
- **Never click a visible "Select from computer" button.** It opens a native picker the browser tools cannot drive. `find` the `input[type=file]` and upload to it directly.
- **When the input does not exist yet**, the `find` returns a wrong element and `file_upload` fails with *"Element is not a file input."* That error means a dialog was not open, not that the path was bad. Open the dialog, then search again.

Instagram-specific, to verify on the first run and write down:

1. Instagram posts from the web via the **Create** button (the ✛ in the left rail), which opens a "Create new post" dialog with a drag-and-drop area and a **Select from computer** button.
2. For a carousel, upload **all cards in one `file_upload` call** so they land in order; the dialog also has a layers control for adding more afterwards.
3. The flow is Create → crop → filters/edit → **Next** → caption screen → **Share**. Stop on the caption screen with the caption typed. Never click Share.
4. **Alt text** is on the caption screen under *Accessibility*, per image. Set it for every card.
5. Instagram may show an **AI-generated content** disclosure toggle. Clad9's images are AI-generated and LinkedIn labels them automatically, so turning it on is the consistent choice — but it changes how the post presents publicly, so leave it as found and say so in the hand-over. The user decides.

## Hand over

One line: the angle, the source page, single or carousel, and that it is staged with images attached. Then the caption's first line only — the rest is on screen. Flag the AI-label state.

If anything in the staging section turned out to be wrong, say what actually happened and fix this file in the same run. A skill that documents a flow it has not walked is a liability; one that quietly stays wrong is worse.
