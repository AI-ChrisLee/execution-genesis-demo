# The web standard

The design rules 1 `index.html` follows, for the website and the software shapes. The content feed
takes The lookup, Tokens, Type, Colour, Layout and The look. The 4 CSV files sit next to this one.

## The lookup, no pick

1. `trades.csv`: the row whose `Trade` matches TRADE on `facts.md` (before `facts.md` exists, WHO on
   `squad/business.md`). No match: try once with a broader name. Still none: take the first row, in file
   order, of the kind closest to what the customer walks out with (a look: a salon row; a treatment: a
   clinic row; a job done at their home: a trade row; something to read or watch: a creator row). Take
   its `Style Shortlist`, `Buys This Result`, `Never Sell This`, `Local Signals` and `Watch Out`.
2. The first style named in `Style Shortlist`, found by its `Style` in `styles.csv`. Take its
   `Palette ID`, `Font Pairing ID`, `Radius`, `Section Order` and `Copy Angle`. A website also takes
   `Imagery Direction`, for its PLACE line only (`references/shapes.md`, Higgsfield, The look). Never read
   `Motion`: motion is set under Layout here. Software and the content feed take only `Palette ID`,
   `Font Pairing ID` and `Radius`.
3. `palettes.csv` by `Palette ID`: Surface, Raised, Ink, Muted, Accent, Text On Accent.
   `fonts.csv` by `Font Pairing ID`: `Google Fonts Import`, `CSS Variables`, `Heading Scale`,
   `Body Size`, `Notes`.
4. A real website run reads their brand colour off their home page: a `theme-color` meta tag, else the
   most used colour on its buttons in the CSS that is not a grey. When a `palettes.csv` row with the same
   `Mode` as the style's palette has its Accent in the same colour family (green, blue, red, orange,
   yellow, purple or brown), take that row instead of the style's Palette ID, and say so in 1 line. No
   match: the style's Palette ID.

5. `squad/demos/<business>/winner.md` (`references/the-winner.md`) wins over steps 2 to 4 for the
   section order and the section count, gives the palette row when the buyer's own site gave no brand
   colour (its accent, by the same colour-family rule), and gives the font pairing when its families
   match a `fonts.csv` row. Say in 1 line what came from the winner.

Copy the values out of the files. Never type a hex or a font name from memory. No 3 directions, no
question to the founder.

When the trade row's `Watch Out` or the style's `Copy Angle` names a place on the page (pinned, header,
every screen size, first screen), that place is built into the skeleton. It is never left for a note
round. The phone is the 1 exception: it always goes where The call bar puts it.

## The file

- 1 file. 1 `<style>` block, the pairing's import line at its top. No framework, no build step, no file
  past the font import and the pictures in `media/`. A website has no script. Software has the scripts
  under Software.
- `<meta name="viewport" content="width=device-width, initial-scale=1">`. `<title>` is the business name.
- The words on the page are in the language of `facts.md`.

## Tokens

```css
<Google Fonts Import, the whole line exactly as the CSV cell holds it>

:root {
  --surface: <Surface>; --raised: <Raised>; --ink: <Ink>;
  --muted: <Muted>; --accent: <Accent>; --on-accent: <Text On Accent>;
  <CSS Variables>
  --s2: .5rem; --s3: .75rem; --s4: 1rem; --s5: 1.5rem; --s6: 2rem; --s7: 3rem; --s8: 4rem;
  --radius: <Radius>;
  --line: 1px solid color-mix(in srgb, var(--ink) 12%, transparent);
}
.wrap { max-width: 72rem; margin: 0 auto; padding: 0 var(--s4); }
```

Every colour below `:root` is a variable. A raw colour value anywhere else fails.

## Type

- `body`: `var(--font-body)`, the pairing's `Body Size` (16px at the least), its line height,
  `color: var(--ink)`, `background: var(--surface)`, `margin: 0`.
- Website headings: `var(--font-display)`. Each `Heading Scale` entry `h1 clamp(a, b, c)/n` becomes
  `h1 { font-size: clamp(a, b, c); line-height: n; }`. Any extra words in the entry (a weight, a
  tracking) become their own properties. `h1, h2 { text-wrap: balance; }`.
