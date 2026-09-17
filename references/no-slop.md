# The no-slop check

Run every item on every file of the demo before the founder sees it, and again on whatever a note
round changed. Each item passes or fails. A fail gets fixed, then the item runs again. Nothing is
shown with a fail still on it, and nothing is shown with a note about what is wrong.

**What runs on each shape.** The website runs every item. Software runs every item by its Software
line. The content feed marks these `n/a, content` and skips them: The result never the tool, Line
limits (the header line excepted), Buttons in their customer's words, The squint, Taps 44px. On the
feed, `--accent` stays in `:root` and is used only on the focus ring; that is a pass. A Notion program
runs The facts rule, Copy and The board, and marks the rest `n/a, program`.

The 1 exception is a generated image or clip that fails: a redo costs credits, so print which piece
failed, why in a few words, and the redo cost, and wait for yes. A redo may rewrite its prompt: keep the
PERSON and PLACE lines, and name the failed part as what it should be (`a plain unmarked grey box`). Get
the new cost before printing it.

---

## The facts rule

- [ ] **Every name, number and claim traces to a line in `facts.md`.** List every proper noun, number,
      price, date, time, phone, rating, count and promise on the page. Find each one on `facts.md`.
      1 that is not there fails. Implied claims count: for every sentence that says who does what, the
      who and the what both trace to `facts.md`. A line counts only when its source is on the list in
      `references/shapes.md` (The folder, Sources). A value the agent set itself (a date, a count, a
      stage name, a week number) fails even when it is written on `facts.md` (a `DERIVED` line excepted), and so does any value a
      skill instruction told the agent to make up.
- [ ] **No stitched claims.** A sentence that joins 2 facts may not claim anything neither fact says on
      its own. A year stays on what the page put it on: "Quality Work Since 1983" dates the business and
      never dates a service. A joined line that makes a new claim fails. Use 1 fact word for word instead.
- [ ] **No fake proof.** No review, rating, count, testimonial, year founded, award, client name,
      client logo, or "as seen on" unless `facts.md` carries it with a source.
- [ ] **Blanks stay blank.** A field under `## Blank` is not on the page in any form, not even as a
      softer version. The section it would fill is dropped.
- [ ] **No price of the founder's.** Nothing from `## PRICE` on `squad/business.md` is on the demo.
- [ ] **No fake send.** Every form, book or pay button that does nothing inside the page is `disabled`
      and carries its 1 line (`references/shapes.md`, `references/web-standard.md`). No success message,
      and no line saying anything was sent, confirmed, saved or charged. Search for `alert(`, `setTimeout`,
      `setInterval` and `preventDefault`: 0 hits.
- [ ] **Conversations say only `facts.md`.** A written-out conversation turns 1 record's facts into
      first-person lines. It may add only these, each with no new fact: a greeting with NAME, a question
      asking for a field `facts.md` has (insurance, day, time), the agent's answer taken from another line
      of `facts.md` (a price, the hours, the insurance list, the emergency rule), and the customer's yes.
      The customer says yes before the result shows. A service, a person or a time the record does not
      name stays out.
- [ ] **The tool uses what it was told.** A record whose question another line answers shows that answer
      (a caller asks what a service costs: its price from SERVICE). Every fact the tool would need on the
      job (hours, prices, insurance, the emergency rule) is used at least once on screens 2 or 3, or it
      fails.
- [ ] **Counts made from the records.** A count or a sum nobody gave (`5 calls, 4 booked`) is written on
      `facts.md` first, as a `DERIVED` line made only from the records (`counted from RECORD 1 to
      RECORD 5`), then used. A count made any other way fails.

---

## Copy

- [ ] **No long dash.** Search every file for the pattern `\x{2014}`: 0 hits.
- [ ] **None of these words:** delve, tapestry, elevate, robust, seamless, cutting-edge, best-in-class,
      state-of-the-art, world-class, unparalleled, bespoke, holistic, solutions, unlock, harness, embark,
      journey, empower, innovative, top-notch, one-stop, hassle-free. Search case-blind: 0 hits.
