---
name: clad9-ig-post
description: Write one original Instagram post for Clad9 - AI Wardrobe App and leave it staged in the composer, unsubmitted, with the image or carousel attached. Use when the user says "instagram post", "post to Clad9 instagram", "ig post", "do a Clad9 IG run", "make a carousel", or invokes /clad9-ig-post. Composes fresh copy from the brand rules and angle bank below — never by pasting stored text.
---

# Stage one Instagram post for Clad9

Everything needed is in this file. Longer-form versions of the same material sit beside it in this skill's own folder (`references/angle-bank.md`, `references/brand-context.md`, `references/platform-playbooks.md`) — read them for extra depth if they're there, but never wait on them and never refuse to run because they aren't.

## Accounts

- **Instagram:** **`@clad9_app`** — note the **underscore**. Display name is currently **Clad9**.
- **Site:** clad9.com
- Operated by Hadaa, Inc., the same company behind hadaa.app

**Two handles that are not us.** `@clad9` is an unrelated dormant account (Brazil, joined January 2023, no posts). `@clad9app` — no underscore — does not exist. Only `@clad9_app` is ours.

## Profile fields: what web can and cannot set — verified 2026-09-17

Instagram's web **Edit profile** (`instagram.com/accounts/edit/`) is missing fields the mobile app has. Don't burn calls hunting for them:

| Field | Web? |
|---|---|
| Bio | **Yes** — edit, then **Submit** at the bottom of the page. Nothing saves until Submit. |
| Profile photo | **Yes** — `find` the hidden input behind **Change photo**, then `file_upload`. Confirms with "Profile photo added." |
| **Website / link** | **No.** The field renders but is disabled: *"Editing your links is only available on mobile."* |
| **Name** (the searchable display name) | **No.** Not present on web at all. |

So the bio must carry the URL as plain text — `clad9.com — free to start` — or the profile has no address at all until someone opens the mobile app. Say this in the hand-over rather than quietly leaving a bio whose "link in bio" points at nothing.

The **AI-generated profile** toggle on that page is about a profile that *features an AI-generated person*. Clad9's is a monogram and flat-lays, so it stays **off**. That is a different control from the per-post AI label below, which does apply.

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

**Aspect ratio: generate 3:4, publish at 4:5.** Instagram's feed portrait is **4:5**, and **Flow does not offer it** — its options are 16:9, 4:3, 1:1, 3:4, 9:16. So generate at **3:4** and **crop to 4:5 in the composer** (see the staging steps). 3:4 is *taller* than Instagram's limit, so it will not publish uncropped — leave a little headroom around the garment when prompting, because the crop takes it off the top and bottom. Never generate 1:1 for feed unless the whole carousel is square; square wastes vertical space.

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

## Staging it — walked end to end 2026-09-17

**Which path `file_upload` accepts.** Only `/mnt/user-data/uploads/...`. Both of these are rejected with *"only files this session is allowed to read can be uploaded"*:

- a path on the user's machine (`/Users/fh/Downloads/...`), even for a folder just granted
- **`/mnt/user-data/outputs/...`** — the outputs folder is *not* readable by the uploader either

So: `device_stage_files` for anything downloaded from Flow, or a plain `cp` into `/mnt/user-data/uploads/` for anything generated in the container. Upload that path.

**Never click a visible "Select from computer" button** — native picker, undrivable. `find` the input and upload to it.

### The flow

1. **Create** — the plus in the left rail. A **Create new post** dialog opens. Its `input[type=file]` is in the DOM as soon as the dialog is up: `find` *"hidden file input associated with Select from computer button"*.
2. **Upload every card in one `file_upload` call** — they land in carousel order, so pass them in reading order.
3. **Crop — do not skip this.** It defaults to **1:1** and will silently square-crop the cards. Click the crop icon (bottom left) and choose **4:5**.

   **Why 4:5 and not Original:** Instagram accepts 1.91:1 down to 4:5. Flow's **3:4 sits outside that range**, so "Original" is not safe; 4:5 is the closest supported ratio and crops only slightly. The ratio applies to the whole carousel.
4. **Filters** — leave **Original** selected; the Flow grading is already the house look. **Next.**
5. **Caption screen.** Type the caption.
6. **AI label — turn it ON.** Instagram's own wording: *"This label is required for realistic photos and videos made with AI."* Our flat-lays are exactly that, so this is a platform requirement, not a brand preference — and **not** the same as Facebook's optional toggle. Turn it on, and say so in the hand-over.
7. **Alt text** — expand **Accessibility**, below the AI label, for one field per card. Fill every one; Instagram otherwise auto-generates something vague.
8. **Stop. Never click Share.**

### Two traps in this composer

- **Never press Escape.** It does not dismiss a dropdown — it opens **"Discard post?"**, and the wrong click there loses the upload, the crop and the caption. If it appears, click **Cancel**.
- **The hashtag autocomplete covers the lower half of the panel** the moment you type a `#`, hiding the AI label and Accessibility sections. Dismiss it by clicking a **non-hashtag line of the caption** — not Escape.

## Hand over

One line: the angle, the source page, single or carousel, and that it is staged with images attached. Then the caption's first line only — the rest is on screen. Flag the AI-label state.

If anything in the staging section turned out to be wrong, say what actually happened and fix this file in the same run. A skill that documents a flow it has not walked is a liability; one that quietly stays wrong is worse.