- Apply the pairing's `Notes` wherever the display font is used: an optical size note becomes
  `font-variation-settings: 'opsz' <n>`, a case or tracking note becomes `text-transform` or
  `letter-spacing`, and a smallest size (`never under 28px`) holds everywhere. A size the Notes give the
  phone number applies to the call bar button only.
- Prices, phone numbers, times and counts: `font-variant-numeric: tabular-nums`.
- Paragraphs `max-width: 68ch`.
- Software type is under Software, and it wins over the body line above.

## Colour

- 6 values: the 5 palette colours and Text On Accent. Nothing else.
- The accent, on a website: the money button, a text link inside a sentence, the focus ring. On
  software: the task button or the agent's question buttons, and the focus ring. On the content feed:
  the ACTION's word in each caption, and the focus ring.
- Borders use `var(--line)`. No shadows. No gradient anywhere.

## Layout, 375px first

- The base CSS is the phone layout. Wider screens change it only inside `@media (min-width: 720px)`.
- Side padding `var(--s4)`. Section padding `var(--s7)` on phones, `var(--s8)` wider. Sections are split
  by space, not a border on every section. On a website, the money section alone sits on a full-width
  `var(--raised)` band, its content inside `.wrap`.
- On phones, no fixed width over 343px. Blocks are `width: 100%` with a `max-width`.
- From 720px the page is laid out for a laptop, not stretched from the phone. Website: the hero by
  The hero below. The service cards run in a row under their heading. The service rows, the About lines
  and the form each sit in 2 columns next to their heading (`grid-template-columns: 1fr 1.4fr`). No
  block spans the full `.wrap` width with nothing in it, and no column of 343px stands alone with empty
  space to its right.
- Every button and link a thumb uses is 44px tall at the least.
- The money button: `var(--accent)` fill, `var(--on-accent)` text, 52px tall, 24px side padding,
  `var(--radius)`, weight 600. Hover: `background: var(--ink); color: var(--surface)`.
- A disabled button reads as switched off, not faded: `background: var(--raised); color: var(--muted);
  border: var(--line); cursor: not-allowed`. Never `opacity`.
- A phone number never breaks across lines, in a button or in a sentence (`.phone { white-space: nowrap; }`).
- Inputs and selects: 52px tall, 16px text, `1px solid var(--muted)`, a visible focus ring in
  `var(--accent)`. Every field has a visible `<label>`. No `placeholder` attribute.
- Motion: a colour change on hover, 150ms, and nothing else. The clip playing on its own in the content
  feed is the post itself, not motion.
- A picture: `display: block; width: 100%; object-fit: cover; border-radius: var(--radius)`, with its
  `aspect-ratio` set in the CSS so the page never jumps while it loads.

## Website

- **Sections:** `winner.md` gives the order and the count (`references/the-winner.md`, The copy); the
  style row's `Section Order` only when there is no `winner.md`. Each section is filled only from these
  fields, and a section whose fields are all blank is dropped and named on the blanks line: hero = NAME, TOWN, the lead fact, PHONE,
  ACTION, the hero photo · trust, proof or credentials strip = YEARS OPEN, RATING with REVIEW COUNT,
  licenses, memberships, INSURANCE or BILLING, a Local Signal that is a yes · services, treatments, menu
  or packages = SERVICE lines · how fast = a response time or same-day fact the founder gave ·
  practitioner, coaches, stylists or about = the About section (`references/shapes.md`, Website, The
  skeleton) · first visit, process or how it works = STEP lines · reviews = reviews pasted with a source
  · area or location = ADDRESS, NEAR, AREA, PARKING, which live in the visit card · money section =
  ACTION · FAQ = FAQ lines · footer = NAME, PHONE, HOURS, ADDRESS or NEAR or AREA. A section this map
  does not name (the work, before and after, a gallery, the team) that `winner.md` has gets a plain 1
  to 3 word heading and the `facts.md` fields that fit it (`references/the-winner.md`, The copy); with
  none, it is dropped and goes first on the blanks line. The money section is the last
  section before the footer; an FAQ in the row moves above it.
