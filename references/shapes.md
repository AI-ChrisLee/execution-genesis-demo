# The 4 shapes

`## THE SHAPE` on `squad/business.md` picks 1 of these. Read that shape's section, plus The folder and
The Loom, which hold for every shape.

| THE SHAPE | The shape line to print | Connect | The build |
|---|---|---|---|
| website | You sell websites, so the demo is the owner's site, 1 page, built for the phone. | nothing | `index.html` |
| content | You sell content, so the demo is a small set of their posts, made in Higgsfield. | Higgsfield | `media/`, `posts.md`, `index.html` |
| consulting program | You sell a program, so the demo is the coach's program on a Notion board. | Notion | `board.md` and the board in the founder's Notion |
| software | You sell software, so the demo is the owner's tool, 3 screens you can click. | nothing | `index.html` |

No `## THE SHAPE` heading, or a word that is not 1 of the 4: read THE SENTENCE and pick by what the
founder makes. A site or a page: website. Posts, videos, images or ads: content. A program that takes
clients through stages, their own or one they set up for a coach: consulting program. A tool, an app,
an automation or an AI agent: software. Say the pick in the shape line.

---

## The folder, every shape

`squad/demos/<business>/`: the business name lowercased, `&` written as `and`, every character that is
not a letter, a digit or a space dropped, spaces as hyphens, and repeated hyphens collapsed to 1
(`Bright Smile Dental` gives `bright-smile-dental`, `Smith & Sons Plumbing, Inc.` gives
`smith-and-sons-plumbing-inc`). A person with no business name (a coach, a creator) uses their NAME
(`dana-cole`).

**`facts.md`**, written before anything is built:

```
# Facts · <business name> · <YYYY-MM-DD>

NAME · Bright Smile Dental · made up, founder · read 2026-09-17
FIRST NAME · Maria · made up, founder · read 2026-09-17
PHONE · (512) 555-0142 · https://brightsmile.example/contact · read 2026-09-17
RATING · 4.8 from 212 reviews · pasted by founder · read 2026-09-17

## Blank
YEARS OPEN
NEW PATIENT OFFER

LOOM https://www.loom.com/share/<id>
```

- 1 line per fact: `FIELD · value · source · read <date>`. Field names in capitals, from the shape's list below.
- **Sources, and only these:**
  - `made up, founder` on a made-up run.
  - On a real run, the URL the fact was read on, or `pasted by founder`.
  - `squad/business.md`, only for FIRST SCREEN, TASK and CHECK on software.
  - `counted from <fields>`, only on a `DERIVED` line: a count or a sum made from lines above it
    (`DERIVED · 5 dogs today, Lena 3, Sam 2 · counted from RECORD 1 to RECORD 5 · read 2026-09-17`).
  - `sample`, only on the sample records of a real software or program run, which show under a
    `Sample data` label.

  A value the agent picks itself (a date, a time, a count, a stage name) has no source, so it never
  goes on `facts.md` or on the page.
- Every field the shape asks for and nobody gave goes under `## Blank`, 1 per line. Nothing blank:
  `none` under the heading.
- The `LOOM` line is written only when the founder pastes the link, and it is always the last line.
  A new link replaces the old line.
- Every shape writes `FIRST NAME`: the first name of the person the message goes to (the owner, the
  coach, the creator), from the founder's message or the page. A person the page names with no role:
  their first name with `(role not given)` after the source, and the Loom opens with the business name.
  Nobody given: it goes under `## Blank`.
- TRADE is never asked. On a made-up run it comes from the founder's words (a dentist: `Dental
  practice`; a dog groomer: `dog grooming`), with the same source. On a real run it is the page's own
  words for what they do, with that URL. Every shape writes NAME, the business or person. A fact with
  no field on the shape's list gets its own name in capitals (`GROOMERS · Lena, Sam`).

**`notes.md`**, written with its header line at the same time as `facts.md`, before anything is built.
1 row per note round:

```
# Notes · <business name>

