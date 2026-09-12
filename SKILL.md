---
name: mep
description: Use this when the offer document exists and the founder needs the deck to put on the screen in the sales hour. They say "/mep", "Build my deck.", "build the MEP", "build that" right after a call with a named person (it runs on that person's folder), "/mep [name]" (the name picks the folder), "build the deck for [company] off my cold list" (the cold path, for a company on squad/cold-list.md nobody has talked to yet), or "continue the MEP" (picking a stopped run back up). It reads squad/business.md and the buyer's own words, plans one slice, stops for go, builds the demo the model calls for, and writes one deck.html of 9 slides with its beat map and deck.pdf into squad/mep/<name>/; nothing deploys, nothing gets a URL, nothing is invented about the buyer.
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

Two days is enough to build the real thing: build it and capture it onto the demo slides.
The site path does that. Two days is not enough: the deck alone, and the piece, the structure
drawn in the deck, or the 3 drawn screens stand in for the product, which gets built after
the money.

The buyer is somebody the founder already talked to. A company off `squad/cold-list.md`
nobody has talked to yet takes the cold path, the appendix at the end of this file.

This skill runs in ANY founder's repo. Read `accent color` and `clients` off
`.claude/squad-roots.md` when they exist; otherwise `#146ef5` and `squad/clients/`. This run
writes no roots row, and the rail on these slides carries the buyer's name.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE READ | AUTO: the install check (`references/deck-shapes.md`, `references/deck-cage.css`), `squad/business.md` (the model), the buyer folder. HUMAN INPUT, one question, only when `squad/clients/` holds more than one folder and neither a name nor "build that" picked one, or the name given has no folder and no cold-list row |
| 1 THE PLAN | AUTO: `squad/mep/<name>/plan.md`, its path and 4 lines printed, then **STOP · GATE: go, or a different slice** |
| 2 THE DEMO | AUTO by model. The site carries the plugin's own turns, HUMAN INPUT 3 times: the install once per laptop, a yes on the 7 pre-filled answers, the pick of one direction from 3; then the 3 captures. The piece carries HUMAN INPUT once: the paste of the buyer's current piece. The structure and the screens carry none |
| 3 THE DECK | AUTO: `deck.html`, `deck.md`, and `deck.pdf` when a renderer is found |
| 4 THE LOOK | AUTO, one line, then **STOP · GATE: the founder names anything that would read the same for anyone else; nothing to name means done** |

The beat numbers ARE the step numbers below. 2 gates, no more; the plugin's turns inside
beat 2 are the plugin's stops. Never pause an automated beat to ask a small question (an
unknown fact is `UNKNOWN`, never a question); never run through a gate because the answer
seems obvious.

**Resuming.** The rule keys on the OUTPUTS, never on a session's memory: check them in this
order and continue at the first one missing or incomplete.

| Missing or incomplete | Resume at |
|---|---|
| `squad/business.md` does not exist | stop: the Winning Offer writes it, warm (g4) or cold (g5) |
| the trigger is "continue the MEP" | resolve `<name>` from `squad/mep/`: the one folder there whose files are incomplete, the newest when more than one. None incomplete falls through to beat 0 |
| no `squad/mep/<name>/plan.md` | beat 0 |
| `plan.md` exists and its last line carries no `go <date>` | beat 1, THE GATE ONLY: print its path and the 4 lines |
| `plan.md` says go and the demo is missing or partial (the site: no `index.html` means the plugin again from the first phase `client.md` does not already answer (no `client.md`: phase 1; its `style` row `UNKNOWN`: phase 2; otherwise phase 3), fewer than 3 `shot-*.png` means the captures; the piece: `piece.md` with no `## THE PIECE`; the structure and the screens have no demo file) | beat 2, at the file it names |
| the demo is whole and `deck.html` or `deck.md` is missing | beat 3 |
| `deck.html` exists, `deck.pdf` does not, and a renderer is found | beat 3, the PDF only |
| `deck.html` and `deck.md` exist and `deck.md`'s last line carries no `looked <date>` | beat 4 |
| `deck.md` carries `looked <date>` | nothing to resume: say the deck is done and where it is |

Never re-ask a yes the files already show, and never rebuild a file that opens.

## The outputs (one folder, every run)

All of it in `squad/mep/<name>/`. The folder name matches the buyer's folder under
`squad/clients/`, lowercased and hyphenated, and `<name>` below stands for the one this run
resolved.

1. `plan.md`: one screen, the plan, with `go <date>` as its last line once the founder says go.
2. `deck.md`: the beat map, one row per slide: the slide, what the founder says (in bold),
   what is on it. Its last line is `looked <date>` once the founder has nothing left to
   name at beat 4.
3. `deck.html`: the deck, one self-contained file, the cage CSS inline, one `<section>` per
   slide at 1920x1080, arrow keys and a click between slides, a print sheet at one slide per
   page.
4. `deck.pdf`: when a headless browser is found on the laptop. Otherwise the founder prints it
   from the browser and `deck.md` says so.
