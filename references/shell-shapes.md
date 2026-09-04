# The 4 shapes (the MEP: step 2, and the plan's lists)

One shape per business model. The model comes off `squad/business.md` (THE MODEL, or THE
DRAFT's model line); the shape is read off it, never asked. A hybrid model line takes its
first word.

| THE MODEL says | and THE STACK (or the draft's deliverable) is | The shape | The file |
|---|---|---|---|
| agency | a site, a page, a funnel, anything a browser opens, or anything else | the page | `index.html` (the plugin's `client.md` beside it) |
| agency | posts, scripts, emails, newsletters, video | the piece | `piece.md` |
| consulting | anything | the structure | `structure.csv` plus `notion.md` |
| software | anything | the prototype | `prototype/index.html` |

## Not in any shell (the list `plan.md` prints, and what keeps 2 days 2 days)

Their domain, a URL, a deploy, a backend, a login, payments, a form wired to anything, an
image file, a second page or a second flow, a new account, a key or a paid seat, and
anything about the buyer that `notes.md` does not carry. The shell opens on the founder's
laptop and goes on a screen share. Nothing goes on the buyer's domain, in their name or on
their accounts until the money clears.

## The page

One page in the buyer's name, built by the `execution-design` plugin, opened as a local
`index.html`.

**It shows**

1. Their business, by name, in their town, with their reviews and rating where
   `notes.md` (or the founder, off Maps at the yes) holds the count.
2. The result their customer buys, in the customer's words from `notes.md`, as the hero.
3. The one money action (book, call, quote), its button disabled with the plugin's line
   under it, the phone number carrying the action when `notes.md` holds one.

**Not in it**, past the shared list: more than one page, a CMS, a login, images you had
to wait for, a wired form.

Day one is the plugin installed (once per laptop), the 7 answers, the direction, the
build. Day two is the 9 boxes, the look, the fixes, one rehearsal of the screen share.

**The plugin run, exactly.** Project root: `squad/mep/<first-last>/`.

- Phase 1, the brief. Fill `client.md` from the offer document and `notes.md`:
  `shape: local-service` for a business, `content-brand` for a person with an audience;
  `email: NONE` and `booking_url: NONE` (nothing is wired); `website_old: NONE`; the money
  action off what the buyer's customers do; the prices in the services table off
  `notes.md` or `quote only`; every unknown fact `UNKNOWN`, never a guess and never a
  question. Print the plugin's 7 questions with the pre-filled answers for one yes. Say in
  that message: copy the review count and rating off Maps into question 4; `UNKNOWN` stays
  `UNKNOWN` and the page carries nothing there. Question 6 (three sites they like, one they
  hate) is answered from the plugin's own data; nothing outside this folder is read.
- Phase 2, the plugin's 3 directions with real palettes and pairings. The founder picks
  one. Never build before the pick.
- Phase 3, the build. One `index.html`, styles inline, the pairing's Google Fonts import
  line, no framework, no build step. Every image slot in the markup at its ratio with its
  alt text and a placeholder painted by CSS. The form's `action` empty, its button
  `disabled`, the plugin's line under it, the phone number as the working action when
  there is one. No `images.md`, no `images/`.
- Phase 5, the polish. Grade the 9 boxes in writing, box 5 as a count (`<n> slots, 0
  filled`), boxes 8 and 9 open, plus any box the page actually fails (box 2 when the font
  fell back on a non-Latin market); run the plugin's AI-made pass and its specificity pass
  (could a competitor down the street say this line word for word?).
- Skipped, said once: phase 4 (image files, the fal.ai key), phase 6 (Lighthouse,
  analytics, redirects, the deploy) and phase 7. Those are W2's, after the yes.

## The structure

A Notion database that shows the shape of the engagement, delivered as a CSV the buyer's
own facts fill, imported into the founder's own free Notion.

**It shows**

1. The columns: what the engagement would track, named in the buyer's words.
2. The rows: their facts from `notes.md`, 5 at most, none invented; fewer facts means
   fewer rows, and the plan says the count.
3. One view, and the one line above it.

**Not in it**, past the shared list: a written diagnosis, the analysis, the full
workspace, automations, a row you made up. The diagnosis is what the pilot sells.

Day one is the columns, the rows, the CSV, the import. Day two is the view, the line, the
look.

**The files.** `structure.csv`: the header row is the columns, then the rows, plain CSV.
`notion.md`: 3 short parts. The one line that sits above the database, in the buyer's
words. The one view (a table or a board, and what it is sorted or grouped by). The import
path: Settings, Import, CSV, or type `/csv` on a page, then map each column to a property.
No Notion connector, no one-page diagnosis.

## The piece

One piece made for this buyer, in their voice, for the channel they already use, written
next to their current one so the gap shows without a word from the founder.

**It shows**

1. Their current piece, as posted.
2. The piece: the same channel, their voice, on the slice.
3. The gap between the two, visible on its own.

**Not in it**, past the shared list: a calendar, a strategy deck, 10 pieces, a retainer
proposal, an image.

Day one is the paste, the piece. Day two is the read-aloud in their voice, the look.

**The file.** `piece.md`, 2 headings: `## THEIRS, as posted` (the paste, untouched, the
channel and the date named) and `## THE PIECE`. The shape follows the channel: one
LinkedIn post, one script, one whole newsletter. Text only.

## The prototype

A clickable mockup as plain HTML: the flow the buyer would run on day one, with their data
in the fake fields, opened locally.

**It shows**

1. Screen one: where they land on day one, their nouns already in it.
2. Screen two: the work, one task done the way the offer says it gets done.
3. Screen three: the money button, disabled, one line under it saying nothing is wired.

**Not in it**, past the shared list: a backend, auth, payments, a database, a second
flow, "roadmap" screens.

Day one is screens one and two. Day two is screen three, the flow end to end, the look.

**The file.** `prototype/index.html`, one file, styles inline: 3 screens as sections
shown by hash links (`#one`, `#two`, `#three`), the buttons move between them, fake data
carrying the buyer's real nouns from `notes.md` (their product names, their customers,
their town), one flow that ends on the money button.

## No named buyer yet

The market-path founder has `squad/clients/self/` at most. Build for the buyer type in the
offer document's WHO line into `squad/mep/<buyer-type>/`, the same shape, with every
buyer-specific noun a marked blank in square brackets: `[their town]`, `[their review
count]`, `[the shop's name]`. The slice is the WHO line's problem in the offer document's
words, labeled `(offer document · <date>)`. The plan's last line before `go` says: rebuild
under a name the day the first call books. Then `/mep <name>` builds the named one; the
buyer-type folder stays as it is.

## A non-Latin market

The plugin's 16 pairings are Latin Google Fonts. A page for a buyer whose market writes in
Korean, Japanese, Thai, Arabic or another non-Latin script falls back to the system font
there, which the plugin's box 2 marks open. Build anyway. `plan.md` carries one LANGUAGE
line naming the gap, and the look at step 3 says which box it opens.