- [ ] **None of these lines:** "curated experience", "tailored to your needs", "passionate about",
      "dedicated to excellence", "we pride ourselves", "your trusted partner", "quality you can count
      on", "we go above and beyond", "customer satisfaction is our top priority", "with years of
      experience", "peace of mind", "look no further", "Welcome to". Search case-blind: 0 hits.
- [ ] **The shop down the street test.** Read every headline and sentence. Could a competitor in the
      same town say it word for word? Then it fails: replace it with their number, their place, their
      hours or their words, or cut it. Putting a person's name into a sentence any shop could say does
      not pass, and it makes a new claim: `Call Dr. X` says the owner answers the phone, and
      `What Dr. X sees you for` says that person does every service. A heading with no fact to carry
      becomes a plain 1 to 3 word label (`Prices`, `Hours`, `Book a visit`). Labels, service names and
      customer types copied word for word off `facts.md` are not tested. Sentences are. Their own line
      (WORDS N) may stand in the display font where a heading would go, at up to 16 words, and it still
      has to pass this test.
- [ ] **The result, never the tool.** Website: the hero leads with the fact THE PROBLEM on
      `squad/business.md` points at, never the provider at work or the tool, and nothing on the page
      leads with the trade row's `Never Sell This`. Software: screen 1 leads with the DERIVED line and
      the records, never with the tool's name or a feature.
- [ ] **Line limits.** H1 12 words or fewer. Subhead 20. Section heading 8 (a WORDS line in its place, 16).
      Button 4, a verb first, the phone number counting as 1 word. Count them.
- [ ] **Buttons in their customer's words.** "Call 604-555-0142", "Book Tuesday", "Hold the spot". Never
      "Learn more", "Get started", "Submit", "Contact us", "Click here".
- [ ] **Sentences vary.** Read 5 in a row. All about the same length fails. A list of 3 in every
      heading fails.
- [ ] **1 adjective per noun at most.** 2 in a row fails. A service name word for word off `facts.md`
      is not tested.
- [ ] **Their nouns.** Software and content use the words on `facts.md`, plus the fixed label set in
      `references/shapes.md` (Software, Words). Read the words a person sees, not the code (`content=`
      and `justify-content` are code). "Dashboard", "Analytics", "Insights", "Overview", "Workflow",
      "Platform", "Content", "Engagement" fail unless the founder said them.
- [ ] **No emoji or hashtag** the facts did not show.

---

## Visuals, for `index.html`

- [ ] **Fonts from `fonts.csv`.** The import line is the pairing's own, whole, as the cell holds it. Its
      `Notes` are applied. Inter, Roboto, Arial or a bare `system-ui` as the body font fails (unless the
      pairing is Inter's own).
- [ ] **6 colours.** List every colour value in the file. Any value past the palette row's 6 (Surface,
      Raised, Ink, Muted, Accent, Text On Accent) fails. `transparent` inside the `--line` token does not
      count.
- [ ] **1 loud colour.** Website: `var(--accent)` is on the money button, and past it only on a text link
      inside a sentence or the focus ring, and exactly 1 accent button shows on each first-screen shot.
      Software: on the task button or the agent's question buttons, and the focus ring. Content: the focus
      ring only.
- [ ] **No gradient.** Search for `gradient`: 0 hits. No gradient text, no purple to blue.
- [ ] **No row of 3 icon cards.** No icons. No "Why choose us" section.
- [ ] **No motion past a hover.** Search for `@keyframes` and `animation`: 0 hits. No counters, no
      parallax, no fade-up.
- [ ] **Nothing waits for content.** Search for `Photo here`, `placeholder`, `Lorem`, `Coming soon`,
      `TBD` and `class="slot"`: 0 hits. Website and software: no `<img>`. Content: every `src` and
      `poster` file exists in the folder. Look at both first screens (375px and 1280x800): a box, band or
      column with nothing in it fails.
