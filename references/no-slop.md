# The no-slop check

Run every item on every file of the demo before the founder sees it, and again on whatever a note
round changed. Each item passes or fails. A fail gets fixed, then the item runs again. Nothing is
shown with a fail still on it, and nothing is shown with a note about what is wrong.

**What runs on each shape.** The website runs every item. Software runs every item by its Software
line, and skips Generated images. The content feed marks these `n/a, content` and skips them: The
result never the tool, Line limits (the header line excepted), Buttons in their customer's words, The
squint, Taps 44px, The paid-build test, Nothing on facts.md is dropped. A Notion program runs The facts
rule, Copy and The board, and marks the rest `n/a, program`.

**A piece that fails is redone, not discussed.** Print 1 line saying which piece failed and why in a
few words, then run it. A redo may rewrite its prompt: keep the PERSON and PLACE lines, and name the
failed part as what it should be (`a plain unmarked box`).
- A piece that fails twice changes its framing, not its wording: WHOLE becomes CLOSE or CLOSE becomes
  WHOLE, and the moment changes. A website photo changes its subject to another part of the same work.
- After the 3rd fail on 1 piece, run no more jobs on it. Print its 3 failed files with the item each
  one failed, and build without it: the set or the page is built from the pieces that pass, and
  nothing with a fail goes on the page. A note round can ask for it again.

---

## The facts rule

- [ ] **Every name, number and claim traces to a line in `facts.md`.** List every proper noun, number,
      price, date, time, phone, rating, count and promise on the page. Find each one on `facts.md`.
      1 that is not there fails. Implied claims count: for every sentence that says who does what, the
      who and the what both trace to `facts.md`. A line counts only when its source is on the list in
      `references/shapes.md` (The folder, Sources). A value the agent set itself (a date, a count, a
      stage name, a week number) fails even when it is written on `facts.md` (a `DERIVED` line and a
      sample record excepted), and so does any value a skill instruction told the agent to make up. The
      clock labels on a day board and a count a task script makes from the records on screen are not
      facts and pass.
- [ ] **Nothing on `facts.md` is dropped.** Website: list every line above `## Blank` except FIRST NAME,
      TRADE, ACTION, SETTING, LIGHT, WORDS N, a person with no role, and LOOM. Find each one on the page.
      1 missing fails.
- [ ] **No stitched claims.** A sentence that joins 2 facts may not claim anything neither fact says on
      its own. A year stays on what the page put it on: "since <year>" dates the business and never
      dates a service. A joined line that makes a new claim fails. Use 1 fact word for word instead.
- [ ] **The weakest wording wins.** When the pages state 1 claim at 2 strengths, `facts.md` carries both
      lines and the page uses the hedged one word for word.
- [ ] **No fake proof.** No review, rating, count, testimonial, year founded, award, client name,
      client logo, or "as seen on" unless `facts.md` carries it with a source.
- [ ] **No photo called theirs.** Website: no caption, alt text, heading or sentence says a generated
      photo shows their room, their team, their work or their customers. Every `<img>` has `alt=""` and
      no caption.
- [ ] **Blanks stay blank.** A field under `## Blank` is not on the page in any form, not even as a
      softer version. The section it would fill is dropped.
- [ ] **No price of the founder's.** Nothing from `## PRICE` on `squad/business.md` is on the demo.
- [ ] **No fake send.** Every form, book or pay button that does nothing inside the page is `disabled`
      and carries its 1 line (`references/web-standard.md`, The money action; Software, The money
      button). No success message, and no line saying anything was sent, confirmed, saved or charged.
      Search for `alert(`, `setTimeout`, `setInterval` and `preventDefault`: 0 hits.
- [ ] **Conversations say only `facts.md`.** A written-out conversation turns 1 record's facts into
      first-person lines. It may add only these, each with no new fact: a greeting with NAME, a question
      asking for a field `facts.md` has (insurance, day, time), the agent's answer taken from another line
      of `facts.md` (a price, the hours, the insurance list, the emergency rule), and the customer's yes.
      The customer says yes before the result shows. A service, a person or a time the record does not
      name stays out.
- [ ] **The tool uses what it was told.** A record whose question another line answers shows that answer
      (a caller asks what a service costs: its price from SERVICE). Every fact the tool would need on the
      job (hours, prices, insurance, the emergency rule, a note on a record) is used at least once on
      screens 1 to 3, or it fails.