- **A section that would hold 1 item under its heading is not its own section.** A person with a role
  goes on the visit card under a label of that role. 1 service joins the hero's second line. A single
  step or a single FAQ is dropped. A person with no role on `facts.md` is never shown.
- **The hero:**
  - **The lead fact** is the first of these that `facts.md` holds:
    1. RESULT.
    2. A fact only this business can say, one that passes the shop down the street test as written: a
       named program, a named specialty with its named training or brand, the owner's named past
       employer, a named guarantee, or a named local problem they fix.
    3. The fact THE PROBLEM points at, when THE PROBLEM is about their customers.
    4. Speed, price, hours or place, picked by the trade row's `Buys This Result`.

    When THE PROBLEM is about the site itself (hard to use on a phone, slow, no booking), it never picks
    the lead, because the call bar, the 375px layout and the money section already answer it. A fact that
    loses the lead keeps its own section, so a response time goes to How fast.
  - `Copy Angle` and `Watch Out` are read as a list of objections to answer with facts. An objection
    `facts.md` cannot answer stays unanswered, and its missing fact goes first on the blanks line.
  - BUYER WORDS from `squad/business.md` never go on the page. WORDS lines on `facts.md` may, but only
    where this file names them: the H1 and the money section's heading.
  - In order:
    1. A small name line: NAME in the display font, TOWN in `var(--muted)`. From 720px, when the call bar
       header carries the name, only TOWN stays on this line.
    2. The H1, 12 words at most, the lead fact in `facts.md` words: RESULT when it is that fact; else a
       WORDS line that carries it and passes the shop down the street test; else the fact said plainly
       (a service with its price, the hours, the place). When that plain fact is one any shop in the trade
       could say, join 1 place fact after a comma, word for word: `<lead fact>, <NEAR, else TOWN, else
       AREA>`, 12 words at most. The name line then drops that place fact.
    3. A second line, 20 words at most, with up to 2 more facts.
    4. The money action (below).
    5. The hero photo, when it was made.
    6. The visit card.

```html
<section class="hero"><div class="wrap hero-grid">
  <div class="hero-words"><!-- the name line, the H1, the second line, the money action --></div>
  <img class="hero-photo" src="media/hero.jpg" alt="">
  <aside class="card" aria-label="Visit"><!-- The visit card --></aside>
</div></section>
```

```css
.hero-grid { display: grid; gap: var(--s5); }
.hero-photo { aspect-ratio: 4 / 3; }
@media (min-width: 720px) {
  .hero-grid { grid-template-columns: 1.15fr 1fr; column-gap: var(--s7); align-items: start;
    grid-template-areas: "words photo" "card photo"; }
  .hero-words { grid-area: words; } .hero .card { grid-area: card; }
  .hero-photo { grid-area: photo; aspect-ratio: 4 / 5; }
}
```

With no hero photo, the `<img>` is left out and from 720px the grid is
`grid-template-areas: "words card"; align-items: center`, the card right of the words.

- **The call bar** (ACTION includes call): 1 `<header class="callbar">` as the first element in `<body>`,
  holding the name and the money button, which reads `Call <PHONE as written on facts.md>` and is the
  working `tel:` link. Below 720px it is fixed to the bottom of the screen with the button full width;
  from 720px it is a header pinned to the top, the name left and the button right. This placement wins
  over any Copy Angle or Watch Out that puts the phone somewhere else. On phones, the hero's `tel:` link
  on the first screen and the pinned bottom bar satisfy a phone "in the header at every screen size".

```html
<header class="callbar"><div class="wrap"><span class="name">NAME</span><a class="money phone" href="tel:<digits>">Call <PHONE></a></div></header>
```

