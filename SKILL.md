---
name: mep
description: Use this when the offer document exists and the founder needs the thing to put on the screen in the sales hour. They say "/mep", "build my shell", "build the MEP", "build that" right after a call with a named person (it runs on that person's folder), "/mep [name]" (the name picks the folder), or "continue the MEP" (picking a stopped run back up). It reads squad/business.md and the buyer's own words, writes a one-screen plan (the buyer, the one slice of their problem in their words, what the shell shows, what is not in it, day one and day two), stops for go, then builds one local file by business model: one page on the design cage, a Notion structure as a CSV, one piece in the buyer's voice, or a 3-screen clickable prototype. Nothing deploys, nothing gets a URL, nothing is invented about the buyer. The founder screen-shares it and sends by hand.
---

# The MEP

The Minimum Executable Product: the shell of the offer, built for one buyer the founder
already talked to, real enough to put on a screen in the sales hour, inside the 2 days the
lesson scopes. Your work, in one line: **read the offer document and the buyer's own words,
plan the one slice, build the one file a laptop builds with nothing new installed, and hand
it to the founder to show.** The founder's part: go, one look, the screen share, the send by
hand.

The shell is a sales object for one person. Finished on the surface, rough underneath. The
test it has to pass is strict: if it could be sent to anybody in the trade, it is a
template, and the buyer treats it like one. So the shell names this buyer, in their facts,
their place and their words, or it is not done.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance
file every member-run skill reads first (founder name, voice sample, the `clients` path),
and its values win over the `squad/` paths written below, which are worked examples. A row
reading "(none yet)" is an unanswered field, not an override: the worked-example path
stands. This run writes no roots row; the shell carries the buyer's brand, and the roots
file is the founder's.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE READ | AUTO: the install check, `squad/business.md`, the buyer's folder (one exception: HUMAN INPUT, which person, only when `squad/clients/` holds more than one folder) |
| 1 THE PLAN | AUTO, one screen, then **STOP · GATE: go, or a different slice** |
| 2 THE BUILD | AUTO, one file by model. The page carries the plugin's own turns, HUMAN INPUT 3 times: the install once per laptop, a yes on the 7 pre-filled answers, the pick of one direction from 3. The piece carries HUMAN INPUT once: the paste of the buyer's current piece |
| 3 THE LOOK | AUTO, one line, then **STOP · GATE: the founder names what would read the same for anyone else; nothing to name means done** |

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
| `squad/business.md` does not exist | stop: G5 forges it, or G4's draft when a call handed one over |
| no `squad/mep/<first-last>/plan.md` | beat 0 |
| `plan.md` exists and its last line carries no `go <date>` | beat 1, THE GATE ONLY: print the plan, never rewrite it |
| `plan.md` says go and the file is missing or partial (the page: no `client.md` means the 7 answers, `client.md` with `style: UNKNOWN` means the direction, no `index.html` means the build; the structure: `structure.csv` with no `notion.md`; the piece: `piece.md` with no `## THE PIECE`; the prototype: fewer than 3 screens) | beat 2, at the file it names |
| the file is whole and the founder has not looked | beat 3 |

Never re-ask a yes the files already show, and never rebuild a file that opens.

## The outputs (2 outputs, every run)

1. `squad/mep/<first-last>/plan.md`: one screen, the plan, with `go <date>` as its last
   line once the founder says go. The folder name matches the buyer's folder under
   `squad/clients/`; with no named buyer it is the buyer type off the offer document's WHO
   line, lowercased and hyphenated.
2. The shell, one by model, in the same folder: `index.html` for the page (the plugin
   writes its own `client.md` beside it, the 7 answers it builds from, and nothing else);
   `structure.csv` plus `notion.md` for the structure; `piece.md` for the piece;
   `prototype/index.html` for the prototype.

No `send.md`, no `log.md`, no roots row, no `squad/demos/`, no `images.md`, no `images/`,
no second page, no second flow. Nothing else gets written.

## Step 0 · The read

**First, a self-check.** `references/shell-shapes.md`, inside this skill's folder next to
`SKILL.md`, must open. Missing means stop and tell the founder to finish the install: copy
the whole skill folder, `references/` included.

**Then the offer document.** Open `squad/business.md`. Read THE SENTENCE, THE MODEL, WHO,
THE STACK and PRICE; a file holding only `## THE DRAFT` and no `confirmed` stamp is
enough (its who, deliverable, model and price lines). No file at all: say so in one line,
name G5 (the market path) or G4 (a warm call drafts it), and stop. The model word, with
THE STACK when the model is agency, decides the shape by the table in
`references/shell-shapes.md`. The shape is never a question.

**Then the buyer.** The folder is the name in the trigger when one was given ("build that"
right after a call, `/mep <name>`); otherwise the one folder under `squad/clients/`,
`self/` and `references/` not counted (the second is W1's screenshot folder, never a
person). More than one folder and no name: the only question this beat asks, in one
message, the folders listed one line each with their THE IDEA line. Read
`notes.md` whole (QUOTES, THE PROBLEM, THE COST, WHAT THEY PAY NOW, THE IDEA, THE
MODEL, THE NEXT STEP) and `transcript.md` for the buyer's nouns. A number appears in the
shell only when `notes.md` carries it. Read the language off the quotes: a non-Latin
script is one LANGUAGE line in the plan (the reference names the gap).

**No named buyer yet** (the market-path founder, `self/` at most): build for the buyer
type in WHO into `squad/mep/<buyer-type>/`, every buyer-specific noun a marked blank in
square brackets, and rebuild under a name the day the first call books. The reference
carries the marking.

This beat prints nothing on its own; the plan is the first thing the founder sees.

## Step 1 · The plan

Write `squad/mep/<first-last>/plan.md`, one screen, in this shape, and print it whole:

```
# MEP · <buyer name, or the buyer type>

THE BUYER   <name>, <what they do>, <their town>
THE SLICE   "<the one problem, in their words>" (<the label notes.md gives it>)
THE SHAPE   <the page | the structure | the piece | the prototype> (THE MODEL: <word>)

IT SHOWS
1. <the first thing the shell shows>
2. <the second>
3. <the third>

NOT IN IT
<the shape's list from the reference, one line>

DAY ONE
- <task>
- <task>

DAY TWO
- <task>
- <task>

LANGUAGE   <only when the buyer's market writes in a non-Latin script>
```

The slice is one quote, the strongest problem line in `notes.md`, verbatim, with the label
`notes.md` gives it (a warm call, or the founder's recollection); the shell is built on
that one problem and nothing wider. The 3 things it shows, the not-in-it list and the 2
day lists come from the shape's section in the reference, with the buyer's nouns filled
in. No XYZ line, no call question, no point
system, no clock.

**STOP · GATE.** One line under the plan: "Go, or a different slice: name it, or point at
another quote, and I rewrite this." A different slice rewrites the plan and prints it again.
On go, append `go <date>` as the plan's last line, then build.

## Step 2 · The build

Read the shape's section in `references/shell-shapes.md` and follow it exactly. In short:

**The page** (agency). Check the `execution-design` plugin first: its `design` skill and
the `/execution-design:design` command answer. Missing, print these 2 lines, once per
laptop, and stop until it is in (a reload request means `/reload-plugins`):

```
/plugin marketplace add AI-ChrisLee/execution-design
/plugin install execution-design@execution-design
```

Then run the plugin with `squad/mep/<first-last>/` as its project root, phases 1, 2, 3
and 5 only. Phase 1: fill its `client.md` from the offer document and `notes.md`, every
unknown fact `UNKNOWN`, then print the 7 questions with their pre-filled answers for one
yes; the founder fixes any line and copies the review count and rating off Maps. Phase 2:
the plugin's 3 directions, the founder picks one. Phase 3: one `index.html`, styles
inline, every image slot a painted placeholder, the form's action empty and its button
disabled with the plugin's own line under it. Phase 5: the 9 boxes graded, box 5 as a
count, boxes 8 and 9 open, and any box the page actually fails open with them. Phases 4,
6 and 7 are skipped and you say so in one line: no image files, no key, no Lighthouse, no
analytics, no redirects, no deploy.

**The structure** (consulting). `structure.csv`: the header row is the columns the
engagement would track, in the buyer's words; the rows are facts from `notes.md`, 5 at
most, none invented. `notion.md`: the one line that sits above the database, the one
view, and the import path (Settings, Import, CSV, or `/csv` on a page; map each column).
The founder's own Notion, no connector.

**The piece** (agency, content). HUMAN INPUT, one message: paste the buyer's current
piece (a post, a script, a newsletter) and name the channel. Then `piece.md`: theirs as
posted, then one piece in their voice for the same channel, on the slice. Text only.

**The prototype** (software). `prototype/index.html`: 3 screens, hash links between
them, fake data carrying the buyer's real nouns, one flow that ends on the money button,
disabled, with one line under it saying nothing is wired.

Open the file in the laptop's browser when it is a page or a prototype (or tell the founder
to double-click it). Then say what got written, one line per file, and move to the look.

## Step 3 · The look

Print one line, quoted from the file, in this shape:

```
It names <buyer> in 3 places: <a fact of theirs>, <their place>, "<their words>".
```

The page adds the plugin's box line. The open list is the boxes phase 5 actually graded
open, in order, never a fixed list: `9 boxes: <n> closed; open: 5 (<n> slots, 0 filled),
8, 9.` Boxes 5, 8 and 9 are open on every shell (no image files, no deploy, the button
disabled). Box 2 joins them when the buyer's market writes in a non-Latin script and the
font fell back.

**STOP · GATE.** Then: "Open it. Name anything that would read the same for anyone else
in their trade. I fix that and print this line again." Each named thing gets fixed in the
file and the line re-prints. That is the whole grade; there is no score. When the founder
has nothing left to name, one closing line: it goes on the screen in the sales hour, and
`/the-close pre <name>` writes the one question before the call. Nothing gets sent from
here.

## Rules

- Every message to the founder is scannable: a short header, then bullets or a table.
- Never send. Never deploy. No URL, no domain, no backend, no login, no payments, no form
  wired to anything, no image file, no new account, no key, no paid seat. Nothing on the
  buyer's domain, in their name or on their accounts until money clears.
- Never price past `squad/business.md`. The founder's price is that document's line and
  appears nowhere in the shell. A price on the shell is the buyer's own, from `notes.md`,
  or the plugin's `quote only`.
- Never invent a number, a name or a need. A number not in `notes.md` does not appear.
  `UNKNOWN` stays `UNKNOWN` and is never a question mid-build.
- Never paraphrase a quote. Verbatim, labeled, dated, in the language it was said.
- One buyer, one slice, one file. The moment the shell would work for the shop next door,
  it is a template, and the founder built the wrong thing.
