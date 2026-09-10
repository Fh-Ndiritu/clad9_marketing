---
name: clad9-image-run
description: Generate marketing images for Clad9 in the user's Google Flow project and download them ready to attach to a post. Use when the user says "generate an image", "make the image", "image run", "create visuals for the post", "flow image", or invokes /clad9-image-run. Also called automatically by the Clad9 posting skills when a post needs a visual.
---

# Generate a Clad9 marketing image in Google Flow

Everything needed is in this file. The UI below was verified live on 2026-09-10 in the Clad9 project; if a label doesn't match what's on screen, trust the screen and note the drift.

**Project:** `https://flow.google.com/project/7d6deb2c-f424-48f2-98d1-c52b13966f6a` (named "Clad9")

## Verified facts

- Image generation on this account costs **0 credits** — the picker says "Generating will use 0 credits". Generate freely; never ration.
- A single 1:1 Nano Banana Pro image takes **~15–20 seconds**.
- Models available: **Nano Banana Pro** (default, and the right choice), Nano Banana 2, Nano Banana 2 Lite.
- Aspect ratios in the Image picker are exactly **16:9, 4:3, 1:1, 3:4, 9:16**. There is **no 4:5** — use **3:4** for portrait.
- Output count: **x1, x2, x3, x4**.
- Flow auto-titles each asset from the prompt.

## The UI

**Left sidebar:** All media · Images · Characters · Scenes · Tools · Trash · Collapse.

**Prompt box (bottom centre):** placeholder "What do you want to create?", a `+` button, an **Agent** toggle, and on the right a chip showing model / aspect ratio / count (e.g. "Nano Banana Pro ☐ x1"), then a **→** submit arrow.

**Clicking the model chip** opens the picker: an **Image | Video** toggle, the five aspect-ratio buttons, the model dropdown, the x1–x4 row, and the credit line.

**Edit View** (click an asset): image centred, **Crop** and **Select** tools on the left, a "What do you want to change?" box for conversational editing, and top right — favourite, share, delete, **download (⤓)**, **Hide history**, **Done**.

**To generate a *new* image while in Edit View, click Done first.** The "What do you want to change?" box edits the asset you're looking at — it does not start a fresh generation, and the aspect-ratio chip there applies to the edit, not to a new image.

## Steps

1. **Open the project URL. Confirm the header reads Clad9** before generating — otherwise assets scatter across the user's account.
2. **Check the visible-watermark toggle is off** (menu under the profile picture, top right) if this is the session's first run. Otherwise every image ships stamped. The invisible SynthID watermark stays and should not be tampered with.
3. **Click the model chip → Image → aspect ratio → Nano Banana Pro → x2.**

   | Destination | Ratio |
   |---|---|
   | Facebook post | **3:4** |
   | LinkedIn post | **1:1** |
   | Landscape | 16:9 |
   | Story / Reel | 9:16 |

4. **Write the prompt** (recipe below), click the **→** arrow, wait ~20s.
5. **Judge it honestly.** Reject and re-prompt on garbled text, warped or impossible garments, extra limbs, a visible watermark, or a palette drifted off-brand. Generating again is free — say plainly if an image isn't good enough rather than shipping it.
6. **Download.** Click the **⤓** icon in Edit View. The icon alone does not download — it opens a small resolution menu:

   | Option | Use it? |
   |---|---|
   | **1K — Original size** | **Yes.** This is the image as generated, no upscale artefacts, ~700 KB. Ample for both Pages. |
   | 2K — Upscaled | Only if the user asks for print or a large hero. |
   | 4K — Upscaled | Locked behind **Upgrade**. Don't. |

   Click **1K / Original size**, then confirm the file arrived before moving on. It lands in the Mac's **`~/Downloads`** as `<Flow asset title>_<yyyymmddhhmmss>.jpeg` — **JPEG, not PNG**, whatever the source format. Flow titles the asset from the prompt, so the filename is guessable but never assume it: list the folder newest-first and take the top entry.

   **Ask the user before the first download in a session.** Once they agree, continue for the rest of that run without asking again.