```css
.callbar { position: fixed; left: 0; right: 0; bottom: 0; z-index: 10; padding: var(--s3) 0;
  background: var(--surface); border-top: var(--line); }
.callbar .name { display: none; }
.callbar .money { display: flex; justify-content: center; align-items: center; box-sizing: border-box; width: 100%; }
body { padding-bottom: 5.5rem; }
@media (min-width: 720px) {
  .callbar { position: sticky; top: 0; bottom: auto; border-top: 0; border-bottom: var(--line); }
  .callbar .wrap { display: flex; justify-content: space-between; align-items: center; }
  .callbar .name { display: block; font-family: var(--font-display); font-size: 1.75rem; }
  .callbar .money { width: auto; }
  body { padding-bottom: 0; }
}
```

- **The money action:**
  - **Call in ACTION:** the call bar carries the accent button. The hero has no second accent button: its
    phone is the number as a large `tel:` link in `var(--ink)` (weight 600, 1.5rem, `.phone`), with the
    after-hours fact under it when `facts.md` has one. The money section repeats the same `Call <PHONE>`
    button, with HOURS under it, and above it the strongest WORDS line that passes the shop down the
    street test, in the display font. No WORDS line passes: the call part gets no heading of its own.
  - **Book or quote in ACTION:** the money section holds the form, `id="book"`, `action=""`, with real
    controls: a `<select>` of the service names on `facts.md`, led, word for word, by the hero's lead fact
    when it is a kind of visit or job (an emergency or same-day slot); a `<select>` of the days HOURS
    names (a range such as Mon-Fri is written out as 1 option per day, which is not a new fact; no HOURS:
    no day field); Name; Phone. Typing and picking work. Only its button is `disabled`, in the disabled
    look, and it reads ACTION's booking words (`Book online`). Under it, 1 line:
    `Online booking connects on the live site. Until then, call <phone>.`, the phone as plain text in
    `<span class="phone">` (no phone: `Online booking connects on the live site.`).
  - **Both:** the money section gets 1 heading in ACTION's words over the call and the form (`Book or
    call`), then the call button with HOURS under it, then the form with no second heading. A heading
    never repeats the first word of the button under it. The hero puts a text link in ACTION's words to
    `#book` under its phone.
  - **Book or quote with no call:** no call bar. The hero's money button is the accent button, and it goes
    to `#book`.
  - The money button says the same words everywhere it appears.
- **The visit card**, in the hero: the facts a customer needs to come in or to call, laid out as a
  finished object. No grey box, no `Photo here`, no slot. It holds 2 to 4 labelled rows, taken from what
  `facts.md` holds in this order until it has 4: Hours; Where (ADDRESS as a link to the map, else NEAR,
  with PARKING on its own line under it); Area (AREA word for word); How fast (a response time the hero
  does not lead with); a person, under a label of their role, when the About section has 1 line only;
  Phone (an ink `tel:` link, only when there is no call bar). A fact in the card is not repeated above
  the footer. With fewer than 2 rows there is no card, and its 1 row joins the hero's second line.

```html
<aside class="card" aria-label="Visit">
  <p class="card-label">Hours</p>
  <dl class="days"><!-- 1 dt and dd per day or day range HOURS names, in its words --></dl>
  <p class="card-label">Where</p>
  <p><!-- ADDRESS as a map link, else NEAR; PARKING on its own line under it --></p>
</aside>
```

```css
.card { background: var(--raised); border: var(--line); border-radius: var(--radius); padding: var(--s5);
  display: grid; gap: var(--s3); align-content: start; }
.card-label { margin: 0; font: 600 .8125rem/1.2 var(--font-body); letter-spacing: .06em;
  text-transform: uppercase; color: var(--muted); }
.days { display: grid; grid-template-columns: auto 1fr; gap: var(--s2) var(--s4); margin: 0; }
.days dd { margin: 0; }
.card a { display: inline-flex; align-items: center; min-height: 44px; color: var(--ink); }
```

ADDRESS links to `https://www.google.com/maps/search/?api=1&query=<the address, URL-encoded>`. Only rows
`facts.md` carries go in, and never a Closed row the founder did not say.

- **The services:** the heading, then the main services as photo cards, then the rest as rows.

```html
<div class="svc-cards">
  <article class="svc"><img src="media/service-1.jpg" alt=""><h3>SERVICE NAME</h3><p class="price">PRICE or Quote only</p><p class="for">WHO IT IS FOR or SERVICE N NOTE</p></article>
</div>
<dl class="svc-rows"><!-- the rest: 1 dt (the name, its note under it in var(--muted)) and 1 dd (the price) each --></dl>
```

