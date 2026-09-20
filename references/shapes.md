# The 4 shapes

`## THE SHAPE` on `squad/business.md` picks 1 of these. Read that shape's section, plus The folder,
Higgsfield (content and website) and The Loom, which hold for every shape.

| THE SHAPE | The shape line to print | Connect | The build |
|---|---|---|---|
| website | You sell websites, so the demo is the owner's site, 1 page, built for the phone, with photos made in Higgsfield. | Higgsfield | `photos.md`, `media/`, `index.html` |
| content | You sell content, so the demo is a small set of their posts, made in Higgsfield. | Higgsfield | `media/`, `posts.md`, `index.html` |
| consulting program | You sell a program, so the demo is the coach's dashboard in Notion: a client board and a guide board. | Notion | `board.md` and the dashboard in the founder's Notion |
| software | You sell software, so the demo is the owner's tool, 3 screens you can click. | nothing | `index.html` |

No `## THE SHAPE` heading, or a word that is not 1 of the 4: read THE SENTENCE and pick by what the
founder makes. A site or a page: website. Posts, videos, images or ads: content. A program that takes
clients through stages, their own or one they set up for a coach: consulting program. A tool, an app,
an automation or an AI agent: software. Say the pick in the shape line.

---

## The folder, every shape

`squad/demos/<business>/`: the business name lowercased, `&` written as `and`, every character that is
not a letter, a digit or a space dropped, spaces as hyphens, and repeated hyphens collapsed to 1
(`<Word> & <Word>, Inc.` gives `<word>-and-<word>-inc`). A person with no business name (a coach, a
creator) uses their NAME. A title before the name (Coach, Dr., Chef) stays in NAME and in the folder,
and FIRST NAME drops it.

**`facts.md`**, written before anything is built:

```
# Facts · <business name> · <YYYY-MM-DD>

NAME · <the business name> · made up, founder · read <YYYY-MM-DD>
FIRST NAME · <first name> · made up, founder · read <YYYY-MM-DD>
PHONE · <phone as written> · <the URL it was read on> · read <YYYY-MM-DD>
RATING · <rating> from <count> reviews · pasted by founder · read <YYYY-MM-DD>

## Blank
<FIELD>
<FIELD>

LOOM https://www.loom.com/share/<id>
```

- 1 line per fact: `FIELD · value · source · read <date>`. Field names in capitals, from the shape's list
  below. A fact with no field on the list gets its own name in capitals, for what it is.
- **Sources, and only these:**
  - `made up, founder` on a made-up run.
  - On a real run, the URL the fact was read on, or `pasted by founder`.
  - `squad/business.md`, only for JOB, TASK and CHECK on software.
  - `counted from <fields>`, only on a `DERIVED` line: a count or a sum made from lines above it
    (`DERIVED · <count> <their word for the records> today · counted from RECORD 1 to RECORD 8 · read <date>`).
  - `sample`, only on the sample records of a software or program run, real or made up, which show under
    a `Sample data` label.

  A value the agent picks itself (a date, a time, a count, a stage name) has no source, so it never goes
  on `facts.md` or on the page. The 1 exception is a sample record, made by the rules for it.
- Every field the shape asks for and nobody gave goes under `## Blank`, 1 per line. Nothing blank: `none`
  under the heading. A half-filled field puts its missing half there (`TOPIC 2 POINT`).
- The `LOOM` line is written only when the founder pastes the link, and it is always the last line.
  A new link replaces the old line.
- Every shape writes NAME and `FIRST NAME`: the first name of the person the message goes to (the owner,
  the coach, the creator), from the founder's message or the page. A person the page names with no role:
  their first name with `(role not given)` after the source, and the Loom opens with the business name.
  Nobody given: it goes under `## Blank`.
- TRADE is never asked, and a program does not write it. On a made-up run it comes from the founder's
  words, with the same source. On a real run it is the page's own words for what they do, with that URL.

**The blanks line**, printed at step 6: the fields under `## Blank` in plain words, never field names.
On a website or software run, the blanks that the trade row's `Watch Out` or the style's `Copy Angle`
needs come first (`Blank: <those blanks>, <the rest>.`). A program names who each blank is for
(`Blank: <what is missing> for <first names>.`). No blanks: no line.

**`notes.md`**, written with its header line at the same time as `facts.md`, before anything is built.
1 row per note round:

```
# Notes · <business name>

round · note · what changed · date
1 · "<the note, word for word>" · <what changed, in 1 line> · <YYYY-MM-DD>
```

**THE PROBLEM and BUYER WORDS** on `squad/business.md` pick what the skeleton puts first: the thing the
buyer complains about, fixed and in plain sight on the first screen. They steer the build. They are
never shown as the buyer's facts. A program has no first screen: there THE PROBLEM picks 1 card property
(Consulting program, The problem property).

**The template test**, printed at step 7:
- <their place> is TOWN, ADDRESS, NEAR, AREA or SETTING. On content, <name> is NAME in the header, and
  SETTING counts when every picture shows it, written as `<SETTING> (in the pictures)`.