7. **Put the file somewhere the browser can upload it** — this is the step that has failed before, and getting it wrong loses the whole run's work. See below.

## Getting the file where the composer can reach it

The browser's `file_upload` will only take files this session is allowed to read. **A raw path on the user's machine is rejected**, even for a folder they've just granted:

- ✗ `/Users/fh/Downloads/Autumn_capsule_wardrobe_flat-lay_20260910184250.jpeg` → *"only files this session is allowed to read can be uploaded"*
- ✓ `/mnt/user-data/uploads/Downloads/Autumn_capsule_wardrobe_flat-lay_20260910184250.jpeg`

So, in order:

1. **`~/Downloads` is not a connected folder by default.** Request access to it once per session (`device_request_folder_access` on `~/Downloads`); it's granted immediately and holds for the rest of the session.
2. **Find the file.** `ls -lt "$HOME/mnt/Downloads" | head -5` in the device shell. Don't list the folder with `device_list_dir` — this user's Downloads is enormous and the listing blows the token budget.
3. **Stage it into the session** with `device_stage_files`. It returns a `stagedPath` under `/mnt/user-data/uploads/...`.
4. **Hand that staged path** to the posting skill. That — not the Mac path — is what gets uploaded.

## Report

Give the posting skill: the **staged path**, the aspect ratio, and a one-line description of what's actually in the frame (it becomes the alt text).

## Prompt recipe

Google's formula for Nano Banana: **[Subject] + [Action] + [Location/context] + [Composition] + [Style]**.

House style, matching clad9.com's cream-and-editorial aesthetic:

> `[Subject and garments, naming fabrics] on a warm cream linen backdrop, [arrangement]. [Composition], soft diffused daylight from the left, subtle natural shadows. Editorial fashion magazine style, shot on medium-format film, fine grain, muted warm colour grading.`

A verified example that produced an on-brand result:

> *Overhead flat-lay of a small capsule wardrobe on a warm cream linen backdrop: a navy wool blazer, a white cotton t-shirt, indigo straight-leg jeans, tan leather ankle boots, and a camel wool scarf, arranged in a neat evenly-spaced grid. Centre-framed, soft diffused daylight from the left, subtle natural shadows. Editorial fashion magazine style, shot on medium-format film, fine grain, muted warm colour grading.*

**Rules that matter:**
- **Name the fabric, not the garment** — "navy wool blazer", never just "blazer". Biggest single quality lever for clothing.
- **Use positive framing** — "empty cream backdrop", never "no clutter".
- **Control the camera with photographic terms** — overhead, centre-framed, shallow depth of field (f/1.8), medium-full shot.
- Keep to Clad9's palette: cream, camel, navy, burgundy, olive, charcoal, tan.

## Prompt shape by angle

| Angle | Shape |
|---|---|
| Capsule / what-you-own | Overhead flat-lay grid of 5–8 named garments on cream linen |
| Colour pairing | Two or three folded garments in the exact colours, close-up, fabric texture visible |
| One garment styled four ways | Four small flat-lays in a 2×2 grid on one backdrop |
| Product mechanism | Hands-only — folding, sorting, hanging. No UI mockups |
| Cost-per-wear / analytics | A sparse, almost-empty rail with a few well-worn pieces, warm light |
| Seasonal | Same recipe, seasonal fabrics and palette (wool and tweed for autumn, linen and cotton for summer) |

## People in images

- **Prefer flat-lays and crops over generated people.** They age better, avoid uncanny faces, and keep attention on the clothes — which is the product.
- Generating anonymous, synthetic adult models is permitted. If a face must appear, prefer a crop that excludes it — shoulders-down, hands, or a back view.
- **Never** prompt for a named person, a celebrity, or a lookalike of a real public figure — Google blocks generating prominent people outright.
- **Never** generate minors.
- **Never** upload photos of real people for image-to-image without their consent.

## Consistency across a campaign

Generate the base image once, then reference it with `@` in later prompts (the `@` key opens the asset picker), or save it into **Characters** for a recurring model.
