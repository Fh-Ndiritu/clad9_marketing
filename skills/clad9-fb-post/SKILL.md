---
name: clad9-fb-post
description: Write one original Facebook Page post for Clad9 - AI Wardrobe App and leave it staged in the composer, unsubmitted, with the image attached. Use when the user says "facebook post", "post to Clad9 facebook", "fb post", "do a Clad9 FB run", or invokes /clad9-fb-post. Composes fresh copy from the brand rules and angle bank below — never by pasting stored text.
---

# Stage one Facebook post for Clad9

Everything needed is in this file. Longer-form versions of the same material sit beside it in this skill's own folder (`references/angle-bank.md`, `references/brand-context.md`, `references/platform-playbooks.md`) — read them for extra depth if they're there, but never wait on them and never refuse to run because they aren't.

## Accounts

- **Page:** `facebook.com/clad9` (fallback `facebook.com/profile.php?id=61594427152424`)
- **Site:** clad9.com — every CTA lands on `clad9.com/users/sign_up`
- Operated by Hadaa, Inc., the same company behind hadaa.app

## The identity trap — check every single time

The Page runs under the personal profile "Dennis Mutahi", which also administers the **Hadaa.app** Page, and **every new browser tab defaults to Hadaa.app**. Before typing anything: click the avatar top right → switch to Clad9 → confirm the composer avatar shows the **C9 monogram** (cream ground, maroon and gold C9). Verify visually. Posting Clad9 copy as Hadaa is the worst failure this skill has.

## What Clad9 is

An AI wardrobe app and digital closet. Batch-upload photos of your clothes; AI catalogs, background-removes and tags every garment. Upload a photo of yourself for body-shape and skin-tone analysis. Connect your calendar. It hands you a finished outfit each morning built from clothes you already own, matched to your body, colouring, the live weather and the event on your schedule.

Named features: Color Combinations for Clothes · How to Style Your Clothes · AI Wardrobe Capture · Daily AI Outfit Recommendations · Calendar-Aware Dressing · AI Personal Color Analysis · Body-Aware Styling · Virtual Try-On · AI Capsule Wardrobe Builder · Instant AI Outfit Feedback. Also: harmony scoring, weather "shed strategy", outfit collages and lookbooks, visual search, Style DNA, week planning, travel packing lists, cost-per-wear, gap analysis, resale estimates, a Chrome extension.

## The claim gate — reject the draft if it breaks any of these

1. **Never state a price.** There is no public pricing; `/pricing` 404s. You may say "free to start" and "14-day free trial, no credit card required" — nothing more, and never a figure.
2. **Never invent social proof.** No user counts, no testimonials, no press. The site has none.
3. **Capture is batch photos, not a video walkthrough.** The `/features` page carries a stale line saying otherwise. Ignore it.
4. **Never claim to replace a human stylist.** The site explicitly refuses this.
5. **Never use guilt as a sustainability lever.** The site's own line: "no guilt, no lectures, no sacrifice to how good you look."
6. The "20% of your wardrobe 80% of the time" stat is uncited — attribute it softly ("studies suggest"), never as Clad9 data.

Rewrite rather than soften. If a claim can't be traced to a page on clad9.com, it isn't grounded.

## Voice — the blog register, not the homepage register

**Not this:** "the world's most complete AI wardrobe app", "the last wardrobe app you'll ever need."

**This:** dry, corrective, mechanical. Name the conventional advice, say why it fails, replace it with a concrete mechanism. Real examples from the site:

- "Most of us don't have a clothing problem — we have a visibility problem."
- "'Flattering' isn't a vague compliment — it's a specific, mechanical thing: creating visual balance between shoulders, waist, and hips."
- "Most capsule wardrobe advice stops at a number — 'own 30 pieces' — and leaves the actual selection up to you. The number was never the point."

Mechanics: em-dash for the correction move ("not X — Y"). Second person throughout. Negation-then-substitution is the core structure. Owned vocabulary: decision fatigue, visibility problem, cost-per-wear, gap analysis, undertone, seasonal palette, neutral-anchored, harmony score, capsule, Style DNA, shed strategy. Short declaratives. No exclamation marks. No hashtags on Facebook. At most one emoji, usually none. Polite about competitors, always.

## Angle bank — rotate, never repeat consecutively

