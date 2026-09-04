---
name: mep
description: Use this when the offer document exists and the founder needs the deck to put on the screen in the sales hour. They say "/mep", "build my deck", "build the MEP", "build that" right after a call with a named person (it runs on that person's folder), "/mep [name]" (the name picks the folder), "build the deck for [company] off my cold list" (the cold path, for a company on squad/cold-list.md nobody has talked to yet), or "continue the MEP" (picking a stopped run back up). It reads squad/business.md and the buyer's own words, or on the cold path that company's row and what can be seen from outside, each line labeled an observation and never a quote, writes a one-screen plan (the buyer, the one slice of their problem in their words, the model, what the demo slides show, the 9 slides, what is not in it, day one and day two), stops for go, builds the demo by business model (a site built with the design plugin and captured onto the demo slides, or one piece beside theirs; the engagement's structure with their facts as rows; 3 drawn screens with the money button disabled), then writes one self-contained deck.html of 9 slides at 1920x1080 on the slide cage, its beat map, and deck.pdf when a headless browser is on the laptop. Nothing deploys, nothing gets a URL, nothing is invented about the buyer. The founder puts it on the screen and sends the PDF by hand.
---

# The MEP

The Minimum Executable Product is a deck: 9 slides for one buyer that explain the offer and
look like it already runs, built inside the 2 days the lesson scopes, on the screen in the
sales hour. Your work, in one line: **read the offer document and the buyer's own words, plan
the one slice, build the demo the model calls for, put it on 3 slides inside one deck, and
hand the deck to the founder to show.** The founder's part: go, one look, the screen share,
the PDF sent by their hand.

The deck is a sales object for one person. Finished on the surface, nothing behind it. The
test it has to pass is strict: if it could be shown to anybody in the trade, it is a template,
and the buyer treats it like one. So the deck names this buyer, in their facts, their town and
their words, or it is not done. Real production happens after the money.

When the founder can build the real thing inside the 2 days (a site, a page, a working
screen), they build it and the deck shows it on slides 5 to 7; the site path already works
this way, the page built for real and captured onto the demo slides. When they cannot, the
deck alone is the MEP: the structure, the piece, or the 3 drawn screens stand in for the
product, and the product gets built after the money.

The buyer is usually somebody the founder already talked to. On **the cold path** they are a
company off `squad/cold-list.md` who has said nothing to anybody here, so there are no words
to quote and the intake is the row plus what can be seen from outside. Beat 0 carries that
branch, and one rule rides on top of it: an observation is never dressed up as a quote.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance
file every member-run skill reads first (founder name, `accent color`, the `clients` path;
those 3 rows and no others), and its values win over the `squad/` paths written below, which
are worked examples. A row reading "(none yet)" is an unanswered field, not an override: the
worked-example path stands. This run writes no roots row; the deck carries the buyer's name
and the roots file is the founder's. The rail on these slides carries the buyer's name, never
the roots file's `brand (the rail)` row, which belongs to the founder's own decks.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE READ | AUTO: the install check (`references/deck-shapes.md`, `references/deck-cage.css`), `squad/business.md` (the model), the buyer folder, or on the cold path that company's row, or the buyer type. HUMAN INPUT, one question, only when `squad/clients/` holds more than one folder and no name was given, or a named company sits in neither place |
| 1 THE PLAN | AUTO, one screen at `squad/mep/<name>/plan.md`, then **STOP · GATE: go, or a different slice** |
| 2 THE DEMO | AUTO by model. The site carries the plugin's own turns, HUMAN INPUT 3 times: the install once per laptop, a yes on the 7 pre-filled answers, the pick of one direction from 3; then the 3 captures. The piece carries HUMAN INPUT once: the paste of the buyer's current piece. The structure and the screens carry none |
| 3 THE DECK | AUTO: `deck.html`, `deck.md`, and `deck.pdf` when a renderer is found |
| 4 THE LOOK | AUTO, one line, then **STOP · GATE: the founder names anything that would read the same for anyone else; nothing to name means done**. With no named buyer the same gate asks for a go instead, because the deck is a shape until a call books |

