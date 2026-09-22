# The winner

Before the skeleton, the demo picks 1 winner and copies its shape. The words and the facts stay the
buyer's own, off `facts.md`. The shape is the winner's: which sections, in which order, what the first
screen does, where the proof sits, where the money action sits, how much is on the page. A demo built
on a generic style next to a winner with 8 sections and 3 kinds of proof reads as a template, and the
buyer has already seen the winner.

## Which winner, by shape

| THE SHAPE | The winner is | Found |
|---|---|---|
| website | the site the top seller in THE WINNERS shows as its work: its example, template or client site. None shown: the site of the top-reviewed business in the buyer's trade | the first block of THE WINNERS on `squad/business.md`, then its "our work", "examples", "portfolio", "templates" or "demo" link. None: WebSearch `<WHO line 1> <TOWN off facts.md>` (no TOWN: `<WHO line 1> website`) and take the business with the most Google reviews that has its own site, never a directory |
| content | the account in the buyer's trade with the most followers among the accounts THE WINNERS or WHO line 2 name. None: WebSearch `<trade> <CHANNEL>` and the top public account | its last 9 posts |
| consulting program | the program page of the top seller in THE WINNERS | the first block of THE WINNERS |
| software | the top seller in THE WINNERS itself: its product's screens on its site (the demo, features, screenshots or tour page) | the first block of THE WINNERS |

A website demo never copies an agency's own sales page: the buyer gets the shape of a site in his
trade. No `## THE WINNERS` on `squad/business.md` (a page written before this section existed): the
Found column's second path, and 1 line saying the offer page has no winners section.

## The read

1. `curl -sL --max-time 20 <url>`, the way A real run reads a page (`references/shapes.md`). Take the
   `<title>`, every `h1`, `h2` and `h3` in document order, every `<nav>` link text, every link or button
   that reads as an action (Book, Call, Get a quote, Start, Buy), every number a heading or a strong line
   carries (reviews, years, clients), the `theme-color` meta tag, any Google Fonts `<link>`, and the
   most used button colour, the way The lookup step 4 in `references/web-standard.md` reads them.
   Empty to curl: WebFetch once for the headings, and no colour or font is read.
2. Look at it. 2 shots of the live URL with the browser The look finds (`references/web-standard.md`):
   `--window-size=500,900` read as a 500px phone (Chrome lays a page out no narrower than 500px from the
   command line), and `--window-size=1280,800`, `--virtual-time-budget=8000`, `--screenshot` on the URL
   itself. Read off the shots what the headings cannot say: what the first screen is (words, a photo, a
   form), where the money action sits and what it says, what the proof looks like and where, how many
   sections come before the money section, whether there is a call bar. A URL that refuses the headless
   shot: read the headings alone and say so in 1 line.
3. Write `squad/demos/<business>/winner.md`:

```
# Winner · <name> · <url> · read <YYYY-MM-DD>

First screen: <what it is: the H1 in <n> words, the line under it, the button words, a photo or a form>
Money action: <the words, and where: a pinned bar, the hero, the bottom>
Proof: <what and where: "312 reviews and 4.8 stars under the H1", "3 logos over the footer", "none">
Sections, top to bottom:
1. <the section in 2 to 4 words, then what is in it, 1 line>
2. ...
Sections before the money action: <n>
Colour: <the accent hex off the CSS, or "not read"> · Fonts: <the Google Fonts families, or "not read">
Nav: <the link words, in order>
```

Content writes the post pattern instead: 1 line per post for the last 9 (the first line, the caption
length in words, the ask at the end, picture, carousel or clip), then
`Pattern: <the first line's move> · <n> words · <the ask> · <n> of 9 are clips`.
A program writes the stage count, the stage names, what each stage promises, and the length.
Software writes the screens the site shows: each one's title, what is on it, and which one it shows first.

Nothing in `winner.md` is a fact about the buyer, and nothing from it goes on the page as words. The
winner's words, numbers, names and photos never enter the demo. `winner.md` is a shape.

## The copy

- **Website.** The skeleton's sections are `winner.md`'s sections, in its order, each filled only from
  the `facts.md` fields the section map in `references/web-standard.md` allows. A winner section the
  map does not name (the work, before and after, a gallery, the team) gets a plain 1 to 3 word heading
  and is filled from the `facts.md` fields that fit it (PERSON N for a team, SERVICE N NOTE for the
  work). With none, it is dropped and goes first on the blanks line, in the winner's words for it, so
  the founder can give what the winner has. The first screen does what the winner's does: a form on
  the first screen when the winner has one there, the photo where the winner puts it, the proof line
  where the winner puts it. The money action sits where the winner's sits, and the call bar rule for
  the phone still wins. The paid-build test in `references/no-slop.md` counts against `winner.md`.
- **Content.** The set copies the pattern line: the first line of every caption makes the winner's
  move (a question, a number, a bare claim), the captions run the winner's length within 20%, the ask
  sits where the winner's sits, and the set has at least as many clips as the pattern says of 4.
- **Consulting program.** The board has the winner's stage count, within 1, and each stage's guides
  follow what the winner promises per stage. Stage names are the founder's own off `facts.md`, never
  the winner's.
- **Software.** The 3 screens are the winner's first 3 screens by job (the thing it shows first is
  screen 1), with the founder's records and words.

## The lookup, after the winner

The lookup in `references/web-standard.md` still runs, and `winner.md` wins where the 2 disagree: the
section order and count come from `winner.md`; the palette row comes from the buyer's own brand colour
first, else `winner.md`'s accent by the same colour-family rule, else the style's; the font pairing
comes from `winner.md` when its families match a `fonts.csv` row, else the style's. The trade row's
`Watch Out` and `Local Signals` still hold. Never a hex or a font typed from memory.

## The line printed

Once `winner.md` is written, before the skeleton, 1 line:
`Copying the shape of <name> (<url>): <n> sections, the first screen is <5 words>, the money action is <its words> <where>.`