```css
.svc-cards { display: grid; gap: var(--s5); }
.svc img { aspect-ratio: 4 / 3; margin-bottom: var(--s3); }
.svc h3, .svc p { margin: 0 0 var(--s2); } .svc .for { color: var(--muted); }
.svc-rows > div { display: flex; justify-content: space-between; gap: var(--s4); padding: var(--s3) 0; border-top: var(--line); }
@media (min-width: 720px) { .svc-cards { grid-template-columns: repeat(3, 1fr); } }
```

2 cards take `repeat(2, 1fr)`. With no photos, every service is a row. Rows wrap each `dt` and `dd` pair
in a `<div>`.

- **The proof cards:** the proof facts, each a card on `var(--raised)` with `var(--radius)` and
  `padding: var(--s4)`. 2 columns on phones (an odd count: the first card spans both). From 720px: 3
  columns for 3 or 6 cards; 3 columns for 5 cards, with the first card spanning 2; 2 columns for 2 or 4
  cards. No grid leaves an empty cell. In each card, the number with its 1 joining word (`Since <year>`,
  `# <license>`, `<rating>`) is in the display font at its heaviest imported weight and the h2 size, and
  the rest of that same fact sits with it in `var(--muted)`. The words keep their reading order: words
  that come before the number on `facts.md` sit above it, and words that come after it sit under it. Both
  are word for word off `facts.md`, split only where the number meets the words. A fact with no number is
  1 line in the display font at the h3 size. A fact that lists 3 or more names is never a card.
- **The About section:** the heading `About <NAME>`, then 1 line per fact, PERSON lines first as
  `<name>, <role>`. No portrait, no photo.
- **The footer:** name, phone, hours, and where (ADDRESS, NEAR or AREA) off `facts.md`. Nothing else.
  From 720px it is 1 row:
  `footer .wrap { display: grid; grid-template-columns: 1.15fr repeat(3, auto); gap: var(--s6); align-items: baseline; }`.

## Software

- The palette, the fonts and the radius come from the lookup on their trade (the shop, not software).
  Section Order, Copy Angle and Heading Scale are skipped.
