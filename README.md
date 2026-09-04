# The MEP: install in 60 seconds

The part of an Execution Squad that builds the deck you put on the screen in the sales
hour. MEP stands for Minimum Executable Product: 9 slides for one person you already talked
to, that explain your offer and look like it already runs, built in 2 days. Not the product.
The deck that sells it, on the one problem they told you about, with their name on it. The
demo lives inside the deck, and its shape follows your business model.

## What to bring

Your offer document at `squad/business.md` (the Winning Offer wrote it, warm off your calls
in g4 or cold off the market in g5) and one buyer folder under `squad/clients/` (the warm
run wrote it after your call). That is the whole intake. No new accounts, no keys, no paid
tools.

Going after a stranger instead? Then all it needs is that company's row on
`squad/cold-list.md`. There are no quotes on that path, so everything it says about them is
labeled an observation, and anything the row does not carry stays blank.

## Run it

Open Claude Code in your business folder and say: **"Build my deck."** Right after a call,
**"build that"** works too, and **"/mep [name]"** picks the person when you have talked to
more than one. For a stranger on your outreach list, say **"build the deck for [company]
off my cold list."** (Downloaded this folder on its own? Drop the whole thing into
`.claude/skills/`, then quit and reopen Claude Code.)

It reads your offer and their words, and prints a one-screen plan: who, the one slice of
their problem in their own words, what the demo slides will show, the 9 slides one line
each, what is not in it, and what day one and day two look like. You say **go**, or point
at a different slice. Then it builds the demo, then the deck. When the deck is done it
prints one line, the 3 places it names your buyer, and asks you to open it and name
anything that would read the same for anyone else. Each thing you name gets fixed. When you
have nothing left to name, it is done.

Stopped halfway, or your usage window closed mid-build? Say **"continue the MEP"** in a new
window. It reads what is on disk and picks up at the first file missing.

## What it builds

One deck, 9 slides (8 when nothing they said gave you a cost, which is every deck built off
your cold list; `deck.md` says which slide was skipped), in `squad/mep/<their-name>/`:
`deck.html` opens by double-click, the arrow keys move it, and `deck.pdf` sits beside it
when your laptop has Chrome or Edge (if not, File, Print, Save as PDF does the same). The 3
demo slides change by the business model in your offer document.

| Your model | The demo slides |
|---|---|
| Agency | Their site, built for real by the design plugin and captured onto 3 slides. The first time, it asks you to install that plugin with 2 lines, once. |
| Agency, content | One piece in their voice, for the channel they already use, on a slide beside their current one. It asks you to paste that one first. |
| Consulting | The structure of the engagement: their columns, their facts as rows, one row lit. The CSV opens in any spreadsheet you already use. |
| Software | 3 screens drawn on 3 slides, their data in the fields, one flow that ends on the money button, disabled. |

## What it never does

It never deploys, never buys a domain, never wires a form, never generates an image, never
opens a new account, never puts your price on a slide, and never sends anything. The deck lives
on your laptop. You screen-share it in the sales hour, or send the PDF after, and the sale
is the Close's job.

## What comes next

The part that turns your first 90 days into weeks fitted to your hours. It arrives one
episode at a time. Subscribe (the link under every episode) and each new part lands in your
inbox the day its episode goes live.