- [ ] **Counts made from the records.** A count or a sum nobody gave (`<N> calls, <N> booked`) is written
      on `facts.md` first, as a `DERIVED` line made only from the records (`counted from RECORD 1 to
      RECORD <N>`), then used. The live rows a tap adds are never counted in it. A count made any other
      way fails.

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
      not pass, and it makes a new claim: `Call <name>` says that person answers the phone, and
      `What <name> sees you for` says that person does every service. A heading with no fact to carry
      becomes a plain 1 to 3 word label (`Prices`, `Hours`, `Book a visit`). Labels, service names and
      customer types copied word for word off `facts.md` are not tested. Sentences are. Their own line
      (WORDS N) may stand in the display font where a heading would go, at up to 16 words, and it still
      has to pass this test. The H1 is always tested, even when it is a `facts.md` line copied word for
      word: an H1 any shop in the trade could say fails while `facts.md` holds a fact only this business
      has, or a place fact it could join (`references/web-standard.md`, The hero).
- [ ] **The result, never the tool.** Website: the hero leads with the lead fact that The hero in
      `references/web-standard.md` picks, never the provider at work or the tool, and nothing on the page
      leads with the trade row's `Never Sell This`. Software: screen 1 leads with the DERIVED line and
      the records, never with the tool's name or a feature.
- [ ] **Line limits.** H1 12 words or fewer. Subhead 20. Section heading 8 (a WORDS line in its place, 16).
      Button 4, a verb first, the phone number counting as 1 word. The agent's question buttons are the
      caller's question and pass. Count them.
- [ ] **Buttons in their customer's words.** `Call <PHONE>`, `Book <day>`, `Hold the spot`. Never
      "Learn more", "Get started", "Submit", "Contact us", "Click here".
- [ ] **Sentences vary.** Read 5 in a row. All about the same length fails. A list of 3 in every
      heading fails.
- [ ] **1 adjective per noun at most.** 2 in a row fails. Any value copied word for word off `facts.md`
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
- [ ] **6 colours.** List every colour value in the file: `#hex`, `rgb()`, `hsl()`, and colour names used
      as a property value. Words inside property names, like `white-space`, are not colours. Any value
      past the palette row's 6 (Surface, Raised, Ink, Muted, Accent, Text On Accent) fails. `transparent`
      inside the `--line` token does not count.
- [ ] **1 loud colour.** Website: `var(--accent)` is on the money button, and past it only on a text link
      inside a sentence or the focus ring, and exactly 1 accent button shows on each first-screen shot.
      Software: on the task button or the agent's question buttons, and the focus ring. Content: on the
      ACTION's word in each caption and the focus ring.
- [ ] **No gradient.** Search for `gradient`: 0 hits. No gradient text, no purple to blue.
- [ ] **No row of 3 icon cards.** No icons. No "Why choose us" section. Photo cards of their services
      pass.
- [ ] **No motion past a hover.** Search for `@keyframes` and `animation`: 0 hits. No counters, no
      parallax, no fade-up. The content clip playing on its own passes.
- [ ] **Nothing waits for content.** Search for `Photo here`, `placeholder`, `Lorem`, `Coming soon`,
      `TBD` and `class="slot"`: 0 hits. Software: no `<img>`. Website and content: every `src` and
      `poster` points at a file that exists in `media/`, and no `<img>` points anywhere else. Look at both
      first screens (375px and 1280x800): a box, band or column with nothing in it fails.
- [ ] **Nothing reads unfinished.** Fails: a native placeholder on show (`yyyy-mm-dd`, `--:--`), a screen
      that is only a heading and a button, a column or card holding half a screen of nothing, a disabled
      button that is faded instead of switched off, 2 different tappable things on 1 screen with the same
      words, a screen button that repeats its own H1, a record row that looks like a link and opens
      nothing, a headline with 1 word alone on its last line. The call bar and the money section's button
      are 1 action and pass. The nav's current tab naming its own screen passes.
- [ ] **The paid-build test.** Website: on the phone slices and the 1280x800 shot, count the filled
      sections between the hero and the money section. Fewer than 3 fails, and so does any section with 1
      item under its heading. Fold the thin section (`references/web-standard.md`, Website, Sections), and
      name the missing Section Order facts first on the blanks line. A page that reads as a contact card
      fails even when every other item passes. Software: screen 1 holds every record on `facts.md` but the
      one that goes wrong, so a made-up task tool shows 7 at the least and the agent 6.
- [ ] **The squint.** Do it on the 375px first-screen shot and on the 1280x800 shot. Website: the promise
      reads first, the money action second. Software: screen 1 reads as the day or the log (who, when,
      what) right under its title; screen 2 shows the record in the form and the task button, or the
      thread and its question buttons; screen 3 shows the record before the button.