- [ ] **Nothing reads unfinished.** Fails: a native placeholder on show (`yyyy-mm-dd`, `--:--`), a screen
      that is only a heading and a button, a column or card holding half a screen of nothing, a disabled
      button that is faded instead of switched off, 2 different tappable things on 1 screen with the same
      words, a screen button that repeats its own H1, a record row that looks like a link and opens
      nothing. The call bar and the money section's button are 1 action and pass.
- [ ] **The squint.** Do it on the 375px first-screen shot and on the 1280x800 shot. Website: the promise
      reads first, the money action second. Software: screen 1 reads as the day or the log (who, when,
      what) before any heading; screen 2 shows the record in the form and the task button, or the thread
      and its question buttons; screen 3 shows the record before the button.
- [ ] **375px first.** The layout is written for 375px and grows with `min-width` media queries. Nothing
      runs off the side at 375px.
- [ ] **Laptop layout.** At 1280x800, website: the hero is 2 columns and no phone column stands alone in
      an empty screen. Software: the nav column and the screen fill the width to 1200px, and screen 1
      shows the whole day or every row. Content: the header and the row of 4 tiles show on the first
      laptop screen, never a blank box.
- [ ] **Taps 44px.** Every button and link a thumb uses is 44px tall or more.
- [ ] **No platform chrome on the content page.** No like counts, follower counts, verified badges,
      logos, or app buttons.

---

## The board, for a Notion program

Fetch the demo page, the board view and 1 card. When a browser can open the link, look at the board.
Otherwise say in 1 line that the board was checked from its config and not seen.

- [ ] **The board comes first.** Under the name and promise lines comes the board. No `inline="false"`
      database link and no table sits on the page.
- [ ] **Every stage is a column.** Count the cards in each Stage option. A stage with 0 cards fails,
      because Notion hides it.
- [ ] **The card face shows the work.** The view's `displayProperties` lists Client and every other
      property the cards carry. `["Client"]` alone fails.
- [ ] **No half card.** Every card fills every property in the schema. An empty property on any card
      fails: get the fact, or drop the column.
- [ ] **Their name and their promise are on the page**, word for word off `facts.md`.
- [ ] **Every stage has its page**, and every card's page links to it.
- [ ] **No property repeated as a text line** on a card's page.
- [ ] **No `demo`, `test`, `sample board` or `template` word** in the page title, the view name or a
      heading.

---

## Generated images and the clip

Open every file and look at it twice: whole, then as 4 quarter crops at full size (Mac, for an image
`W` wide and `H` high: `sips -c <H/2> <W/2> --cropOffset <0 or H/2> <0 or W/2> media/01.png --out <temp>/q1.png`).
Look hard at every object that carries a maker's label in real life (a machine, an appliance, a box,
equipment, packaging) and at every edge of the frame. A fail in any crop fails the piece, and every
piece gets the same look. A clip is not a picture: on a Mac run
`qlmanage -t -s 1080 -o <temp> media/clip-01.mp4` and look at the still it makes. No way to make a
still: say in 1 line that the clip was not looked at.

- [ ] Phone look: real light, a real place, some grain. No studio backdrop, no glossy skin, the subject
      off the centre line.
- [ ] The place and the light match `facts.md`.
- [ ] All 4 pieces show the same person (hair, clothes, build) and the same room (walls, floor, rack or
      bench, door). 1 that reads as another person or another room fails.
- [ ] No face: the head is out of the frame or turned away, or it is hands only.
- [ ] The picture shows what its caption says, from the angle it is taught from. A body in tight clothes
      framed from behind as the subject fails.
- [ ] No readable text, no melted letters, no sign, no logo, no watermark.
- [ ] Hands have 5 fingers. Nothing melts, bends, floats or doubles.
- [ ] No phone, no hand holding a phone, no app screen in the frame.
