# execution-genesis-demo

This agent is a base. Once you have done it your way, tell your squad "update the agent to do it like this."

Agent 2. It builds a working demo of your offer for 1 business, so your buyer sees the thing working
before they pay you. It reads your offer page, finds the winner in your buyer's trade and copies its
shape, builds a first version right away, and changes it 1 note at a time. No deck, no hosting,
nothing made up, nothing sent.

**Install.** Installed with the one line on aichrislee.com/free. Then quit and reopen Claude Code once.

## Run

    /execution-genesis-demo

It asks who the demo is for. Make a business up, or point it at a real one:

    /execution-genesis-demo <the business>, <its website or page link>

It needs `squad/business.md` first. Run `/execution-genesis-offer` if you do not have it yet.

## The winner

Before it builds, it picks 1 winner and copies its shape: the site the top seller on your offer page
shows as its work, or the top-reviewed business in your buyer's trade. It reads that page, looks at
it on a phone and a laptop, and writes `winner.md`: the first screen, where the money action sits,
where the proof sits, every section top to bottom. Your demo gets the same sections in the same order,
filled only with your buyer's own facts. A section the winner has and you have not given a fact for is
named first, so you can hand it over. Not 1 word, number or photo of the winner's goes on your demo.

## What it makes, by what you sell

| You sell | The demo | It copies | You need |
|---|---|---|---|
| websites | the owner's site, built for the phone, photos made in Higgsfield | the winner site's sections, first screen, proof and money action | a paid Higgsfield plan |
| content | a set of their posts and 1 clip | the top account's caption pattern: the first line's move, the length, the ask, the clip count | a paid Higgsfield plan |
| a consulting program | the coach's program on a Notion board | the winner program's stage count and what each stage promises | the Notion connector |
| software | the owner's tool, 3 screens you can click, with the task working | the winner product's first 3 screens by job | nothing |

Everything lands in `squad/demos/<business>/`: `facts.md` (every fact with its source), `winner.md`
(the shape it copied), `notes.md` (every round), and the build. When you are happy with it, you
record a Loom under 2 minutes over the open demo (the free Loom plan is enough) and paste the link
back. That link is how your buyer sees the demo. Next: `/execution-genesis-close`.

The 4 CSV files in `references/` come from Execution Design, MIT license, copyright 2024 Next Level
Builder and 2026 Nova9, Inc. They are the fallback when no winner can be read.

The full procedure is `SKILL.md`.