- [ ] **375px first.** The layout is written for 375px and grows with `min-width` media queries. Nothing
      runs off the side at 375px.
- [ ] **Laptop layout.** At 1280x800, website: the hero is 2 columns and no phone column stands alone in
      an empty screen. Software: the nav column and the screen fill the width to 1200px, screen 1 shows the
      whole day or every row, and screens 2 and 3 are 2 columns. Content: the header and all 4 posts with
      their captions on the first laptop screen, each piece shown once. A piece shown twice, or a column
      with empty screen on both sides, fails.
- [ ] **Taps 44px.** Every button and link a thumb uses is 44px tall or more.
- [ ] **No platform chrome on the content page.** No like counts, follower counts, verified badges,
      logos, app buttons, or video controls.

---

## The board, for a Notion program

Fetch the demo page, the board view and 1 card. Then look at the board in the founder's own logged-in
browser: when tools ending in `claude-in-chrome__navigate` and `claude-in-chrome__computer` exist, loaded
or deferred, open the link there and take 1 screenshot. Check that the last stage column is on screen
without scrolling sideways and that every card face reads. No such tools: say in 1 line that the board
was checked from its config and not seen, and ask for nothing.

- [ ] **The board comes first.** Under the name and promise lines comes the board. No `inline="false"`
      database link and no table sits on the page. When a calendar tab exists, the board is the first tab.
- [ ] **Every stage is a full column.** Count the cards in each Stage option. Fewer than 2 fails: Notion
      hides an empty stage, and 1 card per column reads as a template.
- [ ] **The card face shows the work.** The view's `displayProperties` lists Client and every other
      property the cards carry. `["Client"]` alone fails.
- [ ] **No half card.** Every card fills every property in the schema. An empty property on any card
      fails: get the fact, or drop the column.
- [ ] **Progress shows.** Every thing on a DONE line is a checked to-do on that client's card page, and
      This week is the first thing not done. A made-up board with every to-do unchecked fails unless
      every DONE line says none.
- [ ] **Their name and their promise are on the page**, word for word off `facts.md`.
- [ ] **Every stage has its page**, and every card's page links to it.
- [ ] **No property repeated as a text line** on a card's page. The DOES to-dos and the `Walks out with`
      line are the page's body and pass.
- [ ] **No `demo`, `test`, `sample board` or `template` word** in the page title, the view name or a
      heading.

---

## Generated images and the clip

For content and for website photos. Open every file and look at it twice: whole, then as 4 quarters at
full size, shot in the browser (`references/web-standard.md`, The look). Look hard at every object that
carries a maker's label in real life (a machine, an appliance, a box, equipment, packaging) and at every
edge of the frame. A fail in any quarter fails the piece, and every piece gets the same look. A clip is
not a picture, and its first frame is the start image that already passed: look at the clip at 1.5, 3
and 4.5 seconds in the browser, as the page shows it. Every item below runs on all 3 frames. A frame that
renders black: say in 1 line which part of the clip was not looked at.

- [ ] **Not THE PROBLEM.** Read THE PROBLEM on `squad/business.md`. A piece that shows what it complains
      about fails the set, even if everything else passes (stock photos: studio or dramatic light, a
      spotless room, a sharp professional look, a room that is not PLACE; bad or generic posts: a picture
      that could sit on any account in the trade).
- [ ] Phone look: real light, a real place, some grain. No studio backdrop, no glossy skin, the subject
      off the centre line.
- [ ] The place and the light match PLACE.
- [ ] Every piece shows the same room (walls, floor, the largest things in it, the door), and on content
      the same person (hair, clothes, build). 1 that reads as another room or another person fails.
- [ ] No face, judged on the piece as the page shows it (the 375px shots and the clip frames), never on
      the raw file: no eye, nose, mouth, cheek or jaw line in view. A sliver fails.
- [ ] Never from behind. Both shoulder blades facing the camera, the back of the head with the body
      turned away, or the seat turned to the camera fails, at any angle and whatever else is in the frame.
      A view from behind at an angle counts as from behind. There is no borderline: unsure is a fail.
- [ ] Content: WHOLE or CLOSE, as `references/shapes.md` sets for that piece, showing the TOPIC it
      carries. Website: a person is hands only, and the photo shows the room or the service it heads.
- [ ] Nothing in PLACE says something about the business: no certificate, sign, product, trophy or
      second person.
- [ ] No readable text, no melted letters, no sign, no logo, no watermark.
- [ ] Hands have 5 fingers. Nothing melts, bends, floats or doubles.
- [ ] No phone, no hand holding a phone, no app screen in the frame.