The beat numbers ARE the step numbers below. 2 gates, no more. The plugin's turns inside
beat 2 are the plugin's stops, not this skill's gates, and the run map counts them so the
founder is not surprised. Never pause an automated beat to ask a small question (an unknown
fact is `UNKNOWN`, never a question); never run through a gate because the answer seems
obvious.

**Resuming.** A closed usage window mid-build is not a scope error. The rule keys on the
OUTPUTS, never on a session's memory: check them in this order and continue at the first
one missing or incomplete.

| Missing or incomplete | Resume at |
|---|---|
| `squad/business.md` does not exist | stop: the Winning Offer writes it, warm (g4) or cold (g5) |
| the trigger carries no name ("continue the MEP") | resolve `<name>` from `squad/mep/` first: the one folder there whose files are incomplete, the newest when more than one. Only an empty `squad/mep/` falls through to beat 0 |
| no `squad/mep/<name>/plan.md` | beat 0 |
| `plan.md` exists and its last line carries no `go <date>` | beat 1, THE GATE ONLY: print the plan, never rewrite it |
| `plan.md` says go and the demo is missing or partial (the site: no `client.md`, or a `client.md` carrying no `answers yes` line, means the 7 answers; `client.md` with `answers yes` and `style: UNKNOWN` means the direction; no `index.html` means the build; fewer than 3 `shot-*.png` means the captures; the piece: `piece.md` with no `## THE PIECE`; the structure: no `structure.csv`; the screens: nothing to check, the deck is next) | beat 2, at the file it names |
| the demo is whole and `deck.html` or `deck.md` is missing | beat 3 |
| `deck.html` exists, `deck.pdf` does not, and a renderer is found | beat 3, the PDF only |
| the deck is whole and `deck.md`'s last line carries no `looked <date>` | beat 4 |
| `deck.md` carries `looked <date>` | nothing to resume: say the deck is done and where it is |

Never re-ask a yes the files already show, and never rebuild a file that opens.

## The outputs (one folder, every run)

All of it in `squad/mep/<name>/`. The folder name matches the buyer's folder under
`squad/clients/`; on the cold path it is the company's name off `squad/cold-list.md`; with no
named buyer at all it is the buyer type off the offer document's WHO line. All 3 lowercased
and hyphenated, and `<name>` below stands for whichever one this run resolved.

1. `plan.md`: one screen, the plan, with `go <date>` as its last line once the founder says go.
2. `deck.md`: the beat map, one row per slide: the slide, what the founder says (in bold, it
   is the line said out loud), what is on it. Its last line is `looked <date>` once the
   founder has nothing left to name at beat 4.
3. `deck.html`: the deck, one self-contained file, the cage CSS inline, one `<section>` per
   slide at 1920x1080, arrow keys and a click between slides, a print sheet at one slide per
   page.
4. `deck.pdf`: when a headless browser is found on the laptop. Otherwise the founder prints it
   from the browser and `deck.md` says so.
5. The demo files, by model: `index.html` with the plugin's `client.md` beside it and
   `shot-1.png`, `shot-2.png`, `shot-3.png` (the site); `piece.md` (the piece);
   `structure.csv` (the structure); nothing past the deck when the screens are drawn, and
   the same 3 captures when a real screen was built inside the 2 days.

A `cover.png` or `cover.jpg` in the same folder is the founder's, dropped in by hand: the
buyer's own photo, their logo, or a screenshot of their current site. This skill reads it for
slide 1 and never makes one.

No `send.md`, no `log.md`, no roots row, no `squad/demos/`, no `images.md`, no `images/`, no
`notion.md`, no `prototype/`, no second deck, no second flow. One throwaway wrapper page in
the system temp folder, deleted the moment shots 2 and 3 are taken, is the only file written
outside this folder. Nothing else gets written.

## Beat 0 · The read

**First, a self-check.** `references/deck-shapes.md` and `references/deck-cage.css`, inside
this skill's folder next to `SKILL.md`, must open. Either missing means stop and tell the
founder to finish the install: copy the whole skill folder, `references/` included.

**Then the offer document.** Open `squad/business.md`. Read THE SENTENCE, THE MODEL, WHO,
THE STACK and PRICE; a document whose last line carries no `confirmed <date>` stamp is
enough: read the same headings and build. No file at all: say so in one line, name the
Winning Offer (warm off a call in g4, cold off the market in g5), and stop. The model word,
with THE STACK when the model is agency, decides the demo by the table in
`references/deck-shapes.md`. The demo is never a question.

