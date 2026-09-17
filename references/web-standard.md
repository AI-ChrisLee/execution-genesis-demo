# The web standard

The design rules 1 `index.html` follows, for the website and the software shapes. The content feed
takes The lookup, Tokens, Type, Colour, Layout and The look. The 4 CSV files sit next to this one.

## The lookup, 3 reads, no pick

1. `trades.csv`: the row whose `Trade` matches TRADE on `facts.md` (before `facts.md` exists, WHO on
   `squad/business.md`). No match: try once with a broader name. Still none: take the closest row by
   what the customer walks out with (a look: a salon row; a treatment: a clinic row; a job done at their
   home: a trade row; something to read or watch: a creator row). Take its `Style Shortlist`,
   `Buys This Result`, `Never Sell This`, `Local Signals` and `Watch Out`.
2. The first style named in `Style Shortlist`, found by its `Style` in `styles.csv`. Take its
   `Palette ID`, `Font Pairing ID`, `Radius`, `Section Order` and `Copy Angle`. Never read `Motion` or
   `Imagery Direction`: motion is set under Layout here, and the demo has no photos. Software and the
   content feed take only `Palette ID`, `Font Pairing ID` and `Radius`.
3. `palettes.csv` by `Palette ID`: Surface, Raised, Ink, Muted, Accent, Text On Accent.
   `fonts.csv` by `Font Pairing ID`: `Google Fonts Import`, `CSS Variables`, `Heading Scale`,
   `Body Size`, `Notes`.

Copy the values out of the files. Never type a hex or a font name from memory. No 3 directions, no
question to the founder.

When the trade row's `Watch Out` or the style's `Copy Angle` names a place on the page (pinned, header,
every screen size, first screen), that place is built into the skeleton. It is never left for a note
round.

## The file

- 1 file. 1 `<style>` block, the pairing's import line at its top. No framework, no build step, no file
  past the font import. A website has no script. Software has the scripts under Software.
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
  tracking) become their own properties.
- Apply the pairing's `Notes` wherever the display font is used: an optical size note becomes
  `font-variation-settings: 'opsz' <n>`, a case or tracking note becomes `text-transform` or
  `letter-spacing`, and a smallest size (`never under 28px`) holds everywhere.
- Paragraphs `max-width: 68ch`.
- Software type is under Software.

## Colour

- 6 values: the 5 palette colours and Text On Accent. Nothing else.
- The accent, on a website: the money button, a text link inside a sentence, the focus ring. On
  software: the task button or the agent's question buttons, and the focus ring. On the content feed:
  the focus ring only.
- Borders use `var(--line)`. No shadows. No gradient anywhere.

## Layout, 375px first

- The base CSS is the phone layout. Wider screens change it only inside `@media (min-width: 720px)`.
- Side padding `var(--s4)`. Section padding `var(--s7)` on phones, `var(--s8)` wider. Sections are split
  by space, not a border on every section. On a website, the money section alone sits on a full-width
  `var(--raised)` band, its content inside `.wrap`.
- On phones, no fixed width over 343px. Blocks are `width: 100%` with a `max-width`.
- From 720px the page is laid out for a laptop, not stretched from the phone. Website: the hero is 2
  columns (`grid-template-columns: 1.15fr 1fr; gap: var(--s7); align-items: center`), the words and the
  money action left, the visit card right. The services list and the form each sit in 2 columns next to
  their heading (`grid-template-columns: 1fr 1.4fr`). No block spans the full `.wrap` width with nothing
  in it, and no column of 343px stands alone with empty space to its right.
- Every button and link a thumb uses is 44px tall at the least.
- The money button: `var(--accent)` fill, `var(--on-accent)` text, 52px tall, 24px side padding,
  `var(--radius)`, weight 600. Hover: `background: var(--ink); color: var(--surface)`.
- A disabled button reads as switched off, not faded: `background: var(--raised); color: var(--muted);
  border: var(--line); cursor: not-allowed`. Never `opacity`.
- A phone number never breaks across lines, in a button or in a sentence (`.phone { white-space: nowrap; }`).
- Inputs and selects: 52px tall, 16px text, `1px solid var(--muted)`, a visible focus ring in
  `var(--accent)`. Every field has a visible `<label>`. No `placeholder` attribute.
- Motion: a colour change on hover, 150ms, and nothing else.

## Website

- **Sections:** the style row's `Section Order` gives the order. Each section is filled only from these
  fields, and a section whose fields are all blank is dropped: hero = NAME, TOWN, services, prices,
  HOURS, PHONE, ACTION · trust, proof or credentials strip = YEARS OPEN, RATING with REVIEW COUNT,
  licenses, memberships, INSURANCE or BILLING, KIDS, LANGUAGES · services, treatments, menu or packages =
  SERVICE lines · how fast = a response time or same-day fact the founder gave · practitioner, coaches,
  stylists or about = a person's name with the role `facts.md` gives, no portrait · first visit, process
  or how it works = steps the founder gave · reviews = reviews pasted with a source · area or location =
  ADDRESS, NEAR, AREA, PARKING, which live in the visit card · money section = ACTION · FAQ = only answers
  `facts.md` holds · footer = NAME, PHONE, HOURS, ADDRESS or NEAR or AREA. A section this map does not
  name (the work, before and after, a gallery) is dropped. The money section is the last section before
  the footer; an FAQ in the row moves above it.