- A program or a tool with no place: their NAME where it heads the page or the top bar, and <a fact of
  theirs> is the program name, a stage name, a staff name or a service.
- <their words> is a WORDS line on the page. On a program, PROMISE is their words. No words of theirs on
  the page: the third is another fact of theirs, without quote marks.

**A real run reads the page with curl.**
- Their own website: run `curl -sL --max-time 20 <link>`. Before stripping anything, read every
  `application/ld+json` block: `openingHours` or `openingHoursSpecification`, `telephone` and `address`
  found there count as their website (source: the URL followed by `(structured data)`).
  `aggregateRating` found there never counts: rating and review count come pasted by the founder. Then
  strip the script and style blocks and the tags, and read the text that is left. Nav and footer text
  count as their website, with the page URL as the source.
- Read up to 3 more pages on the same domain: the about page, the contact page, then the services page.
  With no single services page, read the service page for the service the lead fact names.
- Use WebFetch only when curl is missing or the text is empty. WebFetch returns a summary, so a line read
  through it is never quoted as their words. Every read empty: say so in 1 line, and every fact those
  pages were meant to give stays blank.
- A public Instagram profile: WebFetch gives the bio, the link and the follower count.
- Google Maps gives nothing back. Rating, review count and hours from Google come pasted by the founder,
  or stay blank.
- Only what the page says, word for word where it is their words. A fact the page does not carry is blank.
- When 2 pages state 1 claim at 2 strengths (`same day` in one place, `usually same day` in another),
  `facts.md` carries both lines, and the page uses the weaker one word for word.

---

## Higgsfield, for content and website

**Connect: Higgsfield, through its command line tool.** A paid Higgsfield plan is required.
1. Run `higgsfield account status`. A plan other than `free` with more than 0 credits (`plus plan,
   1201.65 credits` counts): connected, go on. A `free` plan or 0 credits: print
   `Higgsfield needs a paid plan with credits to make the pictures.` and stop.
2. `command not found`: run `npm i -g @higgsfield/cli` yourself. `npm` not found: print
   `Install Node from nodejs.org, then type /execution-genesis-demo again.` and stop.
3. Not signed in, or the tool was just installed: print
   `Type ! higgsfield auth login and sign in to Higgsfield in the browser window it opens. Then type /execution-genesis-demo again.`
   and stop.

**The look, written once** at the top of `posts.md` (content) or `photos.md` (website) under
`## The look`, before any prompt:
- PLACE: SETTING and LIGHT in `facts.md` words, plus the 3 largest things in the room and where each
  stands. No SETTING on a website: 1 plain line written from TRADE and the style's `Imagery Direction`,
  its place and its light only. A portrait, a face, a crew, a member or a uniform it names is dropped.
- PERSON, content only: hair, top, bottoms, shoes and build, in `facts.md` words. Nothing given: 1 plain
  line you write and never change. Clothes are loose, never fitted.
- Anything the agent adds to PLACE is plain furniture or plain equipment (a door, a bench, a shelf, a
  chair, a lamp), never something that says something about the business (a certificate, a sign, a
  product, a trophy, a second person).
- PERSON and PLACE direct the pictures. They are not facts: they stay off `facts.md` and never appear as
  words on the page. Both go word for word into every prompt, the redos included.