round · note · what changed · date
1 · "put same-day emergencies at the top, next to the phone" · the hero now leads with same-day emergencies · 2026-09-17
```

**THE PROBLEM and BUYER WORDS** on `squad/business.md` pick what the skeleton puts first: the thing
the buyer complains about, fixed and in plain sight on the first screen. They steer the build. They
are never shown as the buyer's facts. A program has no first screen: there THE PROBLEM picks 1 card
property (Consulting program, The problem property).

**A real run reads the page with curl.**
- Their own website: run `curl -sL --max-time 20 <link>`, strip the script and style blocks and the
  tags out of the HTML, and read the text that is left. When the home page links to an about, services
  or contact page on the same domain, read up to 3 of them the same way. Use WebFetch only when curl is
  missing or that text is empty. WebFetch returns a summary, so a line read through it is never quoted
  as their words. Every read empty: say so in 1 line, and every fact those pages were meant to give
  stays blank.
- A public Instagram profile: WebFetch gives the bio, the link and the follower count.
- Google Maps gives nothing back. Rating, review count and hours from Google come pasted by the
  founder, or stay blank.
- Only what the page says, word for word where it is their words. A fact the page does not carry is blank.

---

## Website

**Made up, the 1 message to print.** Before printing it, find the `trades.csv` row for WHO on
`squad/business.md` (`references/web-standard.md`, The lookup, step 1) and write its `Local Signals`
into item 5 in plain words.

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. Business name, the owner's first name, and town
> 2. 3 services, each with a price or "quote only"
> 3. Hours, phone, and where customers find the business: the street address, or the area the owner drives to
> 4. What the customer does: call, book, or ask for a quote
> 5. <the Local Signals of the trade's row, in plain words>, only the ones that are true
> 6. Proof, only if it's real: years open, review count, rating
>
> For a real business, send the name and the website or page link instead.

**Fields:** NAME, FIRST NAME, TOWN, TRADE, SERVICE 1, SERVICE 2, SERVICE 3 (each `name, price or quote
only`), HOURS, PHONE, ADDRESS or AREA (1 of the 2 is enough; both missing: `WHERE` goes under
`## Blank`), ACTION, YEARS OPEN, REVIEW COUNT, RATING, plus 1 field per Local Signal answered, named in
capitals (`INSURANCE`, `NEW PATIENT OFFER`, `PARKING`, `LANGUAGES`). A Local Signal not answered goes
under `## Blank`. Anything else the founder gives gets its own name (`NEAR · 2 minutes from Metrotown
SkyTrain`, `DENTIST · Dr. Anita Rao`, `KIDS · kids welcome`).

**Real, off their page:**

| Fact | Where it is read | Missing |
|---|---|---|
| Name, services, prices, phone, hours, address, area | their website | blank |
| Licenses, insurance, memberships, customer types | their website | blank |
| Result | only a line on their page that says what their customer gets | blank on most real runs; the hero falls back (`references/web-standard.md`, The hero) |
| Years open | as the page writes it (`since 1983`), never turned into a count of years | blank |
| Trade | the page's own words for what they do, with that URL | never blank on a real run |
| First name | a person the page names as the owner; a person named with no role gets `(role not given)` | blank |
| Their words, 3 phrases, word for word | their website or their Instagram bio | blank |
| Rating, review count | pasted by the founder off the Google listing | blank |
| Their logo | never drawn or generated | the name set in the display font |

Local Signals of the trade row that the page does not carry go under `## Blank`.

**Files:** `facts.md`, `notes.md`, `index.html`.

**The skeleton:** 1 `index.html` by `references/web-standard.md` (Website). Sections by its field map,
in the style row's order. What goes in each:
1. Hero: NAME, TOWN, the lead line, the money action and the visit card (`references/web-standard.md`,
   The hero). ACTION includes call: the call bar too.
2. Proof: every proof fact on `facts.md` (licenses, insurance or billing, memberships, years open,
   rating with its count, kids, languages), up to 6, as the proof cards. 1 proof fact joins the hero's
   second line instead. None: no strip. A person's name alone is never a proof item. A fact appears
   once above the footer.
3. Services: on a real run, every service the page lists, in its order, up to 6. On a made-up run, the
   3 given. Each carries its price, or `Quote only` when the founder said so. With neither, the row is
   the service name alone, with no link on the row. CUSTOMERS, when `facts.md` has it, sits under the
   heading in `var(--muted)`.
4. Any other section the style row names, only when `facts.md` fills it (`references/web-standard.md`,
   Sections).
5. The money section at the bottom, by ACTION (`references/web-standard.md`, The money action).
6. The footer.

Every trade word in NAME (a "Plumbing & Heating" shop has 2) gets at least 1 fact on the first 2 phone
screens when `facts.md` has one. A fact on `facts.md` that fits no section still goes on the page, in
the proof cards or the footer. Only a blank is left off. No image slot. Open the file in the browser.

