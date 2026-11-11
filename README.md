# The November File — Golden Mile Chrysler

A featured-vehicles page for **Golden Mile Chrysler** (Car Doctor Deals, 1743 Eglinton Ave E,
Toronto). Eight units for the month, filed by Rx number and priced as a weekly payment.

**`index.html`** is the current design. It is a single self-contained file — no build step, no
dependencies — so it can be opened directly, dropped on a static host, or pasted into a WordPress
Custom HTML block.

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | The page. All CSS and JS inline. |
| `index-classic.html` | The earlier version, kept for comparison. |
| `images/` | The eight vehicle photographs. |
| `assets/` | Archival photographs of the Golden Mile, plus the composed marquee strip. |
| `assets/credits.json` | Source, author and licence for every found image. |

## The idea

The dealership's own Rx numbering is the organising device: the eight vehicles are presented as
specimens on a dispensary chart, each with its Rx number and its dose — the weekly payment.

The page's one interactive element is a **weekly-budget dial** on the first screen. Dragging it dims
both the hero mosaic and the catalogue to the vehicles that fit the number, with a live count. It
works with a thumb on a phone and degrades to showing all eight if JavaScript does not run.

## The vehicles

| Rx | Vehicle | Weekly |
| --- | --- | --- |
| 001 | 2026 Jeep Compass Sport 4×4 Demo | $100.88 |
| 002 | 2026 Chrysler Grand Caravan SXT Demo | $148.88 |
| 003 | 2026 Jeep Gladiator Willys 4×4 | $171.88 |
| 004 | 2026 Jeep Wrangler Sport S 4-Door 4×4 | $180.88 |
| 005 | 2026 RAM 1500 Black Express 4×4 Crew Cab | $190.88 |
| 006 | 2026 Dodge Durango GT Plus AWD | $204.88 |
| 007 | 2027 Chrysler Pacifica Pinnacle AWD Demo | $209.88 |
| 008 | 2026 Dodge Charger Scat Pack Plus 2-Door AWD | $226.88 |

All on the same terms: $0 down, 96 months, 5.99%, plus HST and licensing.

## Before this goes live

These four items are **not** resolved and need a human:

1. **The eight vehicle links are unverified.** `goldenmilechrysler.ca` returns HTTP 403 to automated
   requests, so the exact listing URLs could not be confirmed. Each card carries a working
   model-level inventory URL as a stand-in, marked in the source with a comment:
   `<!-- VDP LINK — Rx #00n -->`. Replace all eight with the real listing URLs.
   The Charger link (Rx #008) points at a listing described elsewhere as a **grey** car at $74,038,
   while the photo shows a blue one — check whether that is even the same unit.
2. **`sales@goldenmilechrysler.ca` is a guess.** No sales address is published on the dealership
   site. It appears in all nine `mailto:` links.
3. **The disclaimer is a draft, not compliance-approved.** Ontario weekly-payment advertising carries
   specific OMVIC all-in pricing and cost-of-borrowing disclosure requirements. Replace the footer
   text with the dealership's approved wording.
4. **The photographs are crops from a screenshot**, roughly 590px wide, levelled to a common
   background. Fine on screen, soft for production — replace with the originals. The RAM 1500 shot
   also has a gold warranty banner burned into it, which breaks the set.

## Image credits

Vehicle photographs are the dealership's own.

The two photographs of the Golden Mile are used under Creative Commons and are credited in the page
footer:

- "Golden Mile Plaza, north-east corner of Eglinton Avenue East and Victoria Park Avenue" by
  Toronto History, [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/), via
  [Flickr](https://www.flickr.com/photos/48096488@N03/49615500967)
- "Golden Mile Scarborough 2023" by Canmenwalker,
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0), via
  [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Golden_Mile_Scarborough_2023.jpg)

Keep both credit lines in the footer if the page is reused — attribution is a condition of the
licence.

## Design notes

Built against an art-direction brief: the *specimen catalogue* direction (seed 1704183691), type set
in Bricolage Grotesque, and the dealership's own orange, black and white. The page is checked at
1440 / 768 / 390px with an automated inspector; it reports no failures.

Two warnings are knowingly left open:

- **No video.** No honest clip of Eglinton Avenue East exists in the open collections, and footage of
  a different Toronto street presented as "our place" would be misleading. The page's moving picture
  is the drifting photo strip instead.
- **One reported blank gap.** A separate full-page sweep found no empty band over 120px anywhere on
  the page; the warning appears to be counting the composed marquee — a background image rather than
  `<img>` elements — as empty.