**Prompts:** 30 to 70 words for the subject, where it stands in the frame (`left of centre`, `on the
right third`), the framing and the moment. Then the PERSON and PLACE lines word for word, then the phone
line: `shot on a phone, handheld, low contrast, slightly grainy, real light`. The look lines and the
phone line do not count toward the 70.
- Say what is in the frame, never what is not.
- Every object that carries a maker's label in real life is named plain and unmarked (`a plain
  unmarked box`).
- Never a phone, a hand holding a phone, or an app screen in the frame. No logo, no sign, no words.

**People.** No face on the page, and never the body from behind, on every run.
- A website photo shows a person only as hands at work.
- A content piece with a person uses 1 of 2 framings. WHOLE: the person seen from the true side (the
  shoulder line points at the camera, the arm and leg nearest the lens in front), at the moment of the
  TOPIC when the head is highest, with the head in the top fifth of the frame, made at `9:16`. The page
  shows it in a 4:5 box anchored to the bottom, which cuts off the top 30% of the frame and the head with
  it. CLOSE: the work up close (hands on the tool, feet on the floor, the bar), the camera at the work's
  height, made at `4:5`.
- Never ask the model in words to crop at the shoulders or the knees. It ignores that.

**The cost, before any job:**
1. Each image prompt: `higgsfield generate cost nano_banana_2 --prompt "<prompt>" --aspect_ratio <its ratio>`
   (prints `2 credits`). A clip prompt:
   `higgsfield generate cost kling3_0 --prompt "<prompt>" --aspect_ratio 9:16` (prints `8.75 credits`).
2. Add them up, then add the redo allowance: 2 credits for every image and 8.75 for every clip,    which is 1 redo each. That total is the ONE number the founder says yes to. More than the    credits `account status` showed: say so in 1 line and stop.
3. Print the shape's cost line. Wait for yes. No yes, no job.

**The make, after the yes:**
1. The room first, with nobody in it: `media/place` (content) or `media/hero` (website).
   `higgsfield generate create nano_banana_2 --prompt "<the PLACE line, nobody in it, the phone line>" --aspect_ratio <9:16 content, 4:5 website> --wait`.
   Look at it (`references/no-slop.md`, Generated images). A fail gets its redo, with its cost and a
   yes, before anything else is made.
2. Then every other image at the same time, each with `--image media/<that room>.<ending>`, so the room
   carries over. The person carries over from the PERSON line. Never pass a piece with a person in it as
   `--image`, because the model copies its whole framing into every later piece.
3. A clip: `higgsfield generate create kling3_0 --prompt "<prompt>" --aspect_ratio 9:16 --start-image media/clip-01.<ending> --wait --wait-timeout 20m`.
   A create that rejects `--start-image` runs again without it.
- Each job prints its result URL. Download each with
  `curl -L --create-dirs -o squad/demos/<business>/media/<name> "<url>"`.
- Each image goes on the page as a JPEG 1600px on its long side (Mac:
  `sips -Z 1600 -s format jpeg media/<name>.png --out media/<name>.jpg`). No resize tool: the downloaded
  file goes on the page.
- Look at every file before it goes on the page. A fail follows the redo rule in `references/no-slop.md`.

---

## Website

**Made up, the 1 message to print.** Before printing it, find the `trades.csv` row for WHO on
`squad/business.md` and the first style of its `Style Shortlist` in `styles.csv`
(`references/web-standard.md`, The lookup, steps 1 and 2). Fill items 5 to 7 from them. An item with
nothing to write is left out, and the rest are numbered in order.

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. Business name, the owner's first name, and town
> 2. Up to 6 services, each with a price or "quote only", and who each is for
> 3. Hours, phone, and where customers find the business: the street address and parking, or the area the owner drives to
> 4. What the customer does: call, book, or ask for a quote
> 5. <the Local Signals of the trade's row, in plain words>, only the ones that are true
> 6. <1 plain question per customer objection the Watch Out names, asking what the business really does about it (fear: What do you do when a customer is nervous?; cost: What does a first visit cost, or is there a new-customer offer?)>
> 7. <1 line per section in the style's Section Order that items 1 to 6 do not fill (a practitioner: The people customers meet, each with their role; a first visit or process: What the first visit is like, in 2 to 4 steps; an FAQ: The 2 questions customers ask most, with your answers)>
> 8. Proof, only if it's real: years open, review count, rating
> 9. What the place or the work looks like, and its light, in plain words, for the photos
>
> For a real business, send the name and the website or page link instead.

**Must have:** 1 service, and PHONE or ACTION. Also ADDRESS when customers come to the business (a
clinic, a salon, a shop), and, when THE PROBLEM names a time the business is closed (night, weekend,
after hours), what a customer gets when they call then.

**Fields:** NAME, FIRST NAME, TOWN, TRADE, SERVICE 1 to SERVICE 6 (each `name, price or quote only, who
it is for`), HOURS, PHONE, ADDRESS, NEAR or AREA (any 1 of the 3 fills the visit card; all 3 missing:
`WHERE` goes under `## Blank`), PARKING, ACTION, PERSON N (`<name>, <role>`), STEP N, FAQ N (`question,
answer`), YEARS OPEN, REVIEW COUNT, RATING, SETTING, LIGHT, plus 1 field per Local Signal answered and 1
per objection answered, each named in capitals for what it is (`<SIGNAL>`, `FEAR`, `COST`).
- A Local Signal or an objection not answered goes under `## Blank`.
- A SERVICE N slot nobody filled is not a blank: it never goes under `## Blank` or on the blanks line.
  No service carries a price: `PRICES` goes under `## Blank`.
- SETTING and LIGHT are never blanks: without them, PLACE is written from TRADE (Higgsfield, The look).
- Anything else the founder gives gets its own name (`<WHAT IT IS> · <the founder's words>`).

**Real, off their page:**

| Fact | Where it is read | Missing |
|---|---|---|
| Name, services, prices, phone, hours, address, area | their website | blank |
| Licenses, insurance, memberships, customer types | their website | blank |
| What only they have: a named program, a guarantee, the owner's past employer or named training, a named local problem they fix, financing with the lender named | their website, the about page first | blank |
| Their FAQ: up to 4 question and answer pairs, word for word, as FAQ N | their website | no FAQ section |
| Staff: each name with the role the page gives, as PERSON N | their about or team page | blank |
| Result | only a line on their page that says what their customer gets | blank on most real runs |
| Years open | as the page writes it (`since <year>`), never turned into a count of years | blank |
| Trade | the page's own words for what they do, with that URL | never blank on a real run |
| First name | a person the page names as the owner; a person named with no role gets `(role not given)` | blank |
| A service's sentence | the home page's line for it, or the first sentence of its service page, as SERVICE N NOTE | the name alone |
| Their words, 3 phrases, word for word | their website or their Instagram bio | blank |
| Rating, review count | pasted by the founder off the Google listing | blank |
| Their logo | never drawn or generated | the name set in the display font |

