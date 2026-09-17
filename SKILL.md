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
- Never a real person's face, a logo, or readable text in a generated image. Never upload the buyer's photos.
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

Print the shape line for THE SHAPE, from the table in `references/shapes.md`. From here on, read that
shape's section, plus The folder and The Loom.

## 2. Connect first

Only when the shape needs it.

- **Content:** Higgsfield, by the 3 steps under Connect in the Content section of `references/shapes.md`.
  Those steps decide go on or stop.
- **Consulting program:** Notion. Tools ending in `notion-create-database`, `notion-create-view` and
  `notion-create-pages` exist in this session, loaded or deferred: go on. Deferred: load them, plus
  `notion-fetch`, `notion-update-page`, `notion-update-view` and `notion-update-data-source`, in 1 tool
  search. None of them: the steps under Connect in the Consulting program section, and this run stops.
- **Website and software:** nothing to connect. Skip this step without a word.

## 3. Who it is for

A business that already has a folder under `squad/demos/` holding the shape's build: open it and go to
step 6.

**`/the-demo` alone:** print the shape's 1 message (the question and its facts list, together) and
wait. Some messages carry a line filled in from `squad/business.md` first; the shape's section says
which. An answer that carries a link is a real run. An answer missing what the build cannot start
without, ask for those once, in 1 line, and wait:

- website: 1 service, and PHONE or ACTION
- content: SETTING and 1 TOPIC
- consulting program: PROGRAM, the stages with what the client does in each, and a client in every stage
- software: 3 RECORDS. FIRST SCREEN and TASK come from THE SENTENCE, and a task tool's CHECK (what goes
  wrong in the task) from THE PROBLEM, when the founder did not give them, source `squad/business.md`.

That same line also asks for FIRST NAME when it is blank, and on software for USER. Everything else
stays blank.

**`/the-demo <business>, <link>`:** a real run. Read the link by the rules under A real run in
`references/shapes.md`: `curl -sL` first, WebFetch only when curl gives nothing. A name with no link:
ask for the link once.

Then write `squad/demos/<business>/facts.md` and `notes.md` (The folder, in `references/shapes.md`):
1 line per fact with its source, every field nobody gave under `## Blank`. A blank never gets filled
with something that sounds nice.

## 4. The skeleton, right away

Build the shape's skeleton from `references/shapes.md` now. No plan, no pick, no question.
THE PROBLEM and BUYER WORDS decide what goes first.

- **Website:** 1 `index.html` by `references/web-standard.md` (Website).
- **Content:** write The look lines and the 5 prompts, get the cost of each, print the cost line for
  the whole set, and wait for yes. On yes, make the set in the order under The make, then write
  `posts.md` and `index.html`.
- **Consulting program:** the 6 Notion calls, in order, then `board.md`.
- **Software:** 1 `index.html` with 3 screens by `references/web-standard.md` (Software), the task or
  the conversation working inside the page.

## 5. The no-slop check

Before the founder sees anything, run the items `references/no-slop.md` gives this shape (What runs on
each shape). Website, software and the content feed also get The look (`references/web-standard.md`).
A program gets The board. Fix every fail and run the check again. Never show the demo with a note
about what is wrong.

## 6. Show it, 1 note at a time

Open the demo once: `index.html` in the browser (`open` on a Mac, `start` on Windows, `xdg-open` on
Linux), or print the Notion link and open it. On a real or a made-up run, list the fields under
`## Blank` in 1 line, and name first any blank the trade row's `Watch Out` needs
(`Blank: new patient offer, years open, rating.`). No blanks: no line. Then print:

> Give me 1 note: what would they notice first that's wrong?

Each note:

1. Change only what the note names. Nothing next to it gets rebuilt.
2. A note that needs a fact nobody gave: ask for that 1 fact, then add it to `facts.md` with its source.
3. Content: a redo prints its credit cost and waits for yes.
4. Run the no-slop check on what changed, with The look or The board.
5. Say what changed in 3 lines or fewer, then `Reload the tab.` The first show is the only `open`.
6. Add 1 row to `notes.md`: `round · note · what changed · date`.
7. Print the note line again.

Repeat until the founder says done.

## 7. Done

Print the template test, quoted from the demo:

> It names <name> in 3 places: <a fact of theirs>, <their place>, "<their words>".

<their place> is TOWN, ADDRESS, NEAR, AREA or SETTING. A program or a tool with no place: their NAME
where it heads the page or the top bar, and <a fact of theirs> is the program name, a stage name, a
staff name or a service. No words of theirs on `facts.md`: the third is another fact of theirs,
without quote marks. Anything on the demo that would read the same for the next business in the trade
gets fixed first, logged as a round in `notes.md`, and then the line is printed.

Then print:

> Record a Loom under 2 minutes over the open demo, face on, and paste me the link.

A website adds 1 line under it: `Record it in the browser's phone view: right-click the page, Inspect, then the phone icon.`

When the link comes, write `LOOM <url>` as the last line of `facts.md` (a new link replaces the old
line), then print:

> Next: /the-close.
