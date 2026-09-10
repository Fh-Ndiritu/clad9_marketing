# Google Flow — image generation manual

UI verified live on 2026-09-10 in the Clad9 project. If a label below doesn't match what's on screen, trust the screen and note the drift.

**Project:** https://flow.google.com/project/7d6deb2c-f424-48f2-98d1-c52b13966f6a (named "Clad9")

## Verified facts

- Image generation on this account costs **0 credits**. The picker states "Generating will use 0 credits". Generate freely; do not ration.
- A single 1:1 Nano Banana Pro image takes **~15–20 seconds**.
- All three image models are available — **Nano Banana Pro** (default), Nano Banana 2, Nano Banana 2 Lite. Pro is the default and the right choice for marketing stills.
- Aspect ratios offered in the Image picker are exactly: **16:9, 4:3, 1:1, 3:4, 9:16**. There is **no 4:5** — use **3:4** for portrait feed images.
- Output count: **x1, x2, x3, x4**.
- Flow auto-titles each asset from the prompt (e.g. "Capsule wardrobe flat lay arrang…").

## The UI

**Left sidebar:** All media · Images · Characters · Scenes · Tools · Trash · Collapse.
**Prompt box (bottom centre):** placeholder "What do you want to create?", a `+` button, an **Agent** toggle, and on the right a chip showing the current model, aspect ratio and count (e.g. "Nano Banana Pro ☐ x1"), then a **→** submit arrow.
**Clicking the model chip** opens the picker: an **Image | Video** toggle, the five aspect-ratio buttons, the model dropdown, the x1–x4 row, and the credit line.

**Edit View** (click an asset, or hover → **⋮**): the image centred, **Crop** and **Select** tools down the left, a "What do you want to change?" prompt box for conversational editing, and top-right — favourite (♡), share, delete (🗑), **download (⤓)**, **Hide history**, **Done**. The right-hand panel shows version history with the prompt.

## Generating an image

1. Open the project URL. Confirm the header reads **Clad9**.
2. Click the model chip in the prompt box.
3. Ensure **Image** is selected (not Video).
4. Pick the aspect ratio for the destination — see the table below.
5. Leave the model on **Nano Banana Pro**. Set the count to **x2** so there's a choice.
6. Click the prompt box, type the prompt, press the **→** arrow.
7. Wait ~20s. The asset appears top-left of the media grid.
8. Review it before using it. Reject anything with garbled text, warped garments, extra limbs, or a visible watermark.

## Aspect ratio by destination

| Destination | Ratio |
|---|---|
| Facebook Page post (feed) | **3:4** portrait, or 1:1 |
| LinkedIn Page post | **1:1**, or 4:3 |
| Either platform, landscape/link-style | 16:9 |
| Story / Reel cover | 9:16 |

## Prompt recipe

Google's own formula for Nano Banana: **[Subject] + [Action] + [Location/context] + [Composition] + [Style]**.

The house style for Clad9, matching the site's cream-and-editorial aesthetic:

> `[Subject and garments, naming fabrics] on a warm cream linen backdrop, [arrangement]. [Composition], soft diffused daylight from the left, subtle natural shadows. Editorial fashion magazine style, shot on medium-format film, fine grain, muted warm colour grading.`

A verified working example that produced an on-brand result:

> *Overhead flat-lay of a small capsule wardrobe on a warm cream linen backdrop: a navy wool blazer, a white cotton t-shirt, indigo straight-leg jeans, tan leather ankle boots, and a camel wool scarf, arranged in a neat evenly-spaced grid. Centre-framed, soft diffused daylight from the left, subtle natural shadows. Editorial fashion magazine style, shot on medium-format film, fine grain, muted warm colour grading.*

