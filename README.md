# execution-genesis-demo

This agent is a base. Once you have done it your way, tell your squad "update the agent to do it like this."

Builds a working demo of your offer for 1 business, so your buyer sees the thing working before they
pay you. It reads your offer page, builds a first version right away, and changes it 1 note at a time.
No deck, no hosting, nothing made up, nothing sent.

**Install.** Installed with the one line on aichrislee.com/free. Then quit and reopen Claude Code once.

## Run

    /execution-genesis-demo

It asks who the demo is for. Make a business up, or point it at a real one:

    /execution-genesis-demo <the business>, <its website or page link>

It needs `squad/business.md` first. Run `/execution-genesis-offer` if you do not have it yet.

## What it makes, by what you sell

| You sell | The demo | You need |
|---|---|---|
| websites | the owner's site, 1 page, built for the phone, with photos made in Higgsfield | a paid Higgsfield plan |
| content | a small set of their posts and 1 clip | a paid Higgsfield plan |
| a consulting program | the coach's program on a Notion board | the Notion connector |
| software | the owner's tool, 3 screens you can click, with the task working | nothing |

Everything lands in `squad/demos/<business>/`. When you are happy with it, you record a Loom under 2
minutes over the open demo (the free Loom plan is enough) and paste the link back. That link is how
your buyer sees the demo. Next: `/execution-genesis-close`.

The 4 CSV files in `references/` come from Execution Design, MIT license, copyright 2024 Next Level
Builder and 2026 Nova9, Inc.

The full procedure is `SKILL.md`.
