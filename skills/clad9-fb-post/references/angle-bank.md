# Angle bank

Clad9's site is 708 URLs across five programmatic factories plus a 12-post blog. Every social post should trace back to a real page — that keeps claims grounded and gives each post a natural link.

## The content map

| Source | URLs | Pattern |
|---|---|---|
| Colors × occasion | 241 | `/colors/{color}` → `/colors/{color}/{occasion}` |
| Garment × occasion | 250 | `/style/{garment}` → `/style/{garment}/{occasion}` |
| Occasion × audience | 61 | `/what-to-wear/{occasion}/{audience}` |
| Season × audience capsules | 53 | `/capsule/{season}/{audience}` |
| Body shape × garment | 36 | `/body-type/{shape}/{garment}` |
| FAQ | 37 | `/faq/{question-slug}` |
| Blog | 12 + index | `/blog/{slug}` |
| Features | 9 | `/features/{feature}` |
| Alternatives | 5 | `/alternatives/{competitor}` |

The four occasions are fixed everywhere: `casual-weekend`, `first-date`, `job-interview`, `wedding-guest`.
The twelve audiences: big-tall-men, curvy-women, men, men-over-40, non-binary, petite-women, plus-size-women, tall-men, tall-women, teens, women, women-over-50.
The five body shapes: pear, apple, hourglass, rectangle, inverted-triangle.

**Exploitable gap:** roughly 36 of ~48 colour pages and ~37 of ~49 garment pages exist but are not linked from their own hub grids. Social posts pointing at those orphans are the cheapest internal-linking win available.

## The nine angles

Rotate through these. Never run the same angle twice in a row on the same platform.

### 1. The visibility problem
The category's core insight and Clad9's own framing: you don't own too few clothes, you can't see the ones you have. Pairs with the "20% of your wardrobe 80% of the time" stat.
Source: homepage, `/blog/the-real-reason-you-feel-like-you-have-nothing-to-wear`

### 2. Correct a piece of standard styling advice
The highest-performing shape in this voice. Take a rule everyone repeats — "own 30 pieces", "dress for your body shape", "neutrals go with everything" — name why it fails, give the mechanism.
Source: `/capsule`, `/body-type`, blog

### 3. A specific colour pairing, explained
Pick one colour × one occasion and explain the actual reason it works. Concrete, useful, screenshot-able.
Source: any `/colors/{color}/{occasion}` — prefer the ~36 orphan colours

### 4. A specific garment, styled four ways
One garment across the four occasions. Shows range from a single item — reinforces "from what you already own".
Source: any `/style/{garment}` set

### 5. Occasion dressing for a specific audience
Narrow and high-intent: what a petite woman wears to a job interview, what a tall man wears to a wedding. Specificity is the point.
Source: `/what-to-wear/{occasion}/{audience}`

### 6. Seasonal capsule
Sharply seasonal — capsule content peaks Aug–Sep and Dec–Jan. An 8-piece list for the current season and a named audience.
Source: `/capsule/{season}/{audience}`

### 7. How the product actually works
One feature, one mechanism, no adjectives. Batch capture, calendar-aware dressing, colour analysis from one photo, cost-per-wear. Explain the mechanism rather than praising it.
Source: `/features/{feature}`

### 8. The methodology / anti-slop post
Curated relationships first, AI writes the explanation second, embedding-similarity check kills filler. This is the most defensible thing Clad9 says and the market is primed for it.
Source: `/methodology`

### 9. Cost-per-wear and wearing what you own
The money-and-waste angle, delivered without guilt. Answers the real question "can a wardrobe app save me money?"
Source: homepage analytics section, `/blog/is-sustainable-fashion-really-about-buying-less`

## Seasonal calendar

| Window | Lead with |
|---|---|
| Aug–Sep | Autumn capsule, transitional-weather layering, "shed strategy" |
| Oct–Nov | Occasion dressing — weddings, parties, interviews |
| Dec–Jan | New-year declutter, cost-per-wear, clothing inventory, winter capsule |
| Feb–Apr | Colour analysis, "shop your closet", spring refresh |
| May–Jul | Travel capsules, packing lists, hot-weather occasion dressing |

## Keyword targets

Work these in naturally — never as a list. Head terms: *AI wardrobe app, digital closet, outfit planner, AI stylist, virtual closet, closet organizer, virtual try-on*. Long-tail and higher-intent: *app that tells you what to wear, outfit ideas from clothes I own, what to wear today, capsule wardrobe app, AI outfit generator, personal color analysis, cost per wear, travel packing list*.

The single most differentiating phrase, and the one to keep returning to: **"from the clothes you already own."**

## Avoiding repeats

Before writing, read the last 10 posts on the target Page. Reject the angle if it matches any of them, and reject any opening line that reuses the same construction as the most recent post. Rotation matters more than usual here — this plugin is designed to be run on a schedule.
