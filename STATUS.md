# STATUS.md — Free Block Party Starter Pack

Last updated: 2026-11-07

## What was built

A free, printable, no-tracking starter kit for hosting a neighborhood block party, published by Asdale Dynamics, LLC under the MIT License.

Contents:

- `index.html` — one-page HTML index linking to every printable, with usage instructions and a note distinguishing this pack from the Free Party Planner Pack (at-home celebrations) and the Free Meal Train Kit (supporting one household).
- `printables/style.css` — shared print/calming-paper styling (warm palette, print CSS, editable-blank styles).
- `printables/flyer.html` — one-page party flyer with fill-in date/time/location and a rainy-day spot reminder.
- `printables/potluck-signup.html` — potluck dish sign-up grid (mains, sides, dessert, drinks, special-diet items, paper goods) with ingredient-labeling kindness notes.
- `printables/cleanup-signup.html` — cleanup shift sign-up (during-party, wrap-up, after-party, next-morning) with low-energy-friendly notes.
- `printables/table-cards.html` — 8 potluck table cards for allergen/diet labeling (gluten, nuts, vegetarian, vegan, dairy-free, gluten-free, spicy, custom), 4 per printed page.
- `printables/name-tags.html` — 12 name tags per page with playful sub-lines ("ask me about the grill," "future mayor").
- `printables/kid-games.html` — one-page guide to 5 low-cost games (sock race, chalk gallery, cup stacking, sponge water relays, neighborhood bingo) plus a "game runner volunteer" line.
- `printables/rainy-day-plan.html` — Plan B details table (indoor spot, decision time, how neighbors hear) and per-condition plans (drizzle, steady rain, thunderstorm, extreme heat, wind).
- `printables/organizer-reminders.html` — kindly-worded permit/lead-time checklist and reminders about night-shift neighbors, homebound delivery, diet labeling, sensory-considerate calm zones, and safety basics (explicitly not legal or medical advice).
- `LICENSE` — MIT, with the exact line `Copyright (c) 2026 Asdale Dynamics, LLC`.
- `README.md` — credits Asdale Dynamics, LLC, lists the pack, explains printing and the freebie family.

Features: every printable has a Print button and contenteditable fill-in blanks (typed in the browser or filled by pen on dotted lines). No JavaScript beyond `window.print()`; no analytics, cookies, or external resources.

## How to run it

No build step — it's plain HTML/CSS.

- Double-click `index.html`, or
- `python3 -m http.server 8000` then open `http://localhost:8000`.

Print from any browser; regular 8.5×11 paper. Name tags and table cards work best on card stock or sticker paper.

## Verification results (all passing)

1. **Parse check**: all 9 HTML files parsed with Python's html.parser; every tag balanced, no unclosed elements, every file has `<!DOCTYPE html>` and `lang="en"` — none reported.
2. **Link check**: script-followed `href` resolution from every page to `style.css` and between index and printables — no broken links.
3. **HTTP check**: `python3 -m http.server` smoke test; all 10 files (index + 9 assets) returned HTTP 200.
4. **Secrets scan**: grep for api keys, tokens, passwords, email addresses, phone-number patterns across all HTML/MD/CSS — only an intentional README sentence mentioning that no secrets exist; no actual secrets or personal data.
5. **License check**: `Copyright (c) 2026 Asdale Dynamics, LLC` confirmed present verbatim in `LICENSE` line 3; credit present in `README.md` and page footers.
6. Edits during verification fixed two garbled sentences in the rainy-day table and a stray duplicate class on one name tag.

## Known gaps

- No PDF versions bundled (browsers' Print → Save as PDF covers it; no off-the-shelf PDF library was added to keep the pack zero-dependency).
- Name tags are 4-in-a-row rectangles optimized for card stock, not a specific Avery sticker template.
- The reminders page is general good practice, not city-specific legal guidance — organizer must still check local permit rules.
- kid-games bingo grid is a checklist rather than a cut-out bingo board; a future version could add a proper 5×5 board.
- No print-preview screenshots in the README.

## Git

Committed to the local repository only. Nothing pushed, no remotes, no publishing.
