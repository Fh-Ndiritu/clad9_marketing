---
name: clad9-image-run
description: Generate marketing images for Clad9 in the user's Google Flow project and download them ready to attach to a post. Use when the user says "generate an image", "make the image", "image run", "create visuals for the post", "flow image", or invokes /clad9-image-run. Also called automatically by the Clad9 posting skills when a post needs a visual.
---

# Generate a Clad9 marketing image in Google Flow

## Read first

> Paths here are relative to this skill's own folder — the base directory announced when the skill loads. If a path doesn't resolve, locate the plugin directory (the one containing `.claude-plugin/plugin.json`) and read `references/` from there. Never proceed on remembered facts if these files can't be read — say so and stop.

`../../references/flow-images.md` — the verified UI walkthrough, the house prompt recipe, aspect ratios by destination, and the rules on depicting people. Follow it exactly; it was written against the live interface.

## Steps

1. **Open the project.** `https://flow.google.com/project/7d6deb2c-f424-48f2-98d1-c52b13966f6a`. Confirm the header reads **Clad9** before generating anything — generating into the wrong project scatters assets across the user's account.

2. **Check the visible-watermark toggle is off** (profile picture menu, top right) if this is the first run of the session. Every image is otherwise stamped.

3. **Set up the generation.** Click the model chip → **Image** → aspect ratio for the destination → **Nano Banana Pro** → **x2**.

   | Destination | Ratio |
   |---|---|
   | Facebook post | 3:4 |
   | LinkedIn post | 1:1 |
   | Landscape | 16:9 |
   | Story/Reel | 9:16 |

4. **Write the prompt** using the house recipe. Name fabrics, not garments — "navy wool blazer", never "blazer". Keep to Clad9's palette: cream, camel, navy, burgundy, olive, charcoal, tan. Match the prompt shape to the post's angle using the table in the reference.

5. **Generate** and wait ~20 seconds. Costs 0 credits on this account, so generate a second variation rather than settling for a weak first result.

6. **Judge the output honestly.** Reject and re-prompt on: garbled text, warped or impossible garments, extra limbs, a visible watermark, or a palette that has drifted off-brand. Say plainly if an image is not good enough rather than shipping it — a bad image is worse than no image.

7. **Download.** In Edit View, the **⤓** icon top right.

   **Ask the user before the first download in a session** — downloading files needs their go-ahead. Once they agree, continue for the rest of that run without asking again.

8. **Report** where the file landed so the posting skill can attach it.

## Constraints

- Prefer flat-lays and crops over generated people. They age better, avoid uncanny faces, and keep attention on the clothes — which is the product.
- Never prompt for a named or recognisable real person. Never generate minors. Never upload photos of real people without their consent.
- If the user wants a consistent look across a campaign, generate one base image and reference it with `@` in later prompts, or save it into **Characters**.