**Tools:** none. **Cost line:** none. It costs nothing past the Claude plan.

---

## Content

**Connect: Higgsfield, through its command line tool.** A paid Higgsfield plan is required.
1. Run `higgsfield account status`. A plan other than `free` with more than 0 credits (`plus plan,
   1201.65 credits` counts): connected, go on. A `free` plan or 0 credits: print
   `Higgsfield needs a paid plan with credits to make the set.` and stop.
2. `command not found`: run `npm i -g @higgsfield/cli` yourself. `npm` not found: print
   `Install Node from nodejs.org, then type /the-demo again.` and stop.
3. Not signed in, or the tool was just installed: print
   `Type ! higgsfield auth login and sign in to Higgsfield in the browser window it opens. Then type /the-demo again.`
   and stop.

**Made up, the 1 message to print:**

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. Who it is, their first name, and the channel they post on
> 2. Where they film and what the light is like there, in plain words, and what they film on
> 3. 3 things their posts teach, each with the 1 point the post makes, in their words
> 4. What a viewer does next (DM a word, tap the link, or book) and what they get for it
> 5. 3 things they say, word for word
>
> For a real person, send the name and the profile link instead.

**Fields:** NAME, FIRST NAME, WHO, TRADE, CHANNEL, SETTING, LIGHT, FILMS ON, TOPIC 1, TOPIC 2, TOPIC 3
(each `topic, the point`), ACTION, ACTION GETS, WORDS 1, WORDS 2, WORDS 3.

**Real, off the page:** bio and link off the public profile. Captions of the last 3 posts when the page
gives them back, else pasted by the founder, else blank. The topics, their points and the setting, in
words taken from those posts. Their photos are never uploaded to Higgsfield.

**Files:** `facts.md`, `notes.md`, `posts.md`, `media/01`, `media/02`, `media/03` (each keeps the file
ending its URL has) and `media/01.jpg` to `media/03.jpg`, `media/clip-01` (the clip's first frame, also
its poster), `media/clip-01.mp4`, `index.html`.

**The skeleton:** 3 images and 1 clip, off `facts.md`. 01 is TOPIC 1, 02 is TOPIC 2, 03 is TOPIC 3. The
clip is the TOPIC closest to THE PROBLEM (none closer: TOPIC 1), at a different moment from its image.
- **The look, 2 lines written once** at the top of `posts.md` under `## The look`, before any prompt:
  PERSON (hair, top, bottoms, shoes, build, in `facts.md` words; nothing given, 1 plain line you write
  and never change) and PLACE (SETTING and LIGHT in `facts.md` words, plus the 3 largest things in the
  room and where each stands). Both lines go word for word into every prompt, the redos included, so
  all 4 pieces show 1 person in 1 place.
- Prompts, 30 to 130 words each. The subject first and where it stands in the frame (`left of centre`,
  `on the right third`), then the look, the framing, the light. Say what is in the frame, never what is
  not. The phone look in words: `shot on a phone, handheld, low contrast, slightly grainy`.
