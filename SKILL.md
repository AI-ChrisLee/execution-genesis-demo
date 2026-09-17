---
name: the-demo
description: Use this when the offer page exists and the founder wants the demo. They say "/the-demo" (it asks who the demo is for) or "/the-demo <business>, <their website or page>" (a real business, read off its page). It reads squad/business.md, connects Higgsfield or Notion when the shape needs it, builds a working first version in squad/demos/<business>/ right away, and changes it 1 note at a time until the founder says done. No deck, no deploy, no made-up facts, and it never sends anything.
---

# The Demo

The first message of a run with no `squad/demos/` folder yet opens with this line, word for word:

> This agent is a base. Once you have done it your way, tell your squad "update the agent to do it like this."

1 output: a working demo of the founder's offer, built for 1 business, in `squad/demos/<business>/`
(and, for a program, on a board in the founder's own Notion). The buyer sees the thing working before
they pay. Nothing else gets written.

## Never

- Never a deck, slides or a PDF.
- Never deploy it, host it, or give it a URL or a domain.
- Never log into, post to, or write in the buyer's accounts (their site, their Instagram, their Notion,
  their Google listing) before they pay. The demo lives in the founder's folder and the founder's Notion.
- Never make up a fact: a name, number, price, date, review, rating, testimonial, year, award or client.
  A fact nobody gave stays blank.
- Never a real person's face, a logo, or readable text in a generated image. Never upload the buyer's
  photos. A generated photo shows their kind of place and work, and nothing on the demo calls it theirs.
- Never spend a Higgsfield credit without printing the cost and getting a yes.
- Never the founder's price on the demo.
- Never send. The founder records the Loom and sends the message by hand.
- Never ask a first-run question from `CLAUDE.md` in the middle of a run. It waits until `Next: /the-close.`
  is printed.

## 1. Read the page

`references/shapes.md`, `references/no-slop.md`, `references/web-standard.md` and the 4 CSV files next
to them must open. Any missing: say the agent folder was copied without its `references/`, and stop.

Read `squad/business.md`: THE SENTENCE, WHO, THE PROBLEM, THE SHAPE, THE PROMISE, BUYER WORDS.
No file: print `Run /the-winning-offer first. The demo is built off that page.` and stop.

Print the shape line for THE SHAPE, from the table in `references/shapes.md` (on `/the-demo` alone, as
part of the first message in step 3). From here on, read that shape's section, plus The folder,
Higgsfield (content and website) and The Loom.

## 2. Connect first

- **Content and website:** Higgsfield, by the 3 steps under Higgsfield in `references/shapes.md`. Those
  steps decide go on or stop.
- **Consulting program:** Notion. Tools ending in `notion-create-database`, `notion-create-view` and
  `notion-create-pages` exist in this session, loaded or deferred: go on. Deferred: load them, plus
  `notion-fetch`, `notion-update-page`, `notion-update-view` and `notion-update-data-source`, in 1 tool
  search. None of them: the steps under Connect in the Consulting program section, and this run stops.
- **Software:** nothing to connect. Skip this step without a word.

## 3. Who it is for

A business that already has a folder under `squad/demos/` holding the shape's build: open it and go to
step 6.

**`/the-demo` alone:** the first message is, in this order: the base line (first run only), the shape
line, then the shape's 1 message (the question and its facts list, together). Some messages carry lines
filled in from `squad/business.md` or the trade row first; the shape's section says which. Then wait.
An answer that carries a link is a real run. An answer missing what the build cannot start without
(the shape's **Must have** line in `references/shapes.md`): ask for those once, in 1 line, and wait.
That same line also asks for FIRST NAME when it is blank, the role of every person named with no role,
and on software for USER. Everything else stays blank.

**`/the-demo <business>, <link>`:** a real run. Read the link by the rules under A real run in
`references/shapes.md`: `curl -sL` first, WebFetch only when curl gives nothing. A name with no link:
ask for the link once. A website run then looks at their current site first (Website, Their site
first, in `references/shapes.md`).

Then write `squad/demos/<business>/facts.md` and `notes.md` (The folder, in `references/shapes.md`):
1 line per fact with its source, every field nobody gave under `## Blank`. A blank never gets filled
with something that sounds nice.

## 4. The skeleton, right away

Build the shape's skeleton from `references/shapes.md` now. No plan, no pick, no question past the cost
line. THE PROBLEM and BUYER WORDS decide what goes first.

- **Website:** write `photos.md` and its prompts, get the cost of each, print the cost line, and wait for
  yes. On yes, make the photos in the order under The make, then build 1 `index.html` by
  `references/web-standard.md` (Website). A no: the page is built with no photos.
- **Content:** write The look lines and the prompts, get the cost of each, print the cost line for the
  whole set, and wait for yes. On yes, make the set in the order under The make, then write `posts.md`
  and `index.html`.
- **Consulting program:** the Notion calls, in order, then `board.md`.
- **Software:** 1 `index.html` with 3 screens by `references/web-standard.md` (Software), the task or
  the conversation working inside the page.

## 5. The no-slop check

Before the founder sees anything, run the items `references/no-slop.md` gives this shape (What runs on
each shape). Website, software and the content feed also get The look (`references/web-standard.md`).
Every generated photo, image and clip gets Generated images. A program gets The board. Fix every fail
and run the check again. Never show the demo with a note about what is wrong.

## 6. Show it, 1 note at a time

Open the demo once: `index.html` in the browser (`open` on a Mac, `start` on Windows, `xdg-open` on
Linux), or print the Notion link and open it. A run with no person at the screen (an eval, a routine)
skips the open and says so in 1 line. Then the blanks line (The folder, in `references/shapes.md`), and:

> Give me 1 note: what would they notice first that's wrong?

Each note:

1. Change only what the note names. Nothing next to it gets rebuilt. A note that names a person on
   `facts.md` puts that person's name and role, as `facts.md` gives them, into the change.
2. A note that needs a fact nobody gave: on a real run, look first in the pages already read. There:
   add it to `facts.md` with that URL, and name the URL in the 3 lines. Not there: ask for it in 1 line
   (1 value per card or record when the note is about each of them), then add each to `facts.md` with
   its source.
3. A new or redone photo, image or clip prints its credit cost and waits for yes.
4. Run the no-slop check on what changed, with The look or The board.
5. Say what changed in 3 lines or fewer, then `Reload the tab.` The first show is the only `open`.
6. Add 1 row to `notes.md`: `round · note · what changed · date`.
7. Print the note line again.

Repeat until the founder says done.

## 7. Done

Print the template test, quoted from the demo:

> It names <name> in 3 places: <a fact of theirs>, <their place>, "<their words>".

<their place> and <their words> are picked by The template test in `references/shapes.md`. Anything on
the demo that would read the same for the next business in the trade gets fixed first, logged as a
round in `notes.md`, and then the line is printed.

Then print:

> Record a Loom under 2 minutes over the open demo, face on, and paste me the link.

A website adds 1 line under it: `Record it in the browser's phone view: right-click the page, Inspect, then the phone icon.`

When the link comes, write `LOOM <url>` as the last line of `facts.md` (a new link replaces the old
line), then print:

> Next: /the-close.
