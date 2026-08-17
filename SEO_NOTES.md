# SEO build notes (2026-08-17)

Organic search build for sketchysurvival101.com. Strategy: crawlable HTML pages that
target the keyword and offer the PDF as the download, because Google barely ranks PDFs.
House rule respected: no hyphens or dashes in any visible copy I wrote (titles, meta,
new body). Pre-existing article bodies were left as they were (out of scope). URLs keep
their hyphens. Everything is staged, not committed.

## Per page on page SEO (title, meta description, canonical, Open Graph, Twitter card)

| Page | Target keyword | Notes |
|---|---|---|
| index.html | cheap home cooling heating power (physics) | New title/desc, OG+Twitter refreshed, Organization + WebSite (SearchAction) JSON-LD, H1 dash removed, "Free PDFs" nav link + warm room article card added |
| about.html | physics first home survival science / about | canonical + OG + Twitter added, dash-free title/desc |
| contact.html | contact sketchy survival 101 | canonical + OG + Twitter added |
| privacy.html | sketchy survival 101 privacy policy | canonical + OG + Twitter added |
| disclosure.html | affiliate disclosure sketchy survival 101 | canonical + OG + Twitter added |
| 404.html | (noindex) | canonical + OG + noindex added |
| free/index.html | free survival and prepper pdf cheat sheets, printable checklists | Rewritten as a keyword magnet: keyword H1, rich indexable copy, ItemList JSON-LD, price slash kept, "Read the full guide" link added |
| articles/attic-turbine-vent.html | attic turbine vent / whirlybird attic cooling | canonical + OG + Twitter + Article JSON-LD |
| articles/blackout-power-box.html | blackout power box / off grid battery | canonical + OG + Twitter + Article JSON-LD |
| articles/cool-home-without-ac.html | cool a house without ac | canonical + OG + Twitter + Article JSON-LD |
| articles/earth-tube-cooling.html | earth tube cooling / buried pipe ac | canonical + OG + Twitter + Article JSON-LD |
| articles/frozen-bottle-fan-ac.html | frozen bottle fan ac / diy ac fan | canonical + OG + Twitter + Article JSON-LD |
| articles/heat-wave-wet-bulb-survival.html | wet bulb temperature / heat wave survival | canonical + OG + Twitter + Article JSON-LD |
| free/warm-room-checklist.html | (legacy printable) | canonicalized to the new article + noindex so it does not compete; title made dash-free |

## New cornerstone article (article + PDF pattern, first build)

- Path: `free/warm-room-survival-checklist.html`
- Target keywords: grid down warm room, cheap emergency heat, survival heating pdf
- ~1,050 word crawlable HTML article, H2 sections, HowTo JSON-LD (supplies, tools, 5 steps)
- Download CTA to `/free/warm-room-checklist.pdf` (twice in the body)
- Content sourced only from the factchecked script DRAFT.md (no invented claims)
- Internal links in: home page article card + free/index card and closing paragraph
- Internal links out: home, free hub, blackout power box article, YouTube channel
- This is the reusable template: each future cheat sheet gets a full keyword article here,
  with the PDF as the download, an ItemList entry on free/index, and a card on home + free.

## Structured data (JSON-LD)

- index.html: Organization + WebSite with SearchAction (@graph)
- each articles/*.html: Article
- free/index.html: ItemList
- free/warm-room-survival-checklist.html: HowTo
- All blocks validated with json.loads (all valid).

## Sitemap + robots

- `sitemap.xml` created at repo root: 13 indexable URLs with lastmod 2026-08-17
  (home, free hub, new article, 6 articles, about, contact, disclosure, privacy).
  404 and the legacy printable are intentionally excluded (noindex / canonicalized).
- `robots.txt` still allows all crawling and now references the sitemap.

## Verification

- Live YouTube Data API script in index.html: untouched (key, v3 endpoints, __ssStats all present).
- Price slash CSS/markup ($2.99 struck to FREE) in free/index.html: untouched.
- All JSON-LD parses as valid JSON. sitemap.xml parses as valid XML.
- No em dash, en dash, or hyphenated word in any title, meta, or new body copy.
- All HTML parses without tag errors.