- Every object that carries a maker's label in real life is named plain and unmarked (`a plain grey
  opener box`, `plain black plates`).
- Never a phone, a hand holding a phone, or an app screen in the frame.
- No face, on every run. A person is seen side-on or from behind with the head out of the frame or
  turned away, or as hands only. Pick the angle the TOPIC is taught from: a movement side-on, shoulders
  down; a hands job, hands only. The frame centres on the work (the bar, the tool, the hands), never on
  the body from behind.
- No logo, no sign, no words in the frame.

**The cost, before any job:**
1. Each of the 3 image prompts:
   `higgsfield generate cost nano_banana_2 --prompt "<prompt>" --aspect_ratio 4:5` (prints `2 credits`).
   The clip's first frame: the same with `--aspect_ratio 9:16`. The clip prompt:
   `higgsfield generate cost kling3_0 --prompt "<prompt>" --aspect_ratio 9:16` (prints `8.75 credits`).
2. Add them up. More than the credits `account status` showed: say so in 1 line and stop.
3. **Cost line:** `This set costs <total> credits: 4 images at 2 each (1 is the clip's first frame), 1 clip at 8.75. Say yes and I make it.`
4. Wait for yes. No yes, no job.

**The make, after the yes:**
1. 01 first: `higgsfield generate create nano_banana_2 --prompt "<prompt>" --aspect_ratio 4:5 --wait`.
   Download it and look at it (`references/no-slop.md`, Generated images). A fail gets its redo, with
   its cost and a yes, before anything else is made.
2. Then 3 jobs at the same time, each with `--image media/01.<ending>` so the person and the room carry
   over: 02 and 03 at `4:5`, and the clip's first frame at `9:16`.
3. The clip: `higgsfield generate create kling3_0 --prompt "<prompt>" --aspect_ratio 9:16 --start-image media/clip-01.<ending> --wait --wait-timeout 20m`.
   A create that rejects `--start-image` runs again without it.
- Each job prints its result URL. Download each with
  `curl -L --create-dirs -o squad/demos/<business>/media/<name> "<url>"`.
- Each image goes on the page as a JPEG 1600px on its long side (Mac:
  `sips -Z 1600 -s format jpeg media/01.png --out media/01.jpg`). No resize tool: the downloaded file
  goes on the page.
- Look at every file before it goes on the page.

**`posts.md`:** `## The look` with the PERSON and PLACE lines, then 1 heading per piece (`## Clip`,
`## 01`, `## 02`, `## 03`) and its caption under it: the topic's point first, then 1 of their WORDS
where it fits, then the ACTION with what it gets, worded differently on each piece. SETTING, LIGHT and
FILMS ON steer the picture and never go in a caption. Length: a real run matches their last 3 captions;
a made-up run is 2 or 3 sentences. No hashtag wall. No emoji the facts did not show.

**`index.html`:** the feed, nothing else.
- At the top, a header: NAME in `var(--font-display)` at the pairing's h2 size, and under it 1 line in
  `var(--muted)`: WHO and CHANNEL in `facts.md` words. No handle, avatar, count or badge unless
  `facts.md` carries it.
- Then 1 column, 420px wide at most, centred: the clip first, then 01, 02, 03, as
  `<figure id="p1">` to `<figure id="p4">`. Each piece full width at its ratio: the images at 4:5, the
  clip at 9:16 as
  `<video src="media/clip-01.mp4" poster="media/clip-01.<ending>" preload="metadata" controls muted playsinline loop>`.
  A clip made without its first frame takes the still from the clip check, saved as `media/clip-01.png`.
  Its caption under each piece.
- From 720px: under the header, a row of the 4 pieces as 4:5 tiles (`object-fit: cover`, the clip
  tile shows its poster), each a link to its post, so the first laptop screen shows the name and the
  whole set at once.
- Colours and fonts from `references/web-standard.md` (The lookup, Tokens, Type), on TRADE. No platform
  chrome: no like counts, no follower counts, no badges, no logos. Open it in the browser.

**Tools:** the `higgsfield` command line tool, `curl`, `sips` on a Mac.

---

## Consulting program

**Connect: Notion.** Look for tools whose names end in `notion-create-database`, `notion-create-view` and
`notion-create-pages`, loaded or deferred. Deferred: load them, plus `notion-fetch`,
`notion-update-page`, `notion-update-view` and `notion-update-data-source`, in 1 tool search, and go on.
None of them: run `claude mcp add --transport http notion https://mcp.notion.com/mcp` yourself (`claude`
not found: print that line for the founder to paste into a terminal in this folder), then print:

> Quit Claude Code and open it again in this folder. Type /mcp, pick notion, and sign in to your Notion. Then type /the-demo again.

and stop.

**Made up, the 1 message to print.** Before printing it, read THE PROBLEM on `squad/business.md`. When
it is about something a coach tracks per client past the step and its date (the next call, a payment),
add it to the end of item 4 in plain words (`, and when each one's next call is`).

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. The coach's full name, the program name, who it's for, and how long it runs
> 2. The stages, in order: each one's name, what the client does, and what they walk out with
> 3. The result the program promises, in the coach's words
> 4. 1 or 2 client first names for every stage, and the date each one's current step is due
>
> For a real coach, send the name and the program page link instead.

**Fields:** NAME, FIRST NAME, PROGRAM, FOR, LENGTH, PROMISE. Per stage, 3 lines: `STAGE N NAME`,
`STAGE N DOES`, `STAGE N WALKS OUT WITH`. Per client: `CLIENT N` (`first name, stage`) and `DUE N`
(`first name, YYYY-MM-DD`), and the problem property when item 4 asked for it (`NEXT CALL N · first
name, YYYY-MM-DD`).

No stages given: ask for them in the 1 line. A coach's stages never come from the founder's page.

**Real, off their page:** program name, stages, length and promise off the sales page. Clients are never
real people: 1 card per stage, named `Sample client 1` and on, source `sample`, with no Due column and
no problem property.

**Files:** `facts.md`, `notes.md`, `board.md`. The board itself lives in the founder's Notion.

**The skeleton, 6 calls in this order:**
1. `notion-create-pages`: 1 page, `creation_mode` draft, title `<PROGRAM>`. Content, 2 lines off
   `facts.md`: `<NAME> · <FOR> · <LENGTH>`, then PROMISE word for word as a quote (`> <PROMISE>`). A
   blank field is left off its line.
2. `notion-create-database`: no parent, so the database never sits on the demo page as its own link.
   Title `<PROGRAM> clients`. Schema
   `CREATE TABLE ("Client" TITLE, "Stage" SELECT('<stage 1>':gray, '<stage 2>':blue, '<stage 3>':yellow, '<stage 4>':green), "This week" RICH_TEXT, "Due" DATE)`,
   1 option per stage, in order (more than 4 stages: the next colours are orange, purple, pink). The
   problem property, when there is one, joins the schema (`"Next call" DATE`). Leave out `"Due" DATE`
   unless every client has a DUE line on `facts.md`. Keep the data source ID it returns.
3. `notion-create-view`: `parent_page_id` the page from call 1, that `data_source_id`, type `board`,
   name `<PROGRAM>`, configure `GROUP BY "Stage"; SHOW "Client", <the problem property>, "This week", "Due"`
   (leave out any column call 2 left out).
4. `notion-create-pages`: parent the page from call 1, 1 page per stage, title `<N>. <STAGE N NAME>`.
   Content: `What you do`, with each thing in STAGE N DOES as an unchecked to-do (`- [ ] <thing>`), then
   `You walk out with: <STAGE N WALKS OUT WITH>`. A blank field's block is left off. Keep each page URL.
5. `notion-create-pages`: parent the data source, 1 card per client. Properties: Client; Stage; This
   week (that stage's DOES, whole, as written); Due (the client's DUE); the problem property. The card's
   page holds that stage's DOES as unchecked to-dos, the line `Walks out with: <WALKS OUT WITH>`, and a
   link to its stage page from call 4. Never repeat Stage, This week, Due or the problem property as
   text lines, because the properties already show them.
6. `notion-fetch` the page from call 1 and the view, then run The board in `references/no-slop.md`.

**The problem property:** THE PROBLEM picks the 1 card property that sits right under Client on the
card face, the one the problem is about. Stalled work: This week, which is already there. Missed or
forgotten calls: `Next call`. Late payment: `Paid`. It is added only when item 4 of the message asked
for it and every client has its line on `facts.md`.

**`board.md`:** the columns in order, each card with its properties and page text, the stage pages,
and the Notion link last.

**Show:** print the link to the page from call 1 and open it in the browser.

**Note rounds:** `notion-update-page` changes a card, a stage page, or the page's lines.
`notion-create-pages` adds a card or a stage page. `notion-update-view` changes the card face (SHOW),
the sort or the view name. `notion-update-data-source` adds, drops or renames a column. A missing column
is a stage with no card: ask for 1 client first name, then add the card. Nothing gets rebuilt that the
note did not name.

**Tools:** the Notion connector. **Cost line:** none.

---

## Software

THE SENTENCE picks 1 of 2 kinds. **The task tool:** a tool someone works in (a booking board, a job
list, an order screen). **The agent:** an AI agent that answers calls, messages or chats.

**The task tool, the 1 message to print:**

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. The business name and the owner's first name
> 2. Who opens it every morning, and the 1 job it does for them
> 3. 5 words they use for their own things (a grooming shop says "today's dogs")
> 4. What they see first, the 1 task they do in it, what goes wrong in that task today, and the money step (take a payment or a deposit)
> 5. 5 sample records, made up, each with the customer, what they want, who or what does it, and when it starts and ends. Make the 5th the one that goes wrong today
>
> For a real business, send the name and the website link instead.

**Fields:** NAME, FIRST NAME, USER, JOB, WORD 1 to WORD 5, FIRST SCREEN, TASK, CHECK, MONEY STEP,
RECORD 1 to RECORD 5 (each `customer, what, who or what does it, start, end`), TRADE.

**The agent, the 1 message to print:**

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. The business name, the owner's first name, and who reads what it did (the front desk's first name)
> 2. Hours, services with prices, and the rules it answers by (insurance taken, emergencies, deposits)
> 3. 5 calls or messages it handled: first name, when, what they wanted, what it booked or answered
>
> For a real business, send the name and the website link instead.