A real run's `facts.md` is not finished until it holds every fact of these kinds that the pages it read
carry. Local Signals of the trade row that the page does not carry go under `## Blank`.

**Their site first, on a real run.** Before the skeleton, take 1 shot of their current home page at
375px (`references/web-standard.md`, The look, shot 1) and open it. A blank shot means their site refuses
the frame: shoot the URL itself at `--window-size=500,812` and read it as a 500px phone. Print 1 line:
`Their site on a phone: <what reads first>, the phone <where it is, and whether it is tappable>.` When
their site already does what THE PROBLEM says is broken, print:
`Their site already <does it>. The demo has to win on <the lead fact>, so say that in the Loom's beat 1.`
Then build.

**Files:** `facts.md`, `notes.md`, `photos.md`, `media/hero` and `media/service-1` to `media/service-3`
(each keeps the file ending its URL has) with their `.jpg`, `index.html`.

**The photos:** a hero and 1 per main service. The main services are the first 3 on `facts.md`, the
lead fact's service first when it is one.
- The hero: PLACE with nobody in it, wide, made at `4:5`, looking like what the trade row's
  `Buys This Result` sells (a calm room, a finished job).
- A main service: that service's work up close in PLACE, made at `4:3` with `--image media/hero.<ending>`.
  A person in it is hands only.
- `photos.md`: `## The look` with the PLACE line, then 1 heading per photo (`## hero`, `## service-1`)
  with its prompt, the redos included.
- A photo carries no caption and `alt=""`. No words on the page say whose room or work it is.

**Cost line:** `The photos cost <total> credits: <N> images at 2 each, 1 for the top of the page and 1 for each of <the main service names>, plus <N x 2> held back for redos. I will not ask again inside that. Say yes and I make them.`

**The skeleton:** 1 `index.html` by `references/web-standard.md` (Website). Sections by its field map,
in the style row's order. What goes in each:
1. Hero: the name line, the H1, the second line, the money action, the hero photo and the visit card
   (`references/web-standard.md`, The hero). ACTION includes call: the call bar too.
2. Proof: with 1 or 2 proof facts (licenses, insurance or billing, memberships, years open, rating with
   its count, a Local Signal that is a yes), they go on the hero's second line and there is no proof
   strip. With 3 or more, all go in the proof cards, up to 6, and the second line carries the next fact
   THE PROBLEM points at. A person's name is never a proof item, and neither is an AREA line. A fact
   appears once above the footer.
3. Services: on a real run, every service the page lists, in its order, up to 6. On a made-up run, the
   ones given. The main services are photo cards, and the rest are rows under them. Each carries its
   price, or `Quote only` when the founder said so, and under it in `var(--muted)` who it is for or its
   SERVICE N NOTE. With neither, the name alone. No link on a card or a row. CUSTOMERS, when `facts.md`
   has it, sits under the heading in `var(--muted)`.
4. About <NAME>: every fact on `facts.md` that fits no other section, in the style's practitioner or
   about place, else after Services. PERSON N lines first, as `<name>, <role>` word for word, then each
   other fact on its own line word for word, up to 6 lines. No portrait. With 1 line only there is no
   section: a person goes on the visit card under a label of their role, and any other fact joins the
   hero's second line. A person with no role on `facts.md` is never shown.
5. Any other section the style row names, only when `facts.md` fills it (`references/web-standard.md`,
   Sections).
6. The money section at the bottom, by ACTION (`references/web-standard.md`, The money action).
7. The footer.

Every trade word in NAME (a shop named for 2 trades has 2) gets at least 1 fact on the first 2 phone
screens when `facts.md` has one. Only blanks, FIRST NAME, TRADE, ACTION, SETTING, LIGHT and unused WORDS
lines are left off the page. A photo that was not made, or failed, leaves no slot: the page is laid out
as if it never existed. Open the file in the browser.

**Tools:** the `higgsfield` command line tool, `curl`, `sips` on a Mac.

---

## Content

**Connect:** Higgsfield, above.

**Made up, the 1 message to print:**

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. Who it is, their first name, and the channel they post on
> 2. Where they film and what the light is like there, in plain words, and what they film on
> 3. 3 things their posts teach, each with the 1 point the post makes, in their words
> 4. What a viewer does next (DM a word, tap the link, or book) and what they get for it
> 5. 3 things they say, word for word
>
> For a real person, send the name and the profile link instead.

**Must have:** SETTING, each TOPIC with its point, and what ACTION gets.