- **It reads as a tool, not a page.** A top bar on every screen: NAME in `var(--font-display)` at
  1.75rem (the pairing's `Notes` still hold), and at its right a `Sample data` tag in `var(--muted)` at
  .875rem, with a `var(--line)` border and `var(--radius)`. The tag shows when any record is a sample.
  Never an eyebrow over a heading.
- **Type for a tool:** body `1rem/1.5`. Screen titles, column heads, record names and buttons in
  `var(--font-body)` at weight 600, or the nearest weight its import line carries. Screen title 1.5rem,
  section title 1.125rem, meta .875rem, never under 14px. The display font goes only on the name in the
  top bar.
- **The nav:** 3 links in `facts.md` words or the fixed label set (`references/shapes.md`, Software,
  Words). Phones: a bar of 3 equal tabs, 44px tall, under the top bar. From 720px: a left column 220px
  wide beside the screen, the whole page up to 1200px wide, with the top bar, the nav and the screen on 1
  left edge. The current tab: `background: var(--ink); color: var(--surface)`.
- **Screens:** `<section data-screen="s1">`, `<section data-screen="s2">`, `<section data-screen="s3">`
  inside `<main>`, with no `id` on them, so the browser never jumps the top bar off screen. The agent's
  written-out records add `s2-1` to `s2-6`. The CSS carries `main > section[hidden] { display: none; }`.
  Every link opens a screen, no `href="#"`, and every record row that looks like a link opens its screen.
- **The day board:** `display: grid`, a first column of times, then 1 column per person, room or
  vehicle. Each column head carries the person and their count (`<name> <count>`). There is 1 grid row
  per 30 minutes (per 15 when a START or END falls between) from HOURS open to close, every row the same
  height (`grid-auto-rows: minmax(1.75rem, 1fr)`). Every hour row gets a `var(--line)` top border across
  all columns, and only the hour rows get a time label. These labels are the clock, not facts. Each
  record is a block (`grid-row: <start> / <end>`) on `var(--raised)` with `var(--line)` and
  `var(--radius)`. The thing worked on comes first, then the customer's first name in `var(--muted)`. A
  block 1 row tall shows the name and the service on 1 line. A taller block adds its note, status and
  time. Each block is an `<a href="#s3">` that fills screen 3 with its record. On phones, up to 2 columns
  sit side by side, and more stack 1 under the other. At 1280x800, screen 1 shows the whole day without
  scrolling.
- **Screen 2 on a laptop is 2 columns** (from 720px, `grid-template-columns: minmax(0, 36rem) 1fr; gap:
  var(--s6)`). The form goes on the left. On the right goes the chosen person's column from screen 1,
  with the same grid and blocks. The form's record is drawn in a second lane beside that column, as a
  block on `var(--surface)` with a `2px solid var(--ink)` border, redrawn on every choice. An overlap then
  shows as 2 blocks side by side before the press.
- **Screen 3 on a laptop is 2 columns:** the open record with its amount and money button on the left,
  the day's list on the right.
- **Status and note:** a status (where the record is today) is a label, weight 600, with a `var(--line)`
  border and `var(--radius)`, right-aligned where it fits and under the name where it does not. A note
  (how to handle it) is plain text under the name. They never share a style.
- **Choices, never blank pickers:** day, time, person and service on a form are 44px buttons with
  `aria-pressed`, or a `<select>`, built from `facts.md`: the services, the people, the times the records
  use, HOURS. A time taken for the chosen person carries that record's name. An empty native date or time
  input is never used.
- **A conversation is a transcript:** the customer's lines on the left, the agent's lines on the right on
  `var(--raised)`, 80% wide at most, the speaker's label once per turn change (a recorded call: the
  record's first name and NAME; the live thread: `Caller` and NAME), and the result under it as a card
  with labelled fields (Name, Visit, Day, Time, Insurance), only the ones `facts.md` fills.
- **The money button** on screen 3: `disabled`, in the disabled look, with its 1 line under it:
  `Not connected. Nothing is charged.`
- No backend, no login, no `fetch`, no `localStorage`, no cookies, no timers. A reload starts clean.
- No images, no icons.

### The scripts

At most 2 scripts, both in memory only: the screen switch, word for word, and the task script or the
agent script.

```html
<script>
function show(){var id=location.hash.slice(1)||'s1';
document.querySelectorAll('main > section').forEach(function(s){s.hidden=s.dataset.screen!==id});
document.querySelectorAll('nav a').forEach(function(a){a.toggleAttribute('aria-current',a.getAttribute('href').split('-')[0]==='#'+id.split('-')[0])});
scrollTo(0,0);}
addEventListener('hashchange',show);show();
</script>
```

**The task script.** The task button is `type="button"`. On press it reads the form and runs CHECK from
`facts.md` (a time that overlaps a record for the same person, a required choice left empty).
- The check fails on an overlap: 1 line in `var(--ink)`, weight 600, appears under the button and names
  the record it collides with in `facts.md` words (`<person> has <thing worked on> <start> to <end>.`).
  A required choice left empty: the line names its label (`Name is empty.`). The page stays on screen 2.
- The check passes: the new record is added to screen 1 in the same layout as the others, the counts are
  made again from the records on screen, screen 3 is filled with the record, and `location.hash = 's3'`.
  The field the viewer changed may differ from its RECORD line: the viewer changed it.
- A tap on a block on screen 1 fills screen 3 with that record before the screen switch.
- No success message. No word on the page says sent, confirmed, saved or charged. The record on the board
  is the result.

**The agent script.** Each question button is `type="button"`. 1 tap:
- adds the caller's line and the agent's line to the live thread, from these frames and nothing else:
  HOURS: `When are you open?` and `We're open <HOURS>.` · a SERVICE with a price: `How much is <service>?`
  and `<Service> is <price>.` · a SERVICE with quote only: `How much is <service>?` and
  `<Service> is quote only.` · a SERVICE with neither: `Do you do <service>?` and `Yes, we do <service>.` ·
  a RULE: the button and the caller's line are the rule's topic in 1 or 2 `facts.md` words with a
  question mark (`<Topic>?`), and the answer is the RULE line word for word.
- adds 1 row to the top of the `Just now` group on screen 1: the question, `Answered`.
- removes that button.

## The look

Before the founder sees it, look at the page: the website, each software screen, and the content feed.
Find a browser, the first path that exists:

| Where | Path |
|---|---|
| Mac, Chrome | `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome` |
| Mac, Edge | `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` |
| Windows, Chrome | `C:\Program Files\Google\Chrome\Application\chrome.exe` |
| Windows, Edge | `C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe` |
| Linux | `google-chrome`, `chromium` or `microsoft-edge` |

Make a temp folder with `mktemp -d`, never inside `squad/`, and name every file in it
`execution-genesis-demo-<business>-<screen>-<shot>`, so screens and parallel runs never overwrite each other. Chrome
lays a page out no narrower than 500px from the command line, so a phone shot loads the page in a 375px
frame file and shoots a 375px window, which clips the image to the frame:

```
<!doctype html><body style="margin:0"><div style="width:375px;height:<height>px;overflow:hidden"><iframe src="file://<full path>/index.html<#screen>" style="width:375px;height:<iframe height>px;border:0;margin-top:-<offset>px"></iframe></div>
```

```
"<browser>" --headless --hide-scrollbars --window-size=375,<height> --virtual-time-budget=5000 --screenshot=<temp>/execution-genesis-demo-<business>-<screen>-375-<shot>.png "file://<temp>/execution-genesis-demo-<business>-<screen>-frame-<shot>.html"
"<browser>" --headless --hide-scrollbars --window-size=1280,800 --virtual-time-budget=5000 --screenshot=<temp>/execution-genesis-demo-<business>-<screen>-1280.png "file://<full path>/index.html<#screen>"
```

3 shots per page, and per software screen (`#s2`, `#s3` on the end of the file URL):
1. **Phone, first screen:** height 812, iframe height 812, offset 0. Fixed and pinned elements (the call
   bar) are checked on this shot only.
2. **Phone, whole page, in slices:** height 1600, iframe height 8000, offsets 0, 1600, 3200 and on, 1
   frame file per slice, until the slice that holds the footer. Open every slice. The fixed call bar sits
   at the bottom of the 8000px iframe, not next to the content, and is not judged here.
3. **Laptop:** 1280x800 with no frame. Software and the feed are recorded in this window, and a website
   shows this layout on any laptop that opens it.

The content feed takes shots 2 and 3. A real website run also shoots their current home page as shot 1
(`references/shapes.md`, Website, Their site first). Open every shot. A browser error page, a blank shot,
or slices that end before the footer do not count as a look: fix the path or the offsets and shoot again.

A picture is looked at in the same browser (`references/no-slop.md`, Generated images):
- A quarter of an image `W` wide and `H` high, 1 frame file per quarter, shot at `--window-size=<W/2>,<H/2>`:
  `<!doctype html><body style="margin:0"><div style="width:<W/2>px;height:<H/2>px;overflow:hidden"><img src="file://<full path>/media/<name>" style="display:block;margin:-<0 or H/2>px 0 0 -<0 or W/2>px"></div>`
- A clip at 1.5, 3 and 4.5 seconds, 1 frame file per time, shot at `--window-size=375,469`:
  `<!doctype html><body style="margin:0"><video src="file://<full path>/media/clip-01.mp4#t=<time>" muted preload="auto" style="display:block;width:375px;aspect-ratio:4/5;object-fit:cover;object-position:50% 100%"></video>`

Run the Visuals checks in `references/no-slop.md` on the shots. What a tap does (the task script, the agent
script) is checked by reading the script. Then print 1 line,
`Looked at 375px and 1280px: <what reads first>, then <what reads second>.`, and delete the temp folder.
No browser found: run the same checks by reading the CSS, and say in 1 line that the page was not looked at.