1. **The visibility problem** — you don't own too few clothes, you can't see what you have
2. **Correct a standard piece of styling advice** — the highest-performing shape in this voice
3. **A specific colour pairing, explained** — from `/colors/{color}/{occasion}`
4. **One garment styled four ways** — from `/style/{garment}`
5. **Occasion dressing for a specific audience** — from `/what-to-wear/{occasion}/{audience}`
6. **Seasonal capsule** — from `/capsule/{season}/{audience}`
7. **How the product actually works** — one feature, one mechanism, no adjectives
8. **The methodology / anti-slop post** — from `/methodology`; the strongest differentiator Clad9 has
9. **Cost-per-wear and wearing what you own** — the money angle, without guilt

**Source pages** (708 URLs): `/colors/{color}` and `/colors/{color}/{occasion}` (241) · `/style/{garment}[/{occasion}]` (250) · `/what-to-wear/{occasion}/{audience}` (61) · `/capsule/{season}/{audience}` (53) · `/body-type/{shape}/{garment}` (36) · `/faq/{slug}` (37) · `/blog/{slug}` (12) · `/features/{feature}` (9) · `/alternatives/{competitor}` (5). The four occasions everywhere: casual-weekend, first-date, job-interview, wedding-guest.

Seasonal lead: Aug–Sep autumn capsule and transitional layering · Oct–Nov occasion dressing · Dec–Jan declutter and cost-per-wear · Feb–Apr colour analysis and "shop your closet" · May–Jul travel capsules and packing.

## Steps

1. Open the Page. **Switch identity and verify the C9 avatar.**
2. **Read the last 10 posts.** Note angles and opening constructions — this is the de-duplication mechanism. Repeat neither.
3. **Pick the angle** — from the content plan if one exists, otherwise seasonally appropriate and not recently used.
4. **Fetch the source page on clad9.com and read it.** Write from what it says, not from memory of the product. This is what keeps posts specific and true.
5. **Write the copy.** Open on the correction or observation — no "Did you know", no preamble. 60–120 words. The hook must land inside the first 250 characters, before Facebook's fold. Short paragraphs, blank line between.
6. **Run the claim gate** above.
7. **Generate the image** — invoke `clad9-image-run` with a **3:4** brief matched to the angle. **A post without an image is not finished.** Get the staged path back before touching the composer.
8. **Type the copy**, then **attach the image** by the sequence below.
9. **Stop. Do not click Post.**
10. **Prepare the first comment** carrying the source link — Facebook suppresses reach on posts with outbound links in the body. Hand the text to the user to paste after they publish.

## Attaching the image — verified 2026-09-10

**Facebook is easier than LinkedIn here, and the difference matters.** LinkedIn hides its file input until a modal opens; **Facebook's is already in the DOM** as soon as the Create post dialog is up. Don't go looking for a modal — there isn't one.

1. **Open the composer** — click "What's on your mind?" on the Page. The **Create post** dialog opens with the C9 avatar, a **Public** selector and an **AI label** control.
2. **Type the copy first**, then attach — attaching first makes the text area harder to hit.
3. **`find` the file input straight away**: *"hidden file input for photo/video upload in the Create post dialog"*. It comes back as the input behind the **Photo/video** button. No clicking needed.
4. **Never click the green Photo/video icon** — it opens a native macOS file picker the browser tools cannot see or drive. The `find` → `file_upload` route bypasses it entirely.
5. **`file_upload`** that ref with the **staged** `/mnt/user-data/uploads/...` path from `clad9-image-run`.
6. **Scroll down inside the dialog and confirm the preview** sits under the copy. Never report a post staged without seeing it.
7. **Leave it on `Next`.** Facebook's flow is Next → Post, two clicks; stopping at Next keeps both out of your hands.

**Facebook has no alt-text field in this composer** (LinkedIn does — set it there). Facebook auto-generates one.

## The AI label

The Create post dialog carries an **AI label off / on** control. Clad9's images are AI-generated, LinkedIn stamps its own content-credentials badge on them automatically, and the methodology angle is built on being straight about how things are made — so **turning it on is the consistent choice**.

It changes how the post presents publicly, so **don't flip it silently**: leave it as found, and say in the hand-over that it's off and that turning it on would match LinkedIn. The user decides.

## Hand over

One line: the angle, the source page, and that it's staged **with the image attached**. Plus the first-comment text. Don't paste the whole post back — it's on screen.