**Fields:** NAME, FIRST NAME, WHO, TRADE, CHANNEL, SETTING, LIGHT, FILMS ON, TOPIC 1, TOPIC 2, TOPIC 3
(each `topic, the point`; a point still missing after the 1 ask goes under `## Blank` as
`TOPIC N POINT`), ACTION, ACTION GETS, WORDS 1, WORDS 2, WORDS 3.

**Real, off the page:** bio and link off the public profile. Captions of the last 3 posts when the page
gives them back, else pasted by the founder, else blank. The topics, their points and the setting, in
words taken from those posts. Their photos are never uploaded to Higgsfield.

**Files:** `facts.md`, `notes.md`, `posts.md`, `media/place`, `media/01`, `media/02`, `media/03` (each
keeps the file ending its URL has) and `media/01.jpg` to `media/03.jpg`, `media/clip-01` (the clip's
first frame) and `media/clip-01.jpg` (its poster, 1600px on its long side), `media/clip-01.mp4`,
`index.html`.

**The skeleton:** 3 images and 1 clip, off `facts.md`. 01 is TOPIC 1, 02 is TOPIC 2, 03 is TOPIC 3. The
clip is the TOPIC closest to THE PROBLEM (none closer: TOPIC 1), at a different moment from its image.
The clip, 01, 02 and 03 go CLOSE, WHOLE, CLOSE, WHOLE (Higgsfield, People). A TOPIC that is a hands job
is always CLOSE. The clip's first frame is made at `9:16`, with the room like every other image and the
work below the middle of the frame, because the page's 4:5 box cuts its top.

**Cost line:** `This set costs <total> credits: 5 images at 2 each (1 is the empty room, 1 is the clip's first frame), 1 clip at 8.75, plus 18.75 held back for redos. I will not ask again inside that. Say yes and I make it.`

**`posts.md`:** `## The look` with the PERSON and PLACE lines, then 1 heading per piece (`## Clip`,
`## 01`, `## 02`, `## 03`) and its caption under it:
- The topic's point first, as a sentence in their words, never the TOPIC alone as a 2 to 4 word
  fragment. Then 1 of their WORDS that no other piece uses. Then the ACTION with what it gets, worded
  differently on each piece.
- A point still blank: the caption opens with that WORDS line instead.
- SETTING, LIGHT and FILMS ON steer the picture and never go in a caption.
- Length: a real run matches their last 3 captions; a made-up run is 2 or 3 sentences. No hashtag wall.
  No emoji the facts did not show.

**`index.html`:** the feed, nothing else.
- At the top, a header: NAME in `var(--font-display)` at the pairing's h2 size, and under it 1 line in
  `var(--muted)`: WHO and CHANNEL in `facts.md` words. No handle, avatar, count or badge unless
  `facts.md` carries it.
- Then `.feed`, 1 column 420px wide at most, centred: the clip first, then 01, 02, 03, as
  `<figure id="p1">` to `<figure id="p4">`, its caption under each piece. Every piece, the clip too, sits
  in a 4:5 box: `aspect-ratio: 4 / 5; object-fit: cover; object-position: 50% 100%; width: 100%`. The
  images are `<img src="media/01.jpg" alt="">`. The clip is
  `<video src="media/clip-01.mp4" poster="media/clip-01.jpg" autoplay muted loop playsinline preload="auto">`,
  with no `controls`: a feed plays on its own. A clip made without its first frame takes a still from
  the clip check as its poster.
- In each caption, the ACTION's word or link sits in `<b class="kw">` with `color: var(--accent)`.
- From 720px there is no second row of tiles. The feed itself becomes the grid inside `.wrap`:
  `.feed { max-width: none; display: grid; grid-template-columns: repeat(4, 1fr); gap: var(--s5); align-items: start; }`,
  each post with its caption. The first laptop screen shows the name and the whole set once, lined up
  with the header.
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

> Quit Claude Code and open it again in this folder. Type /mcp, pick notion, and sign in to your Notion. Then type /execution-genesis-demo again.

and stop.

**Made up, the 1 message to print.** Before printing it, read THE PROBLEM on `squad/business.md`. A
problem that names calls or meetings adds `, and each one's next call date` to the end of item 4. A
problem about payments adds `, and whether each one has paid`. Nothing else is added.

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. The coach's full name, the program name, who it's for, and how long it runs
> 2. The stages, in order: each one's name, 2 or 3 things the client does there (each starting with a verb, like "book 3 sales calls"), and what they walk out with
> 3. The result the program promises, in the coach's words
> 4. 2 client first names for every stage, which of that stage's things each one has already done, and the day each one's next thing is due
>
> For a real coach, send the name and the program page link instead.

**Must have:** PROGRAM, the stages with 2 or 3 things the client does in each, and 2 clients in every
stage with the day each one's next thing is due. A thing with no verb or a number with no noun is named
in the ask. No stages given: ask for them in the same line. A coach's stages never come from the
founder's page.

