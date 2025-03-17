# Notes on Book Construction

## problems

* mentioning names / terms before concepts are introduced can cause
  issues (e.g. unwanted associations arise and may stick around)

  * are there practical alternatives?

    * [but how do it
      know](https://archive.org/details/jclarkscottbuthowdoitknowthebasicprinciplesofcomputersforeveryonejohnc.scott2009)
      seems to explore one path

* abstraction (e.g. definition statements) before examples can be a problem

  * related to previous point

  * worse is going too long without examples

  * how often is it practical to show motivating examples first and
    then name?

    * could it work to have a throw-away name temporarily?

    * could it work to use a description temporarily?

* author wants to touch on some subject but it may detract from main
  line of thought

  * footnote

  * parenthetical remark

  * appendix

  * side bar

  * explainer (may be)

  * etc.

* figure, table, diagram, code fragment, etc. not visible when needed

  * scrolling back doesn't solve the issue

  * opening a second copy can help, but can be tedious

  * wikipedia has the hovering preview feature - may work in some cases

  * making all figures, tables, diagrams, code fragment,
    etc. targetable by links may make it possible to "open in a new
    window"

* too many items in a single enumeration (irony of the current enumeration (^^; )

  * the magic number 7 +/- 2

  * clustering to reduce number of items below some threshold

  * however, too many "levels" may also be confusing

* advantages for sections having numbering

  * easily count number items in an enumeration

  * helps with memory

    * number AND prose (number -> prose association)

    * "gaps" when enumerating (mentally) might be more apparent

* too much unfamiliarity within a certain space (density)

  * spread things out?

* perception issues

  * spacing and formatting of code

  * highlighting of code

* "views" / "pages" that cannot be seen "all at once" seem harder to
  form a memory of compared to pages that "scroll" (cf. diagrams not
  visible point mentioned elsewhere)

  * examples

    * compare with trying to have a function's definition fit on a
      screen

    * compare with being able to see an overview on a single page

  * "paged" / "split" content

    * some advantages over "one big page"

      * easier to "resume"

      * easier to form an impression of something when you can see the
        whole thing at once

      * easier to "point" at (vs say "scroll down about 3/4 of the way
        through the whole thing" -- which may not make sense depending
        on screen sizes?)

    * potential issues

      * making things fit on individual pages is an additional
        (possibly unwanted) constraint

      * too many pages

* condescending / arrogant tone

  * can put people off which can reduce motivation to read as well as
    reduce the total audience

* for covering code, possibly taking inspiration from some of the
  design recipe stuff from htdp / plt folks might be good (cf. how
  "beautitful racket" doesn't seem to do this in-depth, though one
  might say there are some hints)

  * on a related note, when reading some code, starting at "the end"
    sometimes makes things easier to understand (cf. "begin with the
    end in mind").  this can help for functions as well as entire
    files.  "beautiful racket" may be could have applied this more,
    but to be fair, this kind of issue seems all too common across
    similar books, articles, etc.

* not being able to search the entirety of a book's content with a
  single command is not happy

## ideas

* nice to end up with some artifacts (code, notes, etc.) from the
  reading process.  having some artifacts that are being built while
  reading might help with momentum and motivation.  also might be good
  for review.  thus, suggestions from the reading material about how
  to prepare such artifacts along with the material being in alignment
  with producing such material might be good.

  * in htdp a fair bit of in-place changing one must do (e.g.
    defining something one way and then later being told to change the
    definition in the same buffer -- only one at a time works), but it
    is cumbersome to capture these bits (though git or similar can
    help).

  * in beautfiul racket, the jsonic stuff was awkward because there
    were multiple versions of the same thing and not much guidance
    about activating different versions via raco.

  * in dcic, being pushed toward using google's infrastructure to save
    stuff was unhappy.  trying to do stuff locally seemed quite
    suboptimal (but it's possible i don't yet know how to do it
    properly).

  * in all of the above material, it was cumbersome to copy the
    instructions / questions over to source files for reference.
    would have been nicer if the source files were already
    pre-populated (e.g. somewhat like what the koans repositories do).

* content segmentation / bite-size

  * recall the style in "the little schemer" -- multiple "segments"
    per page with no (or few?) segment(s) crossing a page boundary.
    point of focus is clear (single segment) and in total view (point
    about not crossing boundaries).  easier to think about what was
    important in a segment (vs content that spans pages).

* generate video "commentary"

  * one chapter per video with toc links to sections

  * see "content ideas" below for some details

* single screen / display friendly arrangements

  * book content in one browser, editor or another browser for code
    interaction in another.  in this kind of arrangement, might be
    good to consider how the code or editor might be able to arrange
    its panes.  in the dcic material, using pyret in a browser seems
    to require a left pane / right pane setup.  this seems to lead to
    some unhappiness if the book is in another browser window on the
    same screen as a natural arrangement is to have two browsers
    side-by-side, but this can lead to competition for horizontal
    space.

* glossary and "explainers"

  * glossary can be briefer

  * explainer can be more detailed - [used in sense of beautifulracket
    content](https://beautifulracket.com/#explainers) [1]

  * main content can refer to both

* dialogues

  * where and for what do "dialogues" work well?

  * speakers can emit questions which then may be seeds in the
    reader's mind.  priming.

* dark mode support (some pollen results don't turn out this way, but
  may be that's not a pollen issue per-se?)

* to the extent possible, make code in book automatically tested

* state concretely what version of various things are used for code in
  the book (e.g. janet language version) -- platform details might be
  good to have too?

* clickable plus signs that expand to a pop-up (beautifulracket has
  these)

* could "transitions" (say involving zooming and other effects) help
  with "memory" / "continuity" / "binding" / "association" of
  individual elements?

  * e.g. from an overall view, clicking on a "piece" transitioning via
    zooming to an "enlarged" (zoomed in?) view of that "piece" (have
    seen in some js presentations)

* suggestions to pause and consider at various points of the document
  (htdp and plai both do this)

* surprisingly, typing the code into an editor of one's choice seems
  to have made the content easier to understand.

* trying to recreate the code from scratch from memory also seems
  quite good.  doing this in an order that follows something like the
  design recipe also seems quite good (easier to recall it seems)

## needs

* good syntax highlighting

* good way to do diagrams (i.e. be able to express source of diagram
  using text?)

## content ideas / titles

* series of janet explainers

* janet by example

* just enough janet

* using gdb to observe janet stuff

* janet vm notes

* using janet's debugger and disassembly features

* commentary

  * parts that are/were hard to understand or confusing

    * resolutions if any

  * liked bits

  * outstanding questions

  * improvement suggestions

  * errata

---

[1] other folks have other ideas of what "explainer" means:

* https://medium.com/notes-from-the-classroom/how-to-create-a-good-explainer-explained-4e4236870b24
* https://www.seoforjournalism.com/p/explainers-news-seo