**Then the buyer.** The folder is the name in the trigger when one was given (`/mep
<name>`). On "build that", it is the client folder whose `notes.md` was written last, named
back in one line. On a resume with no name, it is the folder the resume table above
resolved. Otherwise the one folder under `squad/clients/`, `self/` and `references/` not
counted. More than one folder and no name: one question, in one message, the folders listed
one line each with their THE IDEA line. Read `notes.md`
whole (QUOTES, THE PROBLEM, THE COST, WHAT THEY PAY NOW, THE IDEA, THE MODEL, THE NEXT
STEP) and `transcript.md` for the buyer's nouns. A number appears on a slide only when
`notes.md` carries it. Read the language off the quotes: a non-Latin script is one
LANGUAGE line in the plan (the reference names the gap).

**The cold path**, when the founder says "build the deck for <company> off my cold list",
or the name they gave has no folder under `squad/clients/` and does have a row in
`squad/cold-list.md`. Nobody has talked to this company, so there is no folder, no
`notes.md`, no `transcript.md` and no quote. Read that row instead: the company, its town,
its trade, and the one broken-thing sentence the cut carries, plus what you can see from
outside. Every line of it is labeled an observation with the list's own `cut <date>`, and
every fact the row does not carry is `UNKNOWN`. The folder is `squad/mep/<company>/`.
`references/deck-shapes.md` says what each slide does when there are no words. A name in
neither place is one question, asked once: which company, and off which list.

**No named buyer yet** (the market-path founder, `self/` at most): build for the buyer
type in WHO into `squad/mep/<buyer-type>/`, every buyer-specific noun a marked blank in
square brackets, and rebuild under a name the day the first call books. The reference
carries the marking.

**Then the renderer**, so beat 2 and beat 3 know it: look for headless Chrome or Edge at
the paths the reference lists, and remember which one answered, or that none did. No
install is asked for.

**Then the cover.** Look for `cover.png` or `cover.jpg` in `squad/mep/<name>/`, dropped
there by the founder. Found, slide 1 carries it. Not found, the site path's `shot-1.png`
stands in once it is captured, and every other path keeps a text cover. Nothing is asked
for and nothing is made.

This beat prints nothing on its own; the plan is the first thing the founder sees.

## Beat 1 · The plan

Write `squad/mep/<name>/plan.md`, one screen, in this shape, and print it whole:

```
# MEP · <buyer name, or the buyer type>

THE BUYER   <name>, <what they do>, <their town>
THE SLICE   "<the one problem, in their words>" (<the label notes.md gives it>)
THE MODEL   <agency | consulting | software>

THE DEMO    <the site: 3 captures | the piece beside theirs | the structure, N rows | 3 screens>
1. <what slide 5 shows>
2. <what slide 6 shows>
3. <what slide 7 shows>

THE SLIDES
1. <their name, their town>, behind them <cover.png | cover.jpg | shot-1.png | nothing>
2. <the quote>
3. <the cost, or: dropped, no cost on the call>
4. <the slice, as the offer fixes it>
5. <demo>
6. <demo>
7. <demo>
8. <the first 14 days>
9. This week or next.

NOT IN IT
<the shared list from the reference plus the demo's own, one line>

DAY ONE
- <task>
- <task>

DAY TWO
- <task>
- <task>

LANGUAGE   <only when the buyer's market writes in a non-Latin script>
```

