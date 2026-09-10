---
name: clad9-fb-post
description: Write one original Facebook Page post for Clad9 and leave it staged in the composer, unsubmitted, with the image attached. Use when the user says "facebook post", "post to Clad9 facebook", "fb post", "do a Clad9 FB run", or invokes /clad9-fb-post. Composes fresh copy from the brand context and angle bank — never by pasting stored text.
---

# Stage one Facebook post for Clad9

## Read first

> Paths here are relative to this skill's own folder — the base directory announced when the skill loads. If a path doesn't resolve, locate the plugin directory (the one containing `.claude-plugin/plugin.json`) and read `references/` from there. Never proceed on remembered facts if these files can't be read — say so and stop.

- `../../references/brand-context.md` — voice, the ten features, the claim rules
- `../../references/angle-bank.md` — the nine angles and the content map
- `../../references/platform-playbooks.md` — Facebook section, including the identity trap

## Steps

1. **Open the Page** — `facebook.com/clad9`, falling back to `facebook.com/profile.php?id=61594427152424`.

2. **Switch identity, then verify it visually.** Every new tab defaults to the Hadaa.app Page. Click the avatar top right, switch to Clad9, and confirm the composer avatar shows the **C9 monogram** — cream, maroon and gold. Do not type a single character until you have seen it. Posting Clad9 copy as Hadaa is the worst failure mode this skill has.

3. **Read the last 10 posts.** Note the angles and the opening constructions. Whatever you write must not repeat either.

4. **Pick the angle.** From the content plan if one exists, otherwise from the angle bank — seasonally appropriate, not used recently.

5. **Read the source page** on clad9.com. Write from what it actually says. This is what keeps posts specific and claims true; do not write from memory of the product.

6. **Write the copy.**
   - Blog/methodology register: dry, corrective, specific. Name the conventional advice, say why it fails, give the mechanism.
   - Open on the correction or the observation. No "Did you know", no preamble.
   - 60–120 words. The hook must land inside the first 250 characters, before Facebook's fold.
   - Short paragraphs, blank line between.
   - Em-dash for the correction move. Second person. No exclamation marks, no hashtags, at most one emoji and usually none.
   - Soft close. No hard CTA.

7. **Run the claim gate.** Reject the draft if it states a price, invents a user count or testimonial, describes capture as a video walkthrough, claims to replace a human stylist, or uses guilt as a sustainability lever. Rewrite rather than soften.

8. **Generate and attach the image** — invoke `clad9-image-run` with a 3:4 brief matched to the angle.

9. **Stage it.** Click the composer, type the copy, attach the image. **Stop there.** Do not click Post.

10. **Prepare the first comment** containing the source link — Facebook suppresses reach on posts with outbound links in the body. Give the user the comment text to paste after they publish; do not post it yourself.

## Hand over

Tell the user the post is staged and ready, name the angle and the source page in one line, and give them the first-comment text. Do not paste the whole post back at them — it is on screen.