- **The hero:** THE PROBLEM on `squad/business.md` picks which fact leads. The trade row's
  `Buys This Result` only breaks a tie. `Copy Angle` and `Watch Out` are read as a list of objections to
  answer with facts. An objection `facts.md` cannot answer stays unanswered, and its missing fact goes on
  the blanks line. Their own words never go on the page. In order:
  1. A small name line: NAME in the display font, TOWN in `var(--muted)`. From 720px, when the call bar
     header carries the name, only TOWN stays on this line.
  2. The H1, 12 words at most, the leading fact in `facts.md` words: RESULT when it is that fact; else a
     WORDS line that carries it and passes the shop-down-the-street test; else the fact said plainly (a
     service with its price, the hours, the place).
  3. A second line, 20 words at most, with up to 2 more facts.
  4. The money action (below).
  5. The visit card.
- **The call bar** (ACTION includes call): 1 `<header class="callbar">` as the first element in `<body>`,
  holding the name and the money button, which reads `Call <PHONE as written on facts.md>` and is the
  working `tel:` link. Below 720px it is fixed to the bottom of the screen with the button full width;
  from 720px it is a header pinned to the top, the name left and the button right.

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
    phone is the number as a large `tel:` link in `var(--ink)` (weight 600, 1.5rem, `.phone`). The money
    section repeats the same `Call <PHONE>` button, with HOURS under it, and above it the strongest WORDS
    line that passes the shop-down-the-street test, in the display font. No WORDS line passes: a plain 1
    to 3 word label in ACTION's words.
  - **Book or quote in ACTION:** the money section holds the form, `id="book"`, `action=""`, with real
    controls: a `<select>` of the service names on `facts.md`, a `<select>` of the days HOURS names (no
    HOURS: no day field), Name, Phone. Typing and picking work. Only its button is `disabled`, in the
    disabled look, with 1 line under it: `This form is not connected yet. Call <phone>.`, the phone as
    plain text in `<span class="phone">` (no phone: `This form is not connected yet.`).
  - **Both:** the money section holds the call first, then the form under a plain label in ACTION's words
    (`Book online`). The hero puts a text link in ACTION's words to `#book` under its phone.
  - **Book or quote with no call:** no call bar. The hero's money button is the accent button, and it goes
    to `#book`.
  - The money button says the same words everywhere it appears.
- **The visit card**, in the hero: the block a photo would fill holds the facts a customer needs to come
  in, laid out as a finished object. No photo, no grey box, no `Photo here`, no slot.

```html
<aside class="card" aria-label="Visit">
  <p class="card-label">Hours</p>
  <dl class="days"><!-- 1 dt and dd per day or day range HOURS names, in its words --></dl>
  <p class="card-label">Where</p>
  <p><!-- ADDRESS as a link to the map, else NEAR, else AREA; PARKING on its own line under it --></p>
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
`facts.md` carries go in, and never a Closed row the founder did not say. With no call bar and a PHONE,
the card adds a `Phone` label and the number as an ink `tel:` link. With neither HOURS nor a place, there
is no card and the hero is type only. At 375px the card sits under the hero text, from 720px right of it.

- **The proof cards:** the proof facts, each a card on `var(--raised)` with `var(--radius)` and
  `padding: var(--s4)`. 2 columns on phones (an odd count: the first card spans both); from 720px, 3
  columns for 3, 5 or 6 cards, and 2 or 4 for 2 or 4 cards. In each card, the number with its 1 joining
  word (`Since 1983`, `# 23799`, `4.8`) is in the display font at its heaviest imported weight and the h2
  size, and the rest of that same fact sits under it in `var(--muted)`. Both are word for word off
  `facts.md`, split only where the number meets the words. A fact with no number is 1 line in the display
  font at the h3 size.
- **The footer:** name, phone, hours, and where (ADDRESS, NEAR or AREA) off `facts.md`. Nothing else.

## Software

- The palette, the fonts and the radius come from the lookup on their trade (the grooming shop, not
  software). Section Order, Copy Angle and Heading Scale are skipped.