**Fields:** NAME, FIRST NAME, PROGRAM, FOR, LENGTH, PROMISE.
- Per stage, 3 lines: `STAGE N NAME`, `STAGE N DOES` (the founder's things split on commas, each as
  given), `STAGE N WALKS OUT WITH`.
- Per client: `CLIENT N` (`first name, stage`), `DONE N` (`first name, <the things done, as written in
  STAGE N DOES>` or `first name, none`), `DUE N` (`first name, YYYY-MM-DD`), and, only when item 4 asked,
  `NEXT CALL N` (`first name, YYYY-MM-DD`) or `PAID N` (`first name, yes or no`).
- The agent never adds a word to a thing. A thing with no verb (a bare noun) or a number with no noun
  goes into the 1-line ask by name. Dropping a word that only repeats the field (`<N>-week program`
  written as LENGTH `<N> weeks`) is allowed.

**Real, off their page:** program name, stages, length and promise off the sales page. Clients are never
real people: 4 cards per stage, made-up full names, source `sample`, with no problem property.

**Files:** `facts.md`, `notes.md`, `board.md`. The dashboard itself lives in the founder's Notion.

---

### What the dashboard is

TWO inline databases on 1 page, not a page of links. The worked example, built 2026-09-20 and the bar
for this shape:

1. **Clients** · a board grouped by Stage. 1 card per client, 4 per stage, every card a real-looking
   person with a page icon. This answers "where is everyone".
2. **The program** · a board grouped by Stage, sorted by Order. 5 or 6 guide cards per stage, so 20 to
   24 in all. Every card opens to why that step sits where it does, a checklist, and what done looks
   like. This answers "what do I actually do".

A flat list of 4 stage pages is NOT this shape. The stages are columns on the program board, and the
guides are the cards inside them.

### Icons, on every page

`icon` is a top-level parameter on `notion-create-pages` and `notion-update-page`, a sibling of
`properties`, never a property inside it. An emoji in the title text instead of the icon leaves the
grey default document sheet on the card and is wrong.
- Client cards: a person emoji, skin tones and genders varied across the roster (`👩🏾`, `👨🏽`, `👩🏼`,
  `👨🏿`). Never the same 1 twice in a row down a column.