**Fields:** NAME, FIRST NAME, USER, HOURS, SERVICE 1 to SERVICE 3, RULE 1 to RULE 3, RECORD 1 to RECORD 5
(each `first name, when, what they wanted, what it did`), TRADE. FIRST NAME is the owner, the person who
pays. USER is the person who reads it; a person given with a role fills USER, with that role on the
source line. MONEY STEP is never asked for the agent and never goes under `## Blank`.

**Real, off their page:** service names, prices, hours and nouns off their website. The records are
samples: 5 of them, made-up first names, their services, times inside their HOURS, source `sample`,
under the `Sample data` label.

**Files:** `facts.md`, `notes.md`, `index.html`.

**The task tool skeleton:** 1 `index.html` by `references/web-standard.md` (Software), 3 screens, real
clicks between them, the task working inside the page:
1. **What they see first:** the records laid out the way the work runs, with 1 DERIVED line under the
   title. Records with a time and a person, room or vehicle make a day board: 1 column per person, room
   or vehicle, 1 row per time step the records use, each record a block from START to END, so a gap or
   an overlap shows at a glance. Other records make a table with status as its own column. The record
   that goes wrong (the last one) is not on the board: it waits in screen 2's form.
2. **The task, with THE PROBLEM stopped while the viewer watches.** The form opens filled with the
   record that goes wrong. The first press shows the check line (`references/web-standard.md`, The task
   script). Change 1 field and press again: the record joins screen 1, and screen 3 opens carrying it.
   The button is a verb plus a `facts.md` word, never a submit. CHECK blank: the form opens on the first
   choices, and the press adds the record.