- **It reads as a tool, not a page.** A top bar on every screen: NAME in `var(--font-display)` at
  1.75rem (the pairing's `Notes` still hold), and at its right a `Sample data` tag in `var(--muted)` at
  .875rem, with a `var(--line)` border and `var(--radius)`. Never an eyebrow over a heading.
- **Type for a tool:** screen titles, column heads, record names and buttons in `var(--font-body)` at
  weight 600. Screen title 1.5rem, section title 1.125rem, body 1rem/1.5, meta .875rem, never under
  14px. The display font goes only on the name in the top bar.
- **The nav:** 3 links in `facts.md` words. Phones: a bar of 3 equal tabs, 44px tall, under the top bar.
  From 720px: a left column 220px wide beside the screen, the whole page up to 1200px wide, with the top
  bar, the nav and the screen on 1 left edge. The current tab: `background: var(--ink); color:
  var(--surface)`.
- **Screens:** `<section data-screen="s1">`, `<section data-screen="s2">`, `<section data-screen="s3">`
  inside `<main>`, with no `id` on them, so the browser never jumps the top bar off screen. The agent's
  written-out records add `s2-1` to `s2-5`. The CSS carries `main > section[hidden] { display: none; }`.
  Every link opens a screen, no `href="#"`, and every record row that looks like a link opens its screen.
- **The day board:** `display: grid`, a first column of times, then 1 column per person, room or
  vehicle, 1 grid row per time step; each record is a block (`grid-row: <start> / <end>`) on
  `var(--raised)` with `var(--line)` and `var(--radius)`. Phones: up to 2 columns side by side, more stack
  1 under the other. At 1280x800, screen 1 shows the whole day, or every row, without scrolling.
- **Status and note:** a status (where the record is today) is a right-aligned label, weight 600, with a
  `var(--line)` border and `var(--radius)`. A note (how to handle it) is plain text under the name. They
  never share a style.
- **Choices, never blank pickers:** day, time, person and service on a form are 44px buttons with
  `aria-pressed`, or a `<select>`, built from `facts.md`: the services, the people, the times the records
  use, HOURS. A time taken for the chosen person carries that record's name. An empty native date or time
  input is never used.
- **A conversation is a transcript:** the customer's lines on the left, the agent's lines on the right on
  `var(--raised)`, 80% wide at most, the speaker's label once per turn change, and the result under it as
  a card with labelled fields (Name, Visit, Day, Time, Insurance), only the ones `facts.md` fills.
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
- The check fails: 1 line in `var(--ink)`, weight 600, appears under the button and names the record it
  collides with in `facts.md` words (`Lena has Biscuit 8:30 to 11:00.`). The page stays on screen 2.
- The check passes: the new record is added to screen 1 in the same layout as the others, the DERIVED
  line is counted again, screen 3 is filled with the record, and `location.hash = 's3'`.
- No success message. No word on the page says sent, confirmed, saved or charged. The record on the board
  is the result.

**The agent script.** Each question button is `type="button"`. 1 tap:
- adds the customer's line and the agent's line to the live thread, from these frames and nothing else:
  HOURS: `When are you open?` and `We're open <HOURS>.` · a SERVICE with a price: `How much is <service>?`
  and `<Service> is <price>.` · a SERVICE with quote only: `How much is <service>?` and
  `<Service> is quote only.` · a RULE: the button and the customer's line are the rule's topic in 1 or 2
  `facts.md` words with a question mark (`Insurance?`), and the answer is the RULE line word for word.
- adds 1 row to the top of the log on screen 1: `Just now`, the question, `Answered`.
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
`the-demo-<business>-<screen>-<shot>`, so screens and parallel runs never overwrite each other. Chrome
will not lay a page out narrower than 500px from the command line, so the phone shots use a 375px frame,
1 frame file per height:

```
<!doctype html><body style="margin:0"><iframe src="file://<full path>/index.html<#screen>" style="width:375px;height:<height>px;border:0"></iframe>
```

```
"<browser>" --headless --hide-scrollbars --window-size=500,<height> --virtual-time-budget=5000 --screenshot=<temp>/the-demo-<business>-<screen>-375-<first or full>.png "file://<temp>/the-demo-<business>-<screen>-frame-<height>.html"
"<browser>" --headless --hide-scrollbars --window-size=1280,800 --virtual-time-budget=5000 --screenshot=<temp>/the-demo-<business>-<screen>-1280.png "file://<full path>/index.html<#screen>"
```

3 shots per page, and per software screen (`#s2`, `#s3` on the end of the file URL):
1. **Phone, first screen:** height 812. Fixed and pinned elements (the call bar) are checked on this
   shot only.
2. **Phone, whole page:** height 6000. The whole page down to the footer. Empty surface under the footer
   is not a fail.
3. **Laptop:** 1280x800 with no frame. Software and the feed are recorded in this window, and a website
   shows this layout on any laptop that opens it.

The content feed takes shots 2 and 3. Open every shot. A browser error page, a blank shot, or a whole-page
shot that ends before the footer does not count as a look: fix the path or the height and shoot again.
Run the Visuals checks in `references/no-slop.md` on the shots. What a tap does (the task script, the agent
script) is checked by reading the script. Then print 1 line,
`Looked at 375px and 1280px: <what reads first>, then <what reads second>.`, and delete the temp folder.
No browser found: run the same checks by reading the CSS, and say in 1 line that the page was not looked at.