- Guide cards: an emoji for the thing itself (`🪪` a licence, `📞` a call, `🔥` a warm lead, `🚫` a
  don't).
- The page itself: 1 emoji for the program.

### Client cards read like a coach's notes

This is what separates this shape from a template. `This week` is never the stage's generic line
repeated down the column. It says where THAT person is inside the stage, in the coach's voice:
- `31 of 50 called. 4 warm so far.`
- `Stuck on which CRM. Told him to pick 1 and stop looking.`
- `First offer rejected on price. Going again Thursday.`
- `Accepted. Inspection Monday, closing 4 weeks out.`

So the board shows progress INSIDE a column, not only which column. On a made-up run, vary it: some
starting, some most of the way, 1 stalled, 1 nearly done. On a real run it comes off DONE N and nothing
is invented.

Clients get full names (`Danielle Okafor`), never `Sample client 1`.

### The schema, verified

`notion-create-database` takes `{parent, title, schema}` and `schema` is a STRING in this syntax, NOT a
JSON object. Column names in double quotes, type keyword after a space, select options in single quotes:

```
("Client" title, "Stage" select('Setup', 'Sphere', 'Open houses', 'First deal'), "Next call" date, "This week" rich_text, "Walks out with" rich_text)
```

Type keywords are Notion's own: `title`, `rich_text` (not `text`), `date`, `number`, `select`,
`checkbox`. Option colours are NOT part of this string; set them after with
`notion-update-data-source`, and if the chips stay grey, leave them grey rather than retrying.

### The build

Calls 1 and 2 may run in 1 message.

1. `notion-create-pages`: 1 page, title `<PROGRAM>`, `icon` 1 emoji. Content: `<NAME> · <FOR> ·
   <LENGTH>`, then PROMISE word for word as a quote (`> <PROMISE>`). A blank field is left off its line.
2. `notion-create-database` twice, `parent` the page from call 1 both times. Keep both the database URL
   and the data source id each returns.
   - `Clients`, schema as above, with the problem property added when item 4 asked for it.
   - `The program`, schema
     `("Guide" title, "Stage" select(<the same stages>), "Week" rich_text, "Done when" rich_text, "Order" number)`
3. `notion-create-view` on each: `database_id` and `data_source_id` from call 2, type `board`, name
   `By stage`, `group_by` `Stage`. The program also gets `sorts`
   `[{"property": "Order", "direction": "ascending"}]` so its guides run in sequence inside a column.
4. `notion-create-pages` into the Clients data source: 1 card per client, each with an `icon`.
   Properties: Client (full name); Stage; This week (that person's real position, per above); Due; the
   problem property. Never repeat Stage, This week or Due as text in the body, the properties show them.
5. `notion-create-pages` into The program data source, in batches of 6, 1 per guide, each with an
   `icon`. Properties: Guide (the step, no emoji in the text); Stage; Week; Order 1 to 6; Done when (1
   sentence you could check). Content, in this order:
   - 1 short bold line on WHY this sits here, or what it costs to skip it
   - the checklist, `- [ ] <thing>` off STAGE N DOES
   - Every stage gets at least 1 card that is not a task: what this stage does NOT include, or what it
     feels like when it is going badly. That card is what makes it read as a coach and not a checklist.
6. `notion-update-page` on the page from call 1, `replace_content`, laying it out: the heading, the
   2 lines and the promise, `## 👥 Clients` with the Clients database embedded
   `<database url="<url>" inline="true" />`, `## 🗺️ The program` with the program database embedded the
   same way, then a small table of the stages against what each one walks out with.
7. `notion-fetch` the page, 1 client card and 1 guide card, then run The board in `references/no-slop.md`.

`allow_deleting_content` on `notion-update-page` does not serialise as a boolean through this tool. So
lay the page out in call 6 BEFORE anything is nested under it, or keep the child pages in `new_str`.

**The problem property:** THE PROBLEM picks which property sits right under Client on the card face.
Stalled work: This week. Calls or meetings: Next call. Payments: Paid, the only property added for the
problem. Picking This week from DONE N is a choice among `facts.md` lines, not a made-up value.

**`board.md`:** both boards, their columns in order, each card with its properties and page text, and the
Notion link last.

**Show:** print the link to the page from call 1 and open it in the browser.

**Note rounds:** `notion-update-page` changes a card or the page's lines. `notion-create-pages` adds a
card. `notion-update-view` changes the card face, the sort or the view name. `notion-update-data-source`
adds, drops or renames a column. Nothing gets rebuilt that the note did not name.

**Tools:** the Notion connector. **Cost line:** none.

---

## Software

THE SENTENCE picks 1 of 2 kinds. **The task tool:** a tool someone works in (a booking board, a job
list, an order screen). **The agent:** an AI agent that answers calls, messages or chats.

**The task tool, the 1 message to print:**

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. The business name and the owner's first name
> 2. Who opens it every morning, and the 1 job it does for them
> 3. 5 words they use for their own things (what they call today's work, a job that is finished, a person who does the work)
> 4. The hours they are open, the 1 task they do in it, what goes wrong in that task today, and the money step (take a payment or a deposit)
> 5. Up to 8 records, made up. Each has the customer's first name, the thing worked on when it is not the customer (the pet, the car), what they want, who does it, when it starts and ends, and a note on how to handle it when there is one. Make the last one the one that goes wrong today. Give me at least that one, and I fill the rest of the day with sample records.
>
> For a real business, send the name and the website link instead.

**Must have:** HOURS, and the record that goes wrong. JOB and TASK come from THE SENTENCE, and CHECK
(what goes wrong in the task) from THE PROBLEM, when the founder did not give them, source
`squad/business.md`. Fewer than 8 records: the agent adds sample records and never asks for more.

**Fields:** NAME, FIRST NAME, USER, JOB, WORD 1 to WORD 5, HOURS, TASK, CHECK, MONEY STEP, RECORD 1 to
RECORD 8 (each `customer, thing worked on or none, what, who or what does it, start, end, note or none`),
TRADE.

**The agent, the 1 message to print:**

> Who is this demo for? Make 1 up in 1 message with these facts, and skip any you don't have:
> 1. The business name, the owner's first name, and who reads what it did (the front desk's first name)
> 2. Hours, services each with a price or "quote only", and the rules it answers by (insurance taken, emergencies, deposits), said the way the front desk says them
> 3. Up to 6 calls or messages it handled: first name, when, what they wanted, what it booked or answered. Give me at least 1, and I fill the rest with sample calls.
>
> For a real business, send the name and the website link instead.

**Must have:** HOURS, and 1 call it handled. Fewer than 6 records: the agent adds sample records and
never asks for more.

**Fields:** NAME, FIRST NAME, USER, HOURS, SERVICE 1 to SERVICE 6 (each `name, price`, `name, quote
only` or the name alone), RULE 1 to RULE 3, RECORD 1 to RECORD 6 (each `first name, when, what they
wanted, what it did`), TRADE. FIRST NAME is the owner, the person who pays. USER is the person who reads
it; a person given with a role fills USER, with that role on the source line. A RULE the founder gave
about the office in the third person (`they take ...`) is written as the office says it (`We take ...`):
the person changes, nothing else. MONEY STEP is never asked for the agent and never goes under `## Blank`.

**Sample records.** A software run with fewer records than its count (the task tool 8, the agent 6)
adds sample records until it has that count. Each is written `RECORD N · <fields> · sample`, and the
page shows the `Sample data` tag.
- Made-up first names, and only the founder's services, people, rules and hours. No note on a sample.
- The task tool: the records spread evenly across the people, rooms or vehicles, morning and afternoon,
  inside HOURS. No 2 records overlap for 1 person. The record that goes wrong is placed so it overlaps
  exactly 1 record for its person and fits free for exactly 1 other person (1 person only: free at 1
  other time), so changing 1 field clears the check. On a made-up run it is never a sample. With no
  HOURS, the grid runs from the first START given to 6 hours after it, HOURS stays under `## Blank`, and
  no text on the page states the hours.
- The agent: times inside HOURS, with 1 outside HOURS when THE PROBLEM names missed or after-hours
  calls. What each one did comes from a SERVICE or a RULE line.

**Real, off their page:** service names, prices, hours and nouns off their website. Every record is a
sample.

**Files:** `facts.md`, `notes.md`, `index.html`.

**The task tool skeleton:** 1 `index.html` by `references/web-standard.md` (Software), 3 screens, real
clicks between them, the task working inside the page:
1. **What they see first:** the records laid out the way the work runs, with 1 DERIVED line under the
   title. Records with a time and a person, room or vehicle make the day board
   (`references/web-standard.md`, The day board). Other records make a table with status as its own
   column. A record's note shows on its block. The record that goes wrong (the last one) is not on the
   board: it waits in screen 2's form. Each block opens screen 3 with its record.
2. **The task, with THE PROBLEM stopped while the viewer watches.** The form opens filled with the
   record that goes wrong. The first press shows the check line (`references/web-standard.md`, The task
   script). Change 1 field and press again: the record joins screen 1, and screen 3 opens carrying it.
   The button is a verb plus a `facts.md` word, never a submit. CHECK blank: the form opens on the first
   choices, and the press adds the record.
3. **The money step, at the end of the job.** Its title is the founder's word for a finished job when a
   WORD is one, else MONEY STEP in `facts.md` words. At the top, the open record (the one screen 2 made,
   the block tapped on screen 1, else RECORD 1) in 1 block (who, what, with whom, when), then the amount
   as a labelled line (the amount on MONEY STEP, else that service's price; neither: no amount line),
   then the money button `disabled` with 1 line under it: `Not connected. Nothing is charged.` Under it,
   every record of the day by its END, each a row (name, END, amount when known) that opens itself at the
   top. MONEY STEP blank: the same list, the way the owner checks the day at its end, and no button.

**The agent skeleton:** 1 `index.html` by `references/web-standard.md` (Software), 3 screens:
1. **The log:** 1 row per record (when, first name, what they wanted, the result), a DERIVED line under
   the title counted from the records (`<N> calls, <N> booked, <N> after hours`), and each row a link to
   its conversation. The rows a tap adds sit in their own group above the log, under `Just now`, and the
   DERIVED line never counts them.
2. **The conversations:** `s2` is the live one, and `s2-1` to `s2-6` are the records written out
   (`references/no-slop.md`, Conversations). The live one opens with a row of question buttons, 1 per
   HOURS, SERVICE and RULE line. A tap puts the caller's question and the agent's answer into the thread,
   the answer taken from that line of `facts.md` (`references/web-standard.md`, The agent script), and
   adds 1 row to the `Just now` group: the question, `Answered`.
3. **What it booked:** every booked record by day and time, the way the front desk checks it. No money
   button.

**Words:** every screen title and nav link is a word from `facts.md` or from the fixed set below.
Controls and labels may use this fixed set and nothing past it: Open, Back, Sample data, Today, Yesterday, Just now, Live, Calls,
Messages, Booked, Paid, Not paid, Sent, Answered, Not connected, Caller, Name, Phone, Service, Who, Day,
Time, Visit, Insurance, Reason, Status, Amount. A status word goes only on a record whose `facts.md` line
says it, or on a live row as `Answered`. When the agent does TASK, screen 2's title is the record
(`<first name>, <when>`), never an order over a job already done. Open the file in the browser.

**Tools:** none. **Cost line:** none. It costs nothing past the Claude plan.

---

## The Loom, every shape

The founder records it, not the agent. Under 2 minutes, face bubble on, over the open demo. Set the
link so anyone with the link can view it. Then the buyer needs no Loom account. The free Loom plan holds
25 videos of up to 5 minutes.

A website is recorded in the browser's phone view (Chrome: right-click the page, Inspect, the phone
icon, pick a phone). Software, the feed and the board are recorded in the full laptop window. On a real
website run, beat 1 shows their current site in the same phone view for about 10 seconds: what runs off
the side, and where the number is. Before recording a board, turn Full width on (the ••• menu at the top
right of the page) and close the sidebar (Cmd+\ on a Mac, Ctrl+\ on Windows), so every stage column
shows and the clients database in the sidebar is out of the shot.

If the founder asks what to say, 3 beats:
1. Their name and the 1 thing you noticed about their business. On a real website run, use the line
   printed under Their site first.
2. The demo on the screen, and the 1 thing their customer does in it (tap to call, book, hold a spot,
   ask the agent). A board: open 1 card, tick its This week step, close it, and drag the card into the
   next column.
3. "Want to go through it on a call?"

A pasted link that is not a Loom share link: ask once for the share link.