5. The demo files, by model: `index.html` with the plugin's `client.md` beside it and
   `shot-1.png`, `shot-2.png`, `shot-3.png` (the site); `piece.md` (the piece); nothing
   past the deck for the structure and the screens, which are drawn inside it.

Nothing else gets written.

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
<name>`). On "build that", it is the client folder whose `notes.md` was written last. On a
resume with no name, it is the folder the resume table above resolved. Otherwise the one
folder under `squad/clients/`; none there and no name: say so in one line, name g4, and
stop. More than one folder and no name: one question, in one message, the folders listed
one line each with their THE IDEA line. Read `notes.md` whole (QUOTES, THE PROBLEM, THE
COST, WHAT THEY PAY NOW, THE IDEA, THE MODEL, THE NEXT STEP) and `transcript.md` for the
buyer's nouns.

**Then the renderer**, so beat 2 and beat 3 know it: look for headless Chrome or Edge at
the paths the reference lists, and remember which one answered, or that none did. No
install is asked for.

This beat prints nothing on its own; the plan is the first thing the founder sees.

## Beat 1 · The plan

Write `squad/mep/<name>/plan.md`, one screen, in this shape:

```
# MEP · <buyer name>

THE BUYER   <name>, <what they do>, <their town>
THE SLICE   "<the one problem, in their words>" (<the label notes.md gives it>)
THE MODEL   <agency | consulting | software>

THE DEMO    <the site: 3 captures | the piece beside theirs | the structure, N rows | 3 screens>
1. <what slide 5 shows>
2. <what slide 6 shows>
3. <what slide 7 shows>

THE SLIDES
1. <their name, their town>, behind them <shot-1.png on the site path | nothing>
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
```

The slice is one quote, the strongest problem line in `notes.md`, verbatim, with the label
`notes.md` gives it; the deck is built on that one problem and nothing wider. The demo's 3
lines and the not-in-it line come from the demo's section in the reference, with the
buyer's nouns filled in. Slide 1's line names what stands behind the name: `shot-1.png` on
the site path, or nothing.

**STOP · GATE.** Print the file's path, then its THE BUYER, THE SLICE, THE MODEL and THE
DEMO lines, then one line: "Go, or a different slice: name it, or point at another quote,
and I rewrite this." Never the whole file. A different slice rewrites the plan and prints
those lines again. On go, append `go <date>` as the plan's last line, then build.

## Beat 2 · The demo

Read the demo's section in `references/deck-shapes.md` and follow it exactly. In short:

**The site** (agency). Check the `execution-design` plugin first: its `design` skill and
the `/execution-design:design` command answer. Missing, print these 2 lines, once per
laptop, with one line under them (paste them, `/reload-plugins` if asked, then type
"continue the MEP"), and stop until it is in:

```
/plugin marketplace add AI-ChrisLee/execution-design
/plugin install execution-design@execution-design
```

Then run the plugin with `squad/mep/<name>/` as its project root, phases 1, 2 and 3
only. Phase 1: fill its `client.md` from the offer document and `notes.md`, every unknown
fact `UNKNOWN`, then print the 7 questions with their pre-filled answers for one yes; the
founder fixes any line, and the review count and rating off Maps are optional ("I do not
know" leaves them `UNKNOWN`). Phase 2: the plugin's 3 directions, the founder picks one. Phase 3: one
`index.html`, styles inline, every image slot a painted placeholder, the form's action
empty and its button disabled with the plugin's own line under it. Phases 4 to 7 are
skipped, said in one line: they belong to the paid build, after the money.

Then the 3 captures, `shot-1.png`, `shot-2.png`, `shot-3.png` at 1920x1080: the top of the
page, the middle, the money action. A renderer was found at beat 0: capture them the way the
reference says. None: say in 3 lines how the founder takes them by hand and where to drop
them, and build the deck anyway; its demo slides fill in when the files land.

**The piece** (agency, content). HUMAN INPUT, one message: paste the buyer's current
piece (a post, a script, a newsletter) and name the channel. Then `piece.md`: theirs as
posted, then one piece in their voice for the same channel, on the slice. Text only.

**The structure** (consulting). Nothing on disk past the deck. The table is drawn inside
slides 5, 6 and 7 at beat 3: the columns the engagement would track, in the buyer's words;
the rows facts from `notes.md`, 5 at most, none invented.

**The screens** (software). Nothing on disk past the deck. The 3 screens are drawn in HTML
inside slides 5, 6 and 7 at beat 3: fake data carrying the buyer's real nouns, one flow
that ends on the money button, disabled, with one line under it saying nothing is wired.

Say what got written, one line per file, and move to the deck.

## Beat 3 · The deck

Write `deck.html` from the skeleton in the reference: `references/deck-cage.css` pasted
whole into `<style>`, the accent line under it, the first hex on the roots file's `accent color` row
(`#146ef5` when the row is missing or carries no bare hex), one `<section class="slide">`
per slide, the rail on every slide (their name left, the slide number right), the viewer
script last. The 9 slides are the spine in the reference; slides 5, 6, 7 are the demo's
section. Slide 3 is dropped when `notes.md`'s THE COST carries no number and no words of
theirs (a question written there is not a cost), and the deck is 8. The numbers 1 to 9 in
the spine are names, not the rail: the rail counts the sections that exist, so a deck with
the cost slide dropped rails 1 to 8, and `deck.md`'s Slide column carries that same rail
number with `Skipped: the cost slide, no cost on the call` under the table.

