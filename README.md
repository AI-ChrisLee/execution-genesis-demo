# The MEP: install in 60 seconds

The part of an Execution Squad that builds the thing you put on the screen in the sales
hour. MEP stands for Minimum Executable Product: the shell of your offer, built for one
person you already talked to, real enough to show, built in 2 days. Not the product. The
surface of it, on the one problem they told you about, with their name on it.

## What to bring

Your offer document at `squad/business.md` (g5 wrote it, or a warm call drafted it in g4)
and one buyer folder under `squad/clients/` (warm-extract wrote it after your call). That
is the whole intake. No new accounts, no keys, no paid tools.

## Run it

Open Claude Code in your business folder and say: **"Build my shell."** Right after a call,
**"build that"** works too, and **"/mep [name]"** picks the person when you have talked to
more than one. (Downloaded this folder on its own? Drop the whole thing into
`.claude/skills/`, then quit and reopen Claude Code.)

It reads your offer and their words, and prints a one-screen plan: who, the one slice of
their problem in their own words, what the shell will show, what is not in it, and what
day one and day two look like. You say **go**, or point at a different slice. Then it
builds. When the file is done it prints one line, the 3 places the shell names your buyer,
and asks you to open it and name anything that would read the same for anyone else. Each
thing you name gets fixed. When you have nothing left to name, it is done.

Stopped halfway, or your usage window closed mid-build? Say **"continue the MEP"** in a new
window. It reads what is on disk and picks up at the first file missing.

## What it builds

One shape, decided by the business model in your offer document.

| Your model | The shell |
|---|---|
| Agency | One page in their name, on the design cage, as a file that opens in your browser. The first time, it asks you to install the design plugin with 2 lines, once. |
| Agency, content | One piece in their voice, for the channel they already use, written next to their current one. It asks you to paste that one first. |
| Consulting | A Notion database showing the structure, as a CSV you import into your own Notion in a minute, with the one line that goes above it. |
| Software | A clickable prototype, 3 screens, their data in the fields, one flow that ends on the money button. |

Everything lands in `squad/mep/<their-name>/` next to the plan.

## What it never does

It never deploys, never buys a domain, never wires a form, never generates an image, never
opens a new account, and never sends anything. The shell lives on your laptop. You
screen-share it in the sales hour, and the sale is the Close's job.

## What comes next

The part that turns your first 90 days into weekly tasks fitted to your hours. It arrives
one episode at a time. Subscribe (the link under every episode) and each new part lands in
your inbox the day its episode goes live.
