---
name: mep
description: Use this when the offer document exists and the founder needs the deck for the sales hour. They say "/mep", "Build my deck.", "/mep [name]" (the name picks the folder), "build the deck for [company] off my cold list" (the cold path), or "continue the MEP". It reads squad/business.md and the buyer's own words, plans one slice, stops for go, builds the demo the model calls for, and writes deck.html, deck.md and deck.pdf into squad/mep/<name>/; nothing deploys, nothing gets a URL, nothing is invented about the buyer.
---

# The MEP

Open a fresh run with this line, word for word:

This skill is a base. Once you have done it your way, tell your squad "update the skill to do it like this."

One deck for one buyer, on the one problem he said out loud, built from what the squad already
holds. It goes on the screen at minute 40 of the sales hour, or leaves as `deck.pdf`.

This skill runs in any founder's repo. Read `accent color` and `clients` off
`.claude/squad-roots.md` when they exist; otherwise `#146ef5` and `squad/clients/`. This run
writes no roots row.

## Never

Read this block every run.

- Never send, never deploy. Nothing on the buyer's domain, in his name or on his accounts until
  the money clears; the reference's Not in any deck holds the full list. Production happens
  after the money.
- Never price past `squad/business.md`. The founder's price is on no slide, and neither is any
  number worked out from it. The only money on a slide is the buyer's own: what the problem
  costs him off `notes.md`, the prices in his own services table inside the capture, or the
  plugin's `quote only`.
- Never invent a number, a name or a need. A number appears only when `notes.md` carries it, or
  the founder typed it at the plugin's yes. `UNKNOWN` stays `UNKNOWN`, never a question
  mid-build. A cost no call gave is a dropped slide, never a guess.
- Never invent a screenshot or a quote. A capture is of the page that exists; a slide with no
  capture yet carries a labeled hole. A quote is verbatim, labeled, dated, in the language it
  was said. Never save an observation as a quote.
- One buyer, one slice, one deck. The moment it would work for the shop next door, it is a
  template.
- Every readable word in Inter, one subject per slide, nothing on a slide that `notes.md`, the
  offer document or the founder's yes did not give.
- Nothing else gets written. It all lands in `squad/mep/<name>/`, lowercased and hyphenated,
  matching his folder under `squad/clients/`.

## The read

`references/deck-shapes.md` and `references/deck-cage.css` must open. Either missing: say to run
the install paste again, and stop.

`squad/business.md`: THE SENTENCE, THE MODEL, WHO, THE STACK, PRICE. No `confirmed <date>` stamp
is fine. THE MODEL, with THE STACK when it is agency, picks the demo by the reference's table,
never a question. No file: say so in one line, name the Winning Offer (g4 warm, g5 cold), stop.

The buyer: the name in `/mep <name>`, else the one folder under `squad/clients/`, else the
folder whose `notes.md` was written last. Neither: say so in one line, name g4, stop. Read his
`notes.md` (THE COST decides the cost slide, and a question written there is not a cost) and
`transcript.md` for his nouns.

The renderer: Chrome or Edge at the reference's paths, and remember which answered. None: say so
once, never ask for an install.

## The plan

Write `squad/mep/<name>/plan.md`:

```
# MEP · <buyer name>

THE BUYER   <name>, <what they do>, <their town>
THE SLICE   "<the one problem, in his words>" (<the label notes.md gives it>)
THE MODEL   <agency | consulting | software>
THE DEMO    <the site: 3 captures | the piece beside his | the structure | 3 screens>
```

The slice is the strongest problem line in `notes.md`, verbatim, with its label. Print the path
and those 4 lines. Wrong problem: the founder points at another line and it rewrites. On go, build.

## The demo

Read the demo's section in `references/deck-shapes.md` and follow it.

**The site** (agency). The `execution-design` plugin builds it. Missing: print these 2 lines,
say to paste them and then type "continue the MEP", and stop. It carries on at the demo.

```
/plugin marketplace add AI-ChrisLee/execution-design
/plugin install execution-design@execution-design
```

Phases 1, 2 and 3 only, at `squad/mep/<name>/`: the brief pre-filled off the offer document and
`notes.md` with every unknown fact `UNKNOWN`, printed for one yes; 1 pick of 3 directions before
anything is built; one `index.html`, the plugin's `client.md` beside it, with the form's action
empty and its button disabled under the plugin's own line. Phases 4 to 7 are the paid build,
after the money; say that in one line.
Then `shot-1.png`, `shot-2.png` and `shot-3.png` at 1920x1080 the way the reference says. No
renderer: name those 3 files for the founder to shoot by hand, and build the deck anyway.

**The piece** (agency, content). One paste: his current piece and its channel. Then `piece.md`,
his as posted, then the piece in his voice on the slice. Text only.

**The structure** (consulting). His columns, his facts from `notes.md` as rows, 5 at most, drawn
on slides 5, 6 and 7.

**The screens** (software). 3 screens carrying his real nouns, one flow, the money button
disabled with one line under it saying nothing is wired.

## The deck

`deck.html` from the reference's skeleton, with the accent line under the cage CSS: the first
hex on the roots file's `accent color` row, `#146ef5` when that row is missing or carries no
bare hex.

9 slides, the spine in the reference. 8 when `notes.md`'s THE COST carries no number and no
words of his: the cost slide is dropped, and `deck.md` says so.

Under every image on a slide, one short line: a `.note` under the card, above the rail, 8 words
at most. It wins over the reference's "the capture and nothing else". Slide 1's cover already
carries his town in `.sub`; that is its line.

`deck.md`: what the founder says over each slide, one row per slide that exists, his own voice,
no price of the founder's. It ends on the PDF line, and the reference's `looked <date>` last
line is not written.

`deck.pdf` when Chrome or Edge answered, by the reference's print command. None: `deck.md`'s PDF
line says print from the browser, File, Print, Save as PDF, one slide per page.

Open `deck.html` in the browser. Say what got written, one line per file.

## The look

Print one line, quoted from the deck:

```
It names <buyer> in 3 places: <a fact of his>, <his place>, "<his words>".
```

Then ask once: name anything that would read the same for anyone else in his trade. Each one is
fixed in the deck and in the demo file it came from; a fix in `index.html` is not on the deck
until its shot is retaken, and the PDF with it.

Done: it goes on the screen at minute 40, or leaves as `deck.pdf`, sent by the founder's hand.

## Resuming

"continue the MEP" picks a stopped run back up; any other re-run starts at the read. Both key on
the files in `squad/mep/<name>/`, never on a session's memory: continue at the first one missing.
No `plan.md`, the read. A plan and no demo, the demo on "continue the MEP" (go was already said);
on any other trigger, print the plan and wait for go. The demo whole and no deck, the deck. A deck, the look. Never re-ask a
yes the files already show, and never rebuild a file that opens.

## The cold path

"build the deck for <company> off my cold list", or a name with no folder under `squad/clients/`
that has a row on `squad/cold-list.md`. Read that row instead of a folder, into
`squad/mep/<company>/`. Every line off it is labeled `(observation · cold list <cut date>)` and
carries no quote marks. Nobody has talked to this company, so the cost slide is dropped.
`references/deck-shapes.md` (A cold buyer) says what each slide does when there are no words.