Slide 1 on the site path takes `shot-1.png` full-bleed behind the name (the cage's
`.cover`: the image, its scrim, the name and town in white on top), and its `onerror` drops
the slide back to text until the capture lands. Every other path keeps a text cover, the
`h1` and one `.sub`, and nothing is made to fill it.

The file keeps the rules under the reference's deck file section: every readable word in
Inter, one subject per slide, no price of the founder's, nothing on a slide that `notes.md`,
the offer document or the founder's yes did not give.

Then `deck.md`, the beat map, one row per slide that exists, in the shape the reference
gives: what the founder says over it (1 or 2 lines, their voice, no price, in bold) and
what is on it. Its closing lines say what was skipped, which demo it holds, and where the
PDF is; beat 4 appends `looked <date>` under them.

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

**STOP · GATE.** Then: "Open it. Arrow keys move it. Name anything that would read the
same for anyone else in their trade. I fix that and print this line again. Nothing to name:
say so." Each named thing gets fixed in the deck (and in the demo file it came from),
`deck.pdf` is rendered again when beat 0 found a renderer, and the line re-prints. A fix
that lands in `index.html` is not on the deck until the shot is retaken: re-capture
whichever of `shot-1.png`, `shot-2.png`, `shot-3.png` covers the section that changed, the
way `references/deck-shapes.md` says, before the PDF and the line. With no renderer, say
which shot the founder has to retake by hand.
That is the whole grade. When the founder has nothing left to name, and no `shot-*.png` the
plan names is missing (one still missing: say which, and that "continue the MEP" runs this
look again once it is in the folder), append `looked <date>` as the last line of `deck.md`,
then one line: it goes on the screen in the sales hour at the pitch beat, or leaves after
as `deck.pdf`, sent by their hand with one line, "I built this after we talked. Want to try
this together?"

## Rules

- Never send. Never deploy. Nothing on the buyer's domain, in their name or on their
  accounts until the money clears; the full list is the reference's Not in any deck.
- Never price past `squad/business.md`. The founder's price is that document's line, it
  appears on no slide, and neither does any number worked out from it. The only money on a
  slide is the buyer's own: what the problem costs them, off `notes.md`, or the prices in
  their own services table inside the site capture, or the plugin's `quote only` where the
  buyer publishes none.
- Never invent a number, a name or a need. A number appears only when `notes.md` carries
  it, or the founder typed it at the plugin's yes (the review count and rating off Maps).
  `UNKNOWN` stays `UNKNOWN` and is never a question mid-build. A cost no call gave is a
  dropped slide, never a guess.
- Never invent a screenshot or a quote. A capture is of the page that exists; a slide with
  no capture yet carries a labeled hole. A quote is verbatim, labeled, dated, in the
  language it was said, never paraphrased.
- One buyer, one slice, one deck. The moment the deck would work for the shop next door,
  it is a template, and the founder built the wrong thing.

## Appendix · The cold path (o2)

The founder says "build the deck for <company> off my cold list", or the name they gave has
no folder under `squad/clients/` and does have a row in `squad/cold-list.md`. Nobody has
talked to this company, so there is no folder, no `notes.md`, no `transcript.md` and no
quote. The 5 beats run the same way with these differences:

**Beat 0.** Read that row instead: the company, its town, its trade, and the one broken-thing
sentence the cut carries, plus what you can see from outside. Every line of it is labeled an
observation with the list's own `cut <date>`, and every fact the row does not carry is
`UNKNOWN`. The folder is `squad/mep/<company>/`, lowercased and hyphenated. A name in
neither place is one question, asked once: which one, off the folders under
`squad/clients/` listed one line each with their THE IDEA line (and the companies on
`squad/cold-list.md` when that file exists). `references/deck-shapes.md` (A cold buyer)
says what each slide does when there are no words.

**Beat 1.** The slice is not a quote and never wears quote marks. The line reads
`THE SLICE   <the row's broken-thing sentence> (observation · cold list <cut date>)`, and
the buyer line is the row's own company, trade and town. The gate's second half reads:
point at another thing you can see from outside.

**Beat 4.** The look line's third slot has no words in it. It carries the broken thing the
deck acted on, with no quote marks and the same observation label the plan used.

Never save an observation as a quote. What you can see from outside is labeled an
observation and carries no quote marks; only words a person actually wrote or said are
quoted.