**Rules that matter:**
- **Name the fabric, not the garment.** "navy wool blazer", not "blazer". This is the single biggest quality lever for clothing.
- **Use positive framing.** "empty cream backdrop", never "no clutter".
- **Control the camera with photographic terms** — overhead, centre-framed, shallow depth of field (f/1.8), medium-full shot.
- Keep the palette in Clad9's range: cream, camel, navy, burgundy, olive, charcoal, tan.

## Prompt shapes by angle

| Angle | Shape |
|---|---|
| Capsule / what-you-own | Overhead flat-lay grid of 5–8 named garments on cream linen |
| Colour pairing | Two or three folded garments in the exact colours, close-up, fabric texture visible |
| Single garment styled four ways | Four small flat-lays in a 2×2 grid on one backdrop |
| Product mechanism | A phone-free, hands-only shot — folding, sorting, hanging — no UI mockups |
| Cost-per-wear / analytics | A sparse, almost-empty rail with a few well-worn pieces, warm light |
| Seasonal | Same recipe, seasonal fabrics and palette (wool/tweed autumn, linen/cotton summer) |

## People in images — read before prompting

- Generating **anonymous, synthetic adult models** wearing outfits is fine, and Google's own documented example prompt is a fashion model. Prefer flat-lays and crops regardless — they age better, avoid uncanny faces, and keep focus on the clothes.
- **Never** prompt for a named person, a celebrity, or a lookalike of a real public figure. Google blocks generating prominent people outright.
- **Never** upload photos of real people for image-to-image without their consent.
- **Never** generate anything depicting minors.
- If a face must appear, prefer a crop that excludes it — shoulders-down, hands, or a back view.

## Watermark

Outputs carry an **invisible SynthID** watermark always; that's fine and should not be tampered with. A **visible** watermark is controlled by the "Visible watermarking" toggle in the menu under the profile picture (top right). Check it is **off** before a batch, or every marketing image ships with a visible mark.

## Downloading

In Edit View, click the **download (⤓)** icon top right. From the grid, hover the asset → **⋮** → Download. `Ctrl + D` also works.

Downloading is a file download — **ask the user before the first download in a session**, then proceed for the rest of that run.

**Verified 2026-09-10.** The ⤓ icon does not download on its own; it opens a resolution menu:

- **1K — Original size.** The generated image, unmodified. ~700 KB. **This is the one to take** for both Pages.
- **2K — Upscaled.** Only for print or a large hero.
- **4K — Upscaled.** Greyed out behind an **Upgrade** button.

Output is **JPEG**, named `<Flow asset title>_<yyyymmddhhmmss>.jpeg` — Flow titles the asset from the prompt, so a "Autumn capsule wardrobe flat-lay" prompt yields `Autumn_capsule_wardrobe_flat-lay_20260910184250.jpeg`. Never assume the name; list newest-first and take the top entry.

### Getting the file to the composer

The browser's `file_upload` accepts only paths this session may read. A path on the user's own machine is **rejected** — `/Users/fh/Downloads/x.jpeg` fails with *"only files this session is allowed to read can be uploaded"*, even right after granting that folder. The file has to be staged into the session first:

1. `device_request_folder_access` on `~/Downloads` — once per session, granted immediately.
2. `ls -lt "$HOME/mnt/Downloads" | head -5` in the device shell to find it. **Do not** use `device_list_dir` on that folder — this user's Downloads is large enough that the listing overruns the token budget in a single call.
3. `device_stage_files` on the full Mac path → returns a `stagedPath` under `/mnt/user-data/uploads/Downloads/...`.
4. Upload **that** path.

### Provenance

Flow embeds C2PA / SynthID provenance metadata. LinkedIn reads it and stamps the image *"Content credentials label added."* Leave it in place — it is accurate, and Clad9's methodology angle rests on exactly this kind of honesty about how things are made.

## Consistency across a campaign

To reuse the same look across many posts: generate the base image once, then reference it with `@` in later prompts (the `@` key opens the asset picker in the prompt box), or drop it into **Characters** for a recurring model. Nano Banana accepts multiple reference images per prompt.
