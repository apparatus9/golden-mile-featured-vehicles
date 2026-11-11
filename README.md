# Featured Vehicles — Golden Mile Chrysler

A featured-vehicles page for **Golden Mile Chrysler** (1743 Eglinton Ave E, Toronto). Eight units for
the month, each priced as a weekly finance payment and linked to its real listing.

**`index.html`** is the current design. It is a single self-contained file — no build step, one web
font — so it can be opened directly, dropped on a static host, or pasted into a WordPress Custom HTML
block.

The page has **no header or navigation of its own**: it is built to sit inside the dealership site,
which supplies the chrome. It still carries the black contact bar at the top and a footer; remove
those too if the host page duplicates them.

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | The page. All CSS inline. |
| `images/` | The eight vehicle photographs. |
| `index-orange.html` | The previous design, before the site colours were matched. |
| `index-plain.html` | A plainer dealer-style layout. |
| `index-catalogue.html` | An editorial "specimen catalogue" treatment. |
| `index-classic.html` | The first version, closest to the original cdd6.ca layout. |
| `assets/` | Archival Golden Mile photographs, plus a composed strip used only by `index-catalogue.html`. |
| `assets/credits.json` | Source, author and licence for every found image. |

## Matching the dealership site

Colours were sampled from a screenshot of goldenmilechrysler.ca rather than chosen:

| Token | Value | Taken from |
| --- | --- | --- |
| `--red` | `#CA0000` | the "View Featured Special" button |
| `--black` | `#000000` | the brand tile band |
| `--band` | `#EBEBEB` | the card info strip |
| `--photo` | `#C7C7C7` | the studio photo background |

The card anatomy copies the site's Featured Specials cards: a small make line, a large condensed
uppercase trim line, a grey info strip split left and right, then a full-width red button. The
site's strip reads *57 / Kilometers* and *$74,038 / PRICE*; this one reads *826022 / STOCK* and
*$100.88 / WEEKLY*, with the finance breakdown beneath it. The black panel with red-outlined tiles
follows the site's SHOP RAM / SHOP JEEP tiles.

Display type is **Oswald**, which approximates the site's condensed face but has not been confirmed
as the same font.

## The vehicles

Every card links to that unit's listing and carries Call and Email buttons; the email subject is
prefilled with the vehicle, its Rx number and its stock number so a lead is never ambiguous.

| Rx | Vehicle | Stock | Colour | Weekly |
| --- | --- | --- | --- | --- |
| 001 | 2026 Jeep Compass Sport 4×4 (Demo) | 826022 | Bright White | $100.88 |
| 002 | 2026 Chrysler Grand Caravan SXT (Demo) | 826156 | Red Hot | $148.88 |
| 003 | 2026 Jeep Gladiator Willys 4×4 | 826155 | Black | $171.88 |
| 004 | 2026 Jeep Wrangler Sport S 4-Door 4×4 | 826103 | Granite Crystal | $180.88 |
| 005 | 2026 RAM 1500 Black Express 4×4 Crew Cab | 826321 | Bright White | $190.88 |
| 006 | 2026 Dodge Durango GT Plus AWD | 826303 | White Knuckle | $204.88 |
| 007 | 2027 Chrysler Pacifica Pinnacle AWD (Demo) | 827009 | Bright White | $209.88 |
| 008 | 2026 Dodge Charger Scat Pack Plus 2-Door AWD | 826171 | Bludicrous Blue | $226.88 |

All on the same terms: $0 down, 96 months, 5.99%, plus HST and licensing.

## Before this goes live

1. **`sales@goldenmilechrysler.ca` is a guess.** No sales address is published on the dealership
   site. It appears in all eight `mailto:` links.
2. **The disclaimer is a draft, not compliance-approved.** Ontario weekly-payment advertising carries
   specific OMVIC all-in pricing and cost-of-borrowing disclosure requirements. Replace the footer
   text with the dealership's approved wording.
3. **The photographs are crops from a screenshot**, roughly 590px wide, levelled to the site's
   `#C7C7C7` studio grey so they sit flush in their tiles. Fine on screen, soft for production —
   replace with the originals from each listing. The RAM 1500 shot also has a gold warranty banner
   burned into it, which breaks the set and pulls focus in the grid.
4. **Check the Charger's colour.** Stock 826171 is advertised here as Bludicrous Blue and the photo
   is blue, but the dealership's own listing data gives the exterior as "After Dark". The VIN
   (2C3CDAMP3TR216230) matches the stock number, so the colour field is the thing to verify.
5. **Confirm the display typeface.** Oswald stands in for the site's condensed face; swap `--display`
   if the real one differs.

## Not included

The **SHOP RAM / SHOP JEEP / SHOP DODGE / SHOP CHRYSLER** strip from the dealership homepage was left
out: it needs four inventory URLs that could not be verified, and the site returns HTTP 403 to
automated requests. Supply the four links and the strip can be added — the tile styling is already in
the stylesheet.

## Image credits

Vehicle photographs are the dealership's own.

The two photographs of the Golden Mile are Creative Commons and are credited in the page captions:

- "Golden Mile Plaza, north-east corner of Eglinton Avenue East and Victoria Park Avenue" by
  Toronto History, [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/), via
  [Flickr](https://www.flickr.com/photos/48096488@N03/49615500967)
- "Golden Mile Scarborough 2023" by Canmenwalker,
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0), via
  [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Golden_Mile_Scarborough_2023.jpg)

Attribution is a condition of both licences — keep the credit lines if these pages are reused.