The slice is one quote, the strongest problem line in `notes.md`, verbatim, with the label
`notes.md` gives it (a warm call, or the founder's recollection); the deck is built on that
one problem and nothing wider. The demo's 3 lines, the not-in-it list and the 2 day lists
come from the demo's section in the reference, with the buyer's nouns filled in. Slide 1's
line names what stands behind the cover: the file the founder dropped in, `shot-1.png` on
the site path when none was, or nothing. No price line, no XYZ line, no call question, no
point system, no clock.

**On the cold path the slice is not a quote and never wears quote marks.** The line reads
`THE SLICE   <the row's broken-thing sentence> (observation · cold list <cut date>)`, and
the buyer line is the row's own company, trade and town. A stranger has said nothing to
this founder, so the label says where the sentence came from and the shape of the line says
what it is.

**STOP · GATE.** One line under the plan: "Go, or a different slice: name it, or point at
another quote, and I rewrite this." On the cold path the second half reads: point at
another thing you can see from outside. A different slice rewrites the plan and prints it
again. On go, append `go <date>` as the plan's last line, then build.

## Beat 2 · The demo

Read the demo's section in `references/deck-shapes.md` and follow it exactly. In short:

**The site** (agency). Check the `execution-design` plugin first: its `design` skill and
the `/execution-design:design` command answer. Missing, print these 2 lines, once per
laptop, and stop until it is in (a reload request means `/reload-plugins`):

```
/plugin marketplace add AI-ChrisLee/execution-design
/plugin install execution-design@execution-design
```

Then run the plugin with `squad/mep/<name>/` as its project root, phases 1, 2, 3 and 5
only. Phase 1: fill its `client.md` from the offer document and `notes.md`, every unknown
fact `UNKNOWN`, then print the 7 questions with their pre-filled answers for one yes; the
founder fixes any line and copies the review count and rating off Maps. On that yes, append
`answers yes <date>` as the last line of `client.md`, so a window that closes here resumes at
the questions and not past them. Phase 2: the plugin's 3 directions, the founder picks one.
Phase 3: one `index.html`, styles inline,
every image slot a painted placeholder, the form's action empty and its button disabled
with the plugin's own line under it. Phase 5: the 9 boxes graded, box 5 as a count, boxes
8 and 9 open, and any box the page actually fails open with them. Phases 4, 6 and 7 are
skipped and you say so in one line: no image files, no key, no Lighthouse, no analytics,
no redirects, no deploy.

Then the 3 captures, `shot-1.png`, `shot-2.png`, `shot-3.png` at 1920x1080: the top of the
page, the middle, the money action. A renderer was found at beat 0: capture them the way the
reference says. None: say in 3 lines how the founder takes them by hand and where to drop
them, and build the deck anyway; its demo slides fill in when the files land.

**The piece** (agency, content). HUMAN INPUT, one message: paste the buyer's current
piece (a post, a script, a newsletter) and name the channel. Then `piece.md`: theirs as
posted, then one piece in their voice for the same channel, on the slice. Text only.

**The structure** (consulting). `structure.csv`: the header row is the columns the
engagement would track, in the buyer's words; the rows are facts from `notes.md`, 5 at
most, none invented. A plain CSV: it opens in the founder's own spreadsheet or Notion, and
the reference carries the import path for the beat map.

**The screens** (software). Nothing on disk past the deck. The 3 screens are drawn in HTML
inside slides 5, 6 and 7 at beat 3: fake data carrying the buyer's real nouns, one flow
that ends on the money button, disabled, with one line under it saying nothing is wired.
When a real working screen exists, or gets built inside the 2 days, that screen goes on the
slides instead: capture it at 1920x1080 as `shot-1.png`, `shot-2.png`, `shot-3.png` the way
the reference says, and a drawn screen stands in only for what is not built. Nothing
deploys, no URL, the money button stays disabled.

Say what got written, one line per file, and move to the deck.

## Beat 3 · The deck

Write `deck.html` from the skeleton in the reference: `references/deck-cage.css` pasted
whole into `<style>`, the accent line under it from the roots file's `accent color` row
(`#146ef5` when the row is missing or reads "(none yet)"), one `<section class="slide">`
per slide, the rail on every slide (their name left, the slide number right), the viewer
script last. The 9 slides are the spine in the reference; slides 5, 6, 7 are the demo's
section. Slide 3 is dropped when `notes.md` carries no cost, and the deck is 8. The numbers
1 to 9 in the spine are names, not the rail: the rail counts the sections that exist, so a
deck with the cost slide dropped rails 1 to 8, and `deck.md`'s Slide column carries that
same rail number with `Skipped: the cost slide, no cost on the call` under the table.

Slide 1 takes an image when one exists. `cover.png` or `cover.jpg` in the folder goes
full-bleed behind the name (the cage's `.cover`: the image, its scrim, the name and town in
white on top). No file, on the site path: `shot-1.png` stands there the same way, and its
`onerror` drops the slide back to text until the capture lands. No file and no capture: the
cover stays text, the `h1` and one `.sub`, and nothing is made to fill it.

Every readable word in Inter. One subject per slide, the word that carries it the biggest
thing on it. No eyebrow or kicker label above a title. Numbers huge and tabular. No price of
the founder's anywhere. Nothing on a slide that `notes.md`, the offer document, the row, or
the founder's yes did not give: never a screenshot that was not captured, never a quote that
was not said.

Then `deck.md`, the beat map, one row per slide that exists, in the shape the reference
gives: what the founder says over it (1 or 2 lines, their voice, no price, in bold because
it is the line said out loud) and what is on it. Its closing lines say what was skipped,
which demo it holds, and where the PDF is; beat 4 appends `looked <date>` under them.

Then `deck.pdf`, when beat 0 found a renderer: the print command in the reference, then open
it once and check the page count matches the slide count. None found: one line in the chat
and in `deck.md`: print from the browser, File, Print, Save as PDF, one slide per page.

Open `deck.html` in the laptop's browser (or tell the founder to double-click it). Say what
got written, one line per file, and move to the look.

## Beat 4 · The look

Print one line, quoted from the deck, in this shape:

```
It names <buyer> in 3 places: <a fact of theirs>, <their place>, "<their words>".
```

On the cold path the third slot has no words in it. It carries the broken thing the deck
acted on, with no quote marks and the same observation label the plan used.

With no named buyer the line names nobody, so print this instead: `It is built on [their
name] and [their town]: <n> marked blanks, on <n> slides.` The gate under it reads: this one
is a shape, not a deck. Say go and I file it; the day your first call books, run `/mep
<name>` and it gets built for a person.

The site adds the plugin's box line. The open list is the boxes phase 5 actually graded
open, in order, never a fixed list: `9 boxes: <n> closed; open: 5 (<n> slots, 0 filled),
8, 9.` Boxes 5, 8 and 9 are open on every site (no image files, no deploy, the button
disabled). Box 2 joins them when the buyer's market writes in a non-Latin script and the
font fell back.

**STOP · GATE.** Then: "Open it. Arrow keys move it. Name anything that would read the
same for anyone else in their trade. I fix that and print this line again." Each named
thing gets fixed in the deck (and in the demo file it came from) and the line re-prints. A
fix that lands in `index.html` is not on the deck until the shot is retaken: re-capture
whichever of `shot-1.png`, `shot-2.png`, `shot-3.png` covers the section that changed, the
way `references/deck-shapes.md` says, before the line re-prints. With no renderer, say which
shot the founder has to retake by hand.
That is the whole grade; there is no score. When the founder has nothing left to name, one
closing line: it goes on the screen in the sales hour at the pitch beat, or leaves after as
`deck.pdf` with the one line `CLAUDE.md` gives for sending after a call, by their hand.
Nothing gets sent from here. Then append `looked <date>` as the last line of `deck.md`.

## Rules

- Every message to the founder is scannable: a short header, then bullets or a table.
- Never send. Never deploy. No URL, no domain, no backend, no login, no payments, no form
  wired to anything, no image file past the 3 captures (a cover the founder drops in is
  theirs, not one this skill makes), no new account, no key, no paid seat. Nothing on the
  buyer's domain, in their name or on their accounts until money clears.
- Never price past `squad/business.md`. The founder's price is that document's line, it
  appears on no slide, and neither does any number worked out from it. The only money on a
  slide is the buyer's own: what the problem costs them, off `notes.md`, or the prices in
  their own services table inside the site capture, or the plugin's `quote only` where the
  buyer publishes none.
- Never invent a number, a name or a need. A number not in `notes.md` does not appear.
  `UNKNOWN` stays `UNKNOWN` and is never a question mid-build. A cost no call gave is a
  dropped slide, never a guess.
- Never invent a screenshot or a quote. A capture is of the page that exists; a slide with
  no capture yet carries a labeled hole. A quote is verbatim, labeled, dated, in the
  language it was said, never paraphrased.
- Never save an observation as a quote. On the cold path nobody has said anything yet, so
  what you can see from outside is labeled an observation and carries no quote marks, and
  only words a person actually wrote or said are quoted.
- One buyer, one slice, one deck. The moment the deck would work for the shop next door,
  it is a template, and the founder built the wrong thing.