3. **The money step** for the record screen 2 made (RECORD 1 until then). First the record in 1 block
   (who, what, with whom, when), then the amount as a labelled line (the amount on MONEY STEP, else that
   service's price; neither: no amount line), then the money button `disabled`
   with 1 line under it: `Not connected. Nothing is charged.` MONEY STEP blank: every record laid out
   the way the owner checks the day at its end, built only from the records, and no button. A screen
   that is only a heading and a button fails.

**The agent skeleton:** 1 `index.html` by `references/web-standard.md` (Software), 3 screens:
1. **The log:** 1 row per record (when, first name, what they wanted, the result), a DERIVED line under
   the title (`5 calls, 4 booked, 2 after hours`), and each row a link to its conversation.
2. **The conversations:** `s2` is the live one, and `s2-1` to `s2-5` are the records written out
   (`references/no-slop.md`, Conversations). The live one opens with a row of question buttons, 1 per
   HOURS, SERVICE and RULE line. A tap puts the customer's question and the agent's answer into the
   thread, the answer taken from that line of `facts.md` (`references/web-standard.md`, The agent
   script), and adds 1 row to the log: `Just now`, the question, `Answered`.
3. **What it booked:** every booked record by day and time, the way the front desk checks it. No money
   button.

**Words:** every screen title and nav link is a word from `facts.md`. Controls and labels may use this
fixed set and nothing past it: Open, Back, Sample data, Today, Yesterday, Just now, Booked, Paid, Sent,
Answered, Not connected, Name, Phone, Day, Time, Visit, Insurance, Reason, Status, Amount. A status word
goes only on a record whose `facts.md` line says it, or on a live row as `Answered`. When the agent does
TASK, screen 2's title is the record (`Jenny, 12:20 today`), never an order over a job already done.
Open the file in the browser.

**Tools:** none. **Cost line:** none. It costs nothing past the Claude plan.

---

## The Loom, every shape

The founder records it, not the agent. Under 2 minutes, face bubble on, over the open demo. Set the
link so anyone with the link can view it. Then the buyer needs no Loom account. The free Loom plan holds
25 videos of up to 5 minutes.

A website is recorded in the browser's phone view (Chrome: right-click the page, Inspect, the phone
icon, pick a phone). Software, the feed and the board are recorded in the full laptop window. On a real
website run, beat 1 shows their current site in the same phone view for about 10 seconds: what runs off
the side, and where the number is.

If the founder asks what to say, 3 beats:
1. Their name and the 1 thing you noticed about their business.
2. The demo on the screen, and the 1 thing their customer does in it (tap to call, book, hold a spot,
   ask the agent).
3. "Want to go through it on a call?"

A pasted link that is not a Loom share link: ask once for the share link.
