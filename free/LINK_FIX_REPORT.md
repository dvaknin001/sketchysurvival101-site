# Website Link Fix Report — 2026-09-01

Source of truth: `research/WEBSITE_AUDIT_0901.md`. Changes STAGED only (touch site root beyond `free/`, Dean gates the push). No commit, no push.

## 1. Cheat sheet HTML deep links (8 files, 10 watch references)

Each sheet's channel watch reference replaced with its correct `youtu.be/<id>` link. Old link everywhere was `youtube.com/@SketchySurvival101` (plain text or channel anchor).

| File | Line(s) | Old link | New link |
|---|---|---|---|
| blackout-power-kit-checklist.html | 153 | youtube.com/@SketchySurvival101 | https://youtu.be/ee5AWmz7N-s |
| flash-flood-survival-checklist.html | 161 | youtube.com/@SketchySurvival101 | https://youtu.be/RURG0-I1uz4 |
| first-48-hours-after-a-nuke-checklist.html | 284, 292 | youtube.com/@SketchySurvival101 | https://youtu.be/OeIXnRx5lkc |
| endless-clean-water-checklist.html | 146 | youtube.com/@SketchySurvival101 | https://youtu.be/7w1LaswQTAQ |
| sand-vault-checklist.html | 253 | youtube.com/@SketchySurvival101 | https://youtu.be/eyr5FQ88wpY |
| rainwater-harvest-checklist.html | 238 | youtube.com/@SketchySurvival101 | https://youtu.be/i_38OUbgd4E |
| persian-desert-ice-checklist.html | 265, 273 | youtube.com/@SketchySurvival101 | https://youtu.be/g1iBfpKjVZ0 |
| warm-room-survival-checklist.html | 142 | https://www.youtube.com/@SketchySurvival101 (CTA button) | https://youtu.be/fNrX4PlE8V4 |

Plain-text references were converted to clickable anchors pointing at the video, visible text = `youtu.be/<id>`. Existing markup/classes preserved (`<b>`, `<span class="u">`, `.btn`).

Note: `warm-room-survival-checklist.html` line 86 nav "YouTube ▶" button left as the channel link (site navigation, not a per video watch link).

## 2. /free hub cards (`free/index.html`, 8 cards)

Every card's watch CTA repointed from `https://www.youtube.com/@SketchySurvival101/videos` to its video.

| Card | Old | New |
|---|---|---|
| Blackout Power Kit | @SketchySurvival101/videos | https://youtu.be/ee5AWmz7N-s |
| Flash Flood Survival | @SketchySurvival101/videos | https://youtu.be/RURG0-I1uz4 |
| First 48 Hours After a Nuke | @SketchySurvival101/videos | https://youtu.be/OeIXnRx5lkc |
| Endless Clean Water | @SketchySurvival101/videos | https://youtu.be/7w1LaswQTAQ |
| The Sand Vault | @SketchySurvival101/videos | https://youtu.be/eyr5FQ88wpY |
| Free Water From Your Roof | @SketchySurvival101/videos | https://youtu.be/i_38OUbgd4E |
| Persian Desert Ice | @SketchySurvival101/videos | https://youtu.be/g1iBfpKjVZ0 |
| Warm Room Survival | (had no video link, only "Read the full guide") | ADDED "Watch the build →" https://youtu.be/fNrX4PlE8V4 (guide link kept) |

Hub page header links (line 65 Subscribe, line 77 "Watch the builds →") left as channel links — they are page nav, not per card CTAs.

## 3. Homepage "New this week" strip (`index.html` lines 105-122)

Replaced the 3 stale hardcoded cards with the 3 newest public uploads. Updated each `href`, `img src` (maxres + hq fallback), `aria-label`, `alt`, and `<h3>`. No hyphens/dashes in any visible title.

Before:
- Y5WngG2V4tU — The Physics of Heat Waves: Why Most People Pass Out (Science Explained)
- Xh-i8-0_BSs — MIT Confirmed This $12 Pipe Cools Homes for Free (Science Explained)
- atHu3rMwq2Y — Turn Any Fan Into an AC With 3 Frozen Bottles. The Math They Skip

After:
- ee5AWmz7N-s — The $400 Box That Beats a $12,000 Generator When the Grid Dies — https://youtu.be/ee5AWmz7N-s
- RURG0-I1uz4 — The Physics of Flash Floods — https://youtu.be/RURG0-I1uz4
- OeIXnRx5lkc — 48 Hours After a Nuke — https://youtu.be/OeIXnRx5lkc

## 4. Orphan duplicate removed

Deleted `free/warm-room-checklist.html` (real sheet is `warm-room-survival-checklist.html`).
Confirmed before deleting: no HTML links to the orphan `.html`. The only `warm-room-checklist` references are to the `.pdf` (hub card line 194 + the real sheet's download buttons), which stays untouched. Hub card already pointed at the real sheet, so no repoint needed.

## Counts
- Sheet HTML files relinked: 8 (10 references)
- Hub cards relinked: 8 (7 repointed + 1 Warm Room gained a watch link)
- New this week strip updated: yes
- Orphan removed: yes (warm-room-checklist.html)
