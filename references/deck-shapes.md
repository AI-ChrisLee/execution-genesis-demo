# The deck (the MEP: beats 1 to 3)

One deck per buyer, 9 slides, on `references/deck-cage.css`. The demo slides (5, 6, 7) change
shape by business model. The model comes off `squad/business.md` (THE MODEL; a document with
no `confirmed` stamp still carries it); the demo is read off it, never asked.

| THE MODEL says | and THE STACK is | The demo | The demo files |
|---|---|---|---|
| agency | posts, scripts, emails, newsletters, video | the piece: theirs, then the piece, then both side by side | `piece.md` |
| agency | a site, a page, a funnel, anything a browser opens, or anything else | the site: built for real, 3 captures on slides 5, 6, 7 | `index.html` (the plugin's `client.md` beside it), `shot-1.png`, `shot-2.png`, `shot-3.png` |
| consulting | anything | the structure: their columns, their facts as rows, one row lit, drawn in the deck | none past the deck |
| software | anything | 3 screens, one flow, the money button disabled, drawn in the deck | none past the deck |

## The spine (the 9 slides, every deck)

| Slide | What is on it | The cage |
|---|---|---|
| 1 | Their name. Their town under it. On the site path, `shot-1.png` full-bleed behind them; every other path, text alone | cover: `.cover`, the `img` behind the `h1` and one `.sub`; text alone: statement, `h1`, one `.sub` |
| 2 | Their problem, in their words: the strongest problem line off `notes.md`, verbatim, quote marks on, the label small under it (who, the date, "on the call") | quote: `.quote .q`, `.who` |
| 3 | What it costs them, off `notes.md`: the number huge when the call gave one, the cost in their words when the call gave words. **A cost no call gave stays off the deck**: the slide is dropped, the deck is 8, and `deck.md` says so | big number: `.big`, or quote |
| 4 | The one thing I would do: the slice, as the founder's offer would fix it, in the offer document's language, one line | statement: `h2` |
| 5, 6, 7 | The demo, by model (below) | image-embed, two-column, table, or screen |
| 8 | The first 14 days: dated steps from the day the money clears, 4 or 5 rows, each one a thing the founder does | list: `.rows` |
| 9 | The next step: "This week or next." One line | statement: `h2` |

No price of the founder's on any slide: the number is said off the sales script. No agenda
slide, no "about me" slide, no logo wall, no closing "thank you". The rail on every slide:
their name left, the slide number right, and that number counts the sections that exist, so a
deck with the cost slide dropped rails 1 to 8. One subject per slide; the one word that
carries the slide is the biggest thing on it; everything else stays small or stays off.

## Not in any deck (the one line in `plan.md`, and what keeps 2 days 2 days)

Their domain, a URL, a deploy, a backend, a login, payments, a form wired to anything, an
image file past the 3 captures, a second deck, a second flow, a new account, a key or a paid
seat, a price, and anything about the buyer that `notes.md` does not carry. The deck opens on
the founder's laptop and goes on a screen share, or leaves as `deck.pdf` by the founder's hand.
Nothing goes on the buyer's domain, in their name or on their accounts until the money clears.

## The site (agency)

The site is built for real, as one local `index.html` by the `execution-design` plugin, then
captured 3 times and put on the demo slides. The buyer sees their own site running, on a slide.

**Slides 5, 6, 7 show**

5. The top of the page: their business, by name, in their town, the result their customer buys
   as the hero, in the customer's words from `notes.md`.
6. The middle: the services or the proof, with their reviews and rating where `notes.md` (or
   the founder, off Maps at the yes) holds the count.
7. The money action (book, call, quote), its button disabled, the plugin's line under it, the
   phone number carrying the action when `notes.md` holds one.

Each slide is the capture in the card and nothing else. What to say over it is the beat map's.
`shot-1.png` also stands full-bleed behind the name on slide 1.

**Not in it**, past the shared list: more than one page, a CMS, a login, images you had to
wait for, a wired form.

**The plugin run, exactly.** Project root: `squad/mep/<name>/`, whichever name beat 0
resolved (the person, or the company on the cold path).

- Phase 1, the brief. Fill `client.md` from the offer document and `notes.md`:
  `shape: local-service` for a business, `content-brand` for a person with an audience;
  `email: NONE` and `booking_url: NONE` (nothing is wired); `website_old: NONE`; the money
  action off what the buyer's customers do; the prices in the services table off
  `notes.md` or `quote only`; every unknown fact `UNKNOWN`, never a guess and never a
  question. Print the plugin's 7 questions with the pre-filled answers for one yes. Say in
  that message: the review count and rating off Maps go into question 4 when the founder
  has them, and "I do not know" leaves them `UNKNOWN`, the page carrying nothing there.
  Question 6 (3 sites they like, 1 they hate) is not asked. Answer it from the trade's
  `Style Shortlist` in the plugin's `trades.csv` and the `Do Not Use For` column in its
  `styles.csv`: the shortlist is the liked direction, the do-not-use line is the hated one.
  No site is browsed for question 6, and on the warm path nothing about the buyer is read
  outside their folder.
- Phase 2, the plugin's 3 directions with real palettes and pairings. The founder picks
  one. Never build before the pick.
- Phase 3, the build. One `index.html`, styles inline, the pairing's Google Fonts import
  line, no framework, no build step. Every image slot in the markup at its ratio with its
  alt text and a placeholder painted by CSS. The form's `action` empty, its button
  `disabled`, the plugin's line under it, the phone number as the working action when
  there is one. No `images.md`, no `images/`.
- Skipped, said once: phase 4 (image files, the fal.ai key), phase 5 (the 9-box grade),
  phase 6 (Lighthouse, analytics, redirects, the deploy) and phase 7. Those belong to the
  paid build, after the money.

**The 3 captures.** Find a headless browser (the renderer, below). Found: capture `index.html`
3 times at 1920x1080, the top of the page, the middle, and the money action, as `shot-1.png`,
`shot-2.png`, `shot-3.png` in the buyer's folder. Headless Chrome captures the top of the window
only, so the second and third captures go through a throwaway wrapper page in the buyer's
folder, deleted the moment the two shots are taken, that frames `index.html` scrolled to the
section: a 1920x1080 body, `overflow:hidden`, holding `<iframe src="file://<folder>/index.html"
style="width:1920px;height:6000px;border:0;margin-top:-<offset>px">`, the offset being the pixel
that section starts at, read off the page (1080 and 2160 when nothing better is known; check
each capture once and move the offset when it cut a section in half). Not found: the deck
still gets built, its 3 demo slides carry a labeled hole each, and the founder gets 3 lines:
open `index.html` in the browser at full width, take 3 screenshots (the top, the middle, the
money action), and save them in the folder as `shot-1.png`, `shot-2.png`, `shot-3.png`. The
deck fills in the moment the files land.

## The piece (agency, content)

One piece made for this buyer, in their voice, for the channel they already use, shown next to
their current one so the gap shows without a word from the founder.

**Slides 5, 6, 7 show**

5. Their current piece, as posted, the channel and the date small under it.
6. The piece: the same channel, their voice, on the slice.
7. Both side by side: theirs left, the piece right, so the gap is visible on its own.

**Not in it**, past the shared list: a calendar, a strategy deck, 10 pieces, a retainer
proposal, an image.

**The file.** `piece.md`, 2 headings: `## THEIRS, as posted` (the paste, untouched, the
channel and the date named) and `## THE PIECE`. The shape follows the channel: one LinkedIn
post, one script, one whole newsletter. Text only. A piece longer than a slide holds on the
slide is cut at the slide's edge with the first lines showing; the file holds the whole.

## The structure (consulting)

The shape of the engagement, as a table the buyer's own facts fill. On the deck it is one
structure shown 3 ways, drawn in HTML on the slides; there is no file past the deck.

**Slides 5, 6, 7 show**

5. The structure: the columns as what the engagement would track, named in the buyer's words;
   the rows their facts from `notes.md`, 5 at most, none invented; fewer facts means fewer rows,
   and the plan says the count.
6. The same structure with one row lit (`.mark` on that row's text): the row the slice sits
   on, the first thing the engagement moves. Same slide re-lit, never rebuilt.
7. The one line that sits above the structure, in the buyer's words, as a statement.

**Not in it**, past the shared list: a written diagnosis, the analysis, the full workspace,
automations, a row you made up. The diagnosis is what the pilot sells.

## The screens (software)

The flow the buyer would run on day one, on 3 screens inside the deck, their data in the
fields. The screens are HTML drawn on the slides, each in a `.frame`, and there is no file
past the deck. Nothing deploys, nothing gets a URL, and the money button stays disabled.

**Slides 5, 6, 7 show**

5. Screen one: where they land on day one, their nouns already in it (their product names,
   their customers, their town, off `notes.md`).
6. Screen two: the work, one task done the way the offer says it gets done.
7. Screen three: the money button, `.btn.off`, one `.note` under it saying nothing is wired.

The arrow key is the click: the 3 slides read as one flow.

**Not in it**, past the shared list: a backend, auth, payments, a database, a second flow,
"roadmap" screens.

## The deck file (`deck.html`)

One file, self-contained: `references/deck-cage.css` pasted whole into `<style>`, then the one
accent line, then one `<section class="slide">` per slide, then the viewer script. It opens by
double-click, the arrow keys and a click move between slides, and the browser's Print to PDF
gives one slide per page. This is the skeleton; the slides' insides come from the spine and the
demo sections above.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title><buyer name></title>
<style>
/* deck-cage.css, whole, here */
:root{--accent:<the first hex on the roots file's accent color row, or #146ef5>}
</style>
</head>
<body>
<div class="deck">

<!-- 1 the cover, text alone: every path but the site -->
<section class="slide pad grid">
  <div class="mid z"><h1><buyer name></h1><p class="sub"><their town></p></div>
  <div class="rail"><span><BUYER NAME></span><span>1</span></div>
</section>

<!-- 1 the cover on the site path, INSTEAD of the section above: shot-1.png behind the
     name. A file that does not open yet drops the slide back to text -->
<section class="slide pad cover">
  <img src="shot-1.png" alt=""
       onerror="this.parentElement.classList.replace('cover','grid');this.remove()">
  <div class="mid z"><h1><buyer name></h1><p class="sub"><their town></p></div>
  <div class="rail"><span><BUYER NAME></span><span>1</span></div>
</section>

<section class="slide pad grid quote">
  <div class="mid z">
    <p class="q">"<the problem, verbatim>"</p>
    <p class="who"><first name>, <date>, on the call</p>
  </div>
  <div class="rail"><span><BUYER NAME></span><span>2</span></div>
</section>

<!-- 3 the cost (.big when a number, .quote when words; dropped when notes.md has neither) -->
<!-- 4 the slice: h2 -->
<!-- 5, 6, 7 the demo: .shot (an img, its .hole hidden behind it), .cols, table, or .frame -->

<section class="slide shot">
  <img src="shot-1.png" alt="<buyer name>, the top of the page"
       onerror="this.hidden=true;this.nextElementSibling.hidden=false">
  <div class="hole" hidden>shot-1.png is not in this folder yet.<br>Screenshot the top of index.html at full width and save it here.</div>
  <div class="rail"><span><BUYER NAME></span><span>5</span></div>
</section>

<!-- 8 the first 14 days: .rows, each .row a .k (the date) and a .t (the step) -->
<!-- 9 the next step: h2 "This week or next." -->

</div>
<script>
const s=[...document.querySelectorAll('.slide')];let i=0;
function fit(){document.documentElement.style.setProperty('--fit',Math.min(innerWidth/1920,innerHeight/1080))}
function go(n){i=Math.max(0,Math.min(s.length-1,n));s.forEach((x,k)=>x.classList.toggle('on',k===i));history.replaceState(null,'','#'+(i+1))}
addEventListener('keydown',e=>{if(e.key==='ArrowRight'||e.key===' '||e.key==='PageDown')go(i+1);if(e.key==='ArrowLeft'||e.key==='PageUp')go(i-1)});
addEventListener('click',()=>go(i+1));
addEventListener('resize',fit);fit();go((parseInt(location.hash.slice(1))||1)-1);
</script>
</body>
</html>
```

Rules the file keeps: every readable word in Inter (the serif is for one emphasised word at
most, blue, bigger than its neighbours, and never a whole line); numbers in Inter, tabular;
no eyebrow or kicker label above a title; nothing inside the safe area's 144 and 120; no
decoration past the grid ground and the one accent; nothing on a slide that `notes.md`, the
offer document, the row, or the founder's yes did not give. A non-Latin script falls back to
the system font; build anyway.

## The beat map (`deck.md`)

One table, one row per slide that exists, written after the deck so it matches the file:

```
# MEP deck · <buyer name>

| Slide | You say | On the slide |
|---|---|---|
| 1 | **<one or two lines, the founder's own opening>** | <their name>, <their town> |
| 2 | **<read the quote, then stop>** | "<the quote>" |
...
| 9 | **This week or next. Then silence.** | This week or next. |

Skipped: the cost slide, no cost on the call (or "none")
Demo: <the site: 3 captures | the piece | the structure | 3 screens>
PDF: <deck.pdf, rendered <date> | print from the browser: File, Print, Save as PDF>
looked <date>
```

The Slide column carries the rail number the deck itself shows, so a deck built without the
cost slide runs 1 to 8 and its last row is 8. The "You say" column is 1 or 2 lines a slide,
in the founder's voice, and carries no price of the founder's. It is the line said out loud,
in bold. The `looked <date>` line is appended at beat 4, once the founder has nothing left
to name; until it is there, a resume goes back to the look.

## The renderer (the captures and `deck.pdf`)

Look, in this order at beat 0, and use the first one that exists; name it in one line the
first time it is used (the captures, or the PDF), or say there that none was found.

| Where | Path |
|---|---|
| Mac, Chrome | `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome` |
| Mac, Edge | `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` |
| Windows, Chrome | `C:\Program Files\Google\Chrome\Application\chrome.exe` (or under `Program Files (x86)`) |
| Windows, Edge | `C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe` |
| Linux | `google-chrome`, `chromium`, `chromium-browser` or `microsoft-edge` on PATH |

A capture: `"<browser>" --headless --hide-scrollbars --window-size=1920,1080
--screenshot=<folder>/shot-1.png file://<folder>/index.html` (the wrapper page's path for
shots 2 and 3).

The PDF: `"<browser>" --headless --no-pdf-header-footer --print-to-pdf=<folder>/deck.pdf
file://<folder>/deck.html`. The print sheet in the cage makes one slide per page at 1920x1080.
Open the PDF once and check the page count matches the slide count.

None found: no install is asked for. The founder screenshots by hand (the site) and prints
from the browser (File, Print, Save as PDF), and `deck.md`'s PDF line says so.

## A cold buyer

The company came off `squad/cold-list.csv` and nobody has talked to them, so `notes.md` does
not exist. The intake is that row: the company, its town, its trade, its one broken-thing
sentence, plus what you can see from outside (their site on a phone, their Maps listing,
whether the booking button goes anywhere, their review count). Every line of it is labeled
`(observation · cold list <cut date>)` and carries no quote marks.

What the deck does when there are no words:

**Slide 2** carries the broken-thing sentence, no quote marks, the observation label small
under it where the call label would sit.

**Slide 3** is dropped: no call gave a cost.

**Slide 4** turns the broken thing into the result the founder's own offer sells, in
`squad/business.md`'s language and never in the buyer's.

**The site.** The top slide comes off the row, with the review count and rating when the
founder has them at the yes. The hero has no customer words to use, so it carries the
offer's result. The money action is unchanged.

**The piece.** Their current piece is public, so the paste still works. The slice is the
observation.

**The structure.** The rows are the row's own facts, so there are fewer of them. The plan
says the count, and you never pad it.

**The screens.** The fields carry the nouns on the row and nothing else.

Every fact the row does not carry is `UNKNOWN`, and `UNKNOWN` is never a question. The
template test still holds: if the deck would read the same for the shop next door, it is not
built yet, and on this path the broken-thing sentence is the only thing that makes it theirs.
