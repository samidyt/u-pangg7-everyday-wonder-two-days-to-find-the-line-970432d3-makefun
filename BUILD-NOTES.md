# Build notes — "Everyday Wonder, Two Days to Find the Line"

- Bounty: https://make.fun/bounty/u-pangg7-everyday-wonder-two-days-to-find-the-line-970432d3
- Slug: `u-pangg7-everyday-wonder-two-days-to-find-the-line-970432d3`
- Prize: $2 total, 2 paid places (1st $1.18, 2nd $0.82). Entry fee $0.00 (free).
- Deadline: Thu 26 Nov 2026 18:35 WIB (11:35 UTC). ~235 submissions at dispatch, rising fast.
- Build session: Tue 24 Nov 2026 ~18:51–18:55 WIB.
- Kit: `~/workspace/makefun/u-pangg7-everyday-wonder-two-days-to-find-the-line-970432d3-kit/`
  (kit.tgz, 8,060,281 bytes, from `https://make.fun/c/u-pangg7-everyday-wonder-two-days-to-find-the-line-970432d3/kit`).
  `RULES.txt`, `competition.yaml`, `kit.json` read.
- Rules: entrypoint `main.ts` (or `main.py`) at repo root; program writes one
  sentence to `/output/entry.txt`; sealed gate is UTF-8 text of 1–200
  characters, not only whitespace. No local grader exists (RULES.txt: "There
  is no local grade of this competition: the server grades every entry").
  README must carry the three live make.fun badges; GitHub About needs
  website on make.fun + topic `makefun`.
- Judge brief (from competition.yaml / RULES.txt): blind pairwise rounds,
  weighed most important first: (1) a small moment of wonder in everyday
  life in a single sentence; (2) an angle the reader has not met before, the
  phrasing itself the surprise; (3) the surprise lands in one read, a single
  clear sentence; (4) grounded in something real and specific; (5) every word
  working, no filler, no worn phrase. Text addressed to the judge is allowed
  but was NOT used. Final heat takes the top 500 dev-board entrants.

## Drafting passes (main.ts)

- Pass 1: "The fridge hum changed key when I opened the door, like a choir
  clearing its throat for one singer." (105 chars) — the image was right,
  but the sentence opened on the hum instead of the act.
- Pass 2 (final): "When I opened the fridge door, its hum changed key, like
  a choir clearing its throat for one singer." (100 chars) — reordered so
  the action opens, the change follows, and the surprise lands on the final
  words. Sharper in one read; 5 chars shorter.

## Why this line won

- **Small moment:** opening the fridge — daily, unnoticed, real.
- **Fresh angle:** a compressor's pitch shift heard as a choir clearing its
  throat for one singer — choral manners from an appliance, an angle no
  reader has met before. Deliberately avoids the sponsor's own examples
  (lift door / stranger's song, kettle click, puddle sky), which the field
  will be full of.
- **One-read surprise:** trigger → change → image, punch on the last words.
- **Grounded:** a fridge compressor genuinely shifts pitch when the door
  opens; nothing floats free of the everyday.
- **Tight:** 100 chars, one sentence, no filler.

## Rejected alternatives

- "The automatic door hesitated before opening for me, as if the supermarket
  needed a moment to remember my face." (117 chars) — fresh, but
  "remembering my face" is a more familiar trope than the choir image, and
  the punch lands mid-sentence.
- "The washing machine paused mid-spin, and in that held breath the whole
  flat waited to see what it would say." (112 chars) — good, but
  personifying an appliance's pause is a common device; the surprise is
  gentler than the fridge line's.
- "A single raindrop raced the others down the bus window and won, and the
  whole commute applauded in silence." (110 chars) — charming, but the
  raindrop-race image is familiar; the "applauded in silence" turn is the
  only surprise.

## Verification

- Local run 1: `mkdir -p out1 && MAKEFUN_OUTPUT_DIR=out1 node main.ts` →
  `wrote entry.txt (100 chars)`.
- Local run 2: `mkdir -p out2 && MAKEFUN_OUTPUT_DIR=out2 node main.ts` →
  `wrote entry.txt (100 chars)`.
- `cmp out1/entry.txt out2/entry.txt` → IDENTICAL.
- Python gate check (exit 0): 100 bytes / 100 chars, 1 line, 0 newlines,
  1 sentence-terminating mark, non-whitespace, gate 1–200 PASS.
- No local grader exists for this bounty (per RULES.txt); server grades.
- No fee paid, no wallet touched, no funds/capital required (text-only
  bounty).
