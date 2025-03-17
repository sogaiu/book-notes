# Notes on A Data Centric Introduction to Computing (DCIC)

## liked

* focus on examples

    > For our purposes, we are writing examples as part of the process
    > of making sure we understand the problem. It’s always a good
    > idea to make sure you understand the question before you start
    > writing code to solve a problem. Examples are a nice
    > intermediate point: you can sketch out the relevant computation
    > on concrete values first, then worry about turning it into a
    > function. If you can’t write the examples, chances are you won’t
    > be able to write the function either. Examples break down the
    > programming process into smaller, manageable steps.

    via: [3.3.4 Documenting Functions with Examples](https://dcic-world.org/2025-02-09/From_Repeated_Expressions_to_Functions.html#(part._writing-examples))

* "do now!" boxen (and they are clearly visible)

* exercise boxen (and they are clearly visible)

* ability to use via web page

* error messages seemed pretty decent

* going over some of the error message content

* clear explanation of difference between expression and statement (e.g. definition)

* [creating functions from
  expressions](https://dcic-world.org/2025-02-09/From_Repeated_Expressions_to_Functions.html#(part._defining-functions)) -
  starting with concrete examples is nice (ambivalent about the type
  part; expressing info about the input and output values seems good,
  but whether that should be in the form of "types"...(cf. spec))

* [documenting functions with
  examples](https://dcic-world.org/2025-02-09/From_Repeated_Expressions_to_Functions.html#(part._writing-examples)) -
  very nice to have this kind of thing built in

## mixed

* for htdp-experienced folks, the similarities of some of the
  functions (e.g.  `circle(25, "solid", "red")` -- parameters and
  order of them seems the same as in htdp) can be nice, but the
  constant having to specify "solid" seems unnecessarily verbose.

* discussion of how one might use documentation seemed
  well-intentioned and had some good bits, though some of the
  instructions seem tedious or vague:
  * "Scroll down until you see “rectangle” in the sidebar" - alternate
    instructions for searching seemed more appropriate
  * "Scroll down a bit further, and you’ll see a list of functions for
    composing and manipulating images." - does not use actual terms
    that appear in the left pane so one may be left guessing,
    "composing and manipulating images" is not concrete enough of a
    target imo

* dark-mode seems to work mostly, but there is stuff like references
  to "shaded area" which though visible are not the most noticeable

## not so much
* some dark-mode unfriendly bits

  * screenshots

  * functions like `frame` which seem to only draw black borders

* node-based for local use

* local version felt quite slow - may be pilot error?

* that web version's persistence features rely on authentication with
  google is a big meh

* ergonomics of web version has rough edges (will try to list as they
  come up)

  * found the clicking on "run" clearing the interactions pane with no
    warning to be not great

* prefer a top pane / bottom pane arrangement over the left pane /
  right pane default(?)

  * given that the book might often be read in a browser, it seems
    reasonable that a common arrangement would be to have two browser
    windows, one for the text and one for pyret.  it also seems
    reasonable to have the two browser windows arranged so that one is
    on the left and the other on the right.  having two panes for
    pyret where one is on the left and the other on the right seems
    like it can lead to competition between the two browser windows
    for horizontal space.  if the panes in pyret could be instead one
    on top and the other on the bottom (like in dr racket's default
    setup), this "pressure" might be alleviated?

* `::` use in type info felt quite verbose.  probably wanted to use
  `:` but due to python similarity constraints, went with double?

* completion would be nice for things that have already been typed at
  least once (think dabbrev-expand from emacs)

* not detailed enough sometimes, e.g.

    > For now, remember that the names you associate with values using
    > = cannot contain quotation marks, while word- or text-based data
    > must be wrapped in double quotes.

  also giving explicit examples seems like this would illustrate the points better.

* vague (and demotivating for folks who thought of many examples)
  exercises

    > Find the characteristics of tabular data in the other examples
    > described above, as well as in the ones you described.

  via: https://dcic-world.org/2025-02-09/intro-tabular-data.html

  would have liked to have seen an example worked out (or pointed to).

## questionable

* in 3.1.6.2 there is this:

    > Use the functions we have learned so far to create an image of
    > the Armenian flag. You pick the dimensions (we recommend a width
    > between 100 and 300).
    >
    > Make a list of the questions and ideas that occur to you along the way.

  trying to do both of these things at the same time seems problematic.  did the first part of
  the exercise a second time and it was easier to think of questions and ideas:

  * expression is way too long and complex (too easy to get wrong,
    hard to read, doesn't fit so well in interactions pane (the right
    pane), ...)

  * might be nicer to be able to name the parts (e.g. each rectangle)

  * having to nest calls to `above` felt more complicated than necessary

  * hard-wiring the dimensions and colors means making changes later
    might be error-prone and tedious

  * not being able to vary parameters in real-time to see the results
    seems to discourage tweaking

* in 3.4.3.2, there is an exercise that says:

    > Explain why numbers and strings are not good ways to express the
    > answer to a true/false question.

  it's unclear to me whether every one will agree about the assumed
  premise of this question.

## tips

* can make right pane in web-based ui wider by dragging the "divider"
  between the left and right panes (to the left).  this can be helpful
  for perception of entered code in some cases.

