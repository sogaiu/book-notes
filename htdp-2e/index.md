# Notes on How to Design Programs Second Edition (htdp-2e)

## liked

* clear and detailed

* recipes and iterative refinement

* hints for skipping, reading ahead, coming back, revisiting previous
  bits, etc.

* explicit attempts to get a reader to pause (e.g. "Stop!" followed by
  suggested action)

## not so much

* didn't work so well in parts with darkreader :(

  * [here](https://htdp.org/2024-11-6/Book/part_prologue.html), the
    bit after

      > the teacher wants to see something like this:

      is (was) not visible

* "assuming" text

    > When you were a small child, your parents taught you to count
    > and perform simple calculations with your fingers: “1 + 1 is 2”;
    > “1 + 2 is 3”; and so on.

    via: https://htdp.org/2024-11-6/Book/part_prologue.html

    one problem with this kind of thing is that it's distracting

    > So here is what you learned in this section. Functions are
    > useful because they can process lots of data in a short time.

    via: https://htdp.org/2024-11-6/Book/part_prologue.html

* tone in parts feels condescending - similar problem ("distracting")
  to the "assuming" bit above

* default "affordances" (e.g. no dynamic abbrev style completion)
  doesn't help from an ergonomics perspective

  * working with images (frequent copy-and-pasting) felt laborious

    * may be there's a better way?

* if you're going to the trouble of including images as well as
  different customized languages, why not also make graphical
  coordinates match expectations (i.e. why make y = 0 be at the top of
  the screen?)

* the "exercises"
  [here](https://htdp.org/2024-11-6/Book/part_prologue.html#(part._pro-many-def))
  were ok, but it seemed like looking up info that wasn't introduced
  yet was needed (e.g. existence of `overlay/align`; `empty-scene` can
  take a third argument, etc.).  didn't see a hint in the text (near
  the "exercises" anyway) about looking stuff up and it might have
  been nice.  that seems like the kind of thing programmers /
  developers are going to have to do, so bringing the point up
  repeatedly (at least early on) seems like it would be helpful.

* the instructions at various points regarding whether to start a new
  tab and/or modifying existing code seem weak and inconsistent.  on
  more than one occasion it was easy to have cluttered / confused
  content.  the prologue was the place this was noticed first (may be
  the rest of the book is better?)

* some instructions seemed somewhat inappropriate, e.g.

    > We picked our way through the alphabet just to show the variety
    > of operations. Explore what they compute, and then find out how
    > many more there are.

    via: https://htdp.org/2024-11-6/Book/part_one.html#(part._sec~3aarith-num)

    if you tried to do this, it would take quite some time.  for such
    a potentially time-consuming endeavor, the instructions seemed
    off.  for reference, i did it across several sittings.  it took
    more than a few minutes.  there seemed to be errors in the docs as
    well.

* if recipes and design are so important, why does it take so long to
  get to actually seeming them in action?  matthew flatt (one of the
  authors) has short videos showing the use of recipes,
  e.g. [here](https://www.youtube.com/watch?v=4Jz6D5ekBT8).  jumping
  right in to give folks a concrete idea sooner seems like a better
  approach to me.

* terms and phrases that were not easy to find elsewhere (actually
  have not succeeded in finding some either):

  * "garage programming" - chapter 3
  * "programming product" - chapter 3

## trivia

* there were some imperative bits in the 1st edition; some [advice
  from
  felleisen](https://racket.discourse.group/t/am-i-barking-up-the-wrong-tree-with-htdp/1169/4)
  in response to a query from an experienced developer: reading 2nd
  edition, then parts of the 1st edition that were removed might work
  to fill in some imperative gaps.

## some quotes

> Good programming is far more than the mechanics of acquiring a
> language. Most importantly, it is about keeping in mind that
> programmers create programs for other people to read them in the
> future. A good program reflects the problem statements and its
> important concepts. It comes with a concise
> self-description. Examples illustrate this description and relate it
> back to the problem. The examples make sure that the future reader
> knows why and how your code works. In short, good programming is
> about solving problems systematically and conveying the system
> within the code. Best of all, this approach to programming actually
> makes programming accessible to everyone — so it serves two masters
> at once.

via: https://htdp.org/2024-11-6/Book/part_prologue.html#(part._sec~3anot)

> A purpose statement is a BSL comment that summarizes the purpose of
> the function in a single line. If you are ever in doubt about a
> purpose statement, write down the shortest possible answer to the
> question
>
> what does the function compute?

via: https://htdp.org/2024-11-6/Book/part_prologue.html#(part._sec~3anot)

> Every reader of your program should understand what your functions
> compute without having to read the function itself.

Note that providing illustrative examples might be an alternative
method of imparting understanding in some cases.

via: https://htdp.org/2024-11-6/Book/part_one.html#(part._sec~3adesign-func)

> A multi-function program should also come with a purpose
> statement. Indeed, good programmers write two purpose statements:
> one for the reader who may have to modify the code and another one
> for the person who wishes to use the program but not read it.

Two?  Haven't come across this being done, but perhaps later in the
book?

via: https://htdp.org/2024-11-6/Book/part_one.html#(part._sec~3adesign-func)

> Our parameter names reflect what kind of data the parameter
> represents. Sometimes, you may wish to use names that suggest the
> purpose of the parameter.

via: https://htdp.org/2024-11-6/Book/part_one.html#(part._sec~3adesign-func)

> As this signature points out, introducing a data definition as an
> alias for an existing form of data makes it easy to read the
> intention behind signatures.
>
> Nevertheless, we recommend that you stay away from aliasing data
> definitions for now. A proliferation of such names can cause quite a
> lot of confusion. It takes practice to balance the need for new
> names and the readability of programs

via: https://htdp.org/2024-11-6/Book/part_one.html#(part._sec~3adesign-func)

## recipe-related

* brief summary of initial version

  1. Express how to represent information as data.  Formulate data
     definitions, for the classes of data you consider relevant for
     the design of your program.

  2. Write down a signature, a purpose statement, and a function header / stub.

  3. Illustrate the signature and the purpose statement with some
     functional examples.

  4. Take inventory, to understand what are the givens and what we
     need to compute (as function template)

  5. Replace the body of the function (template) with an expression
     that attempts to compute from the pieces in the template what
     the purpose statement promises.

  6. Test the function on the examples that you worked out
     before. (fix if needed)

* commentary on steps

  1. "information" is "out of your program / process" stuff, while
     "data" is what that stuff "maps" to "in your program".  there may
     not be a single correct mapping / inversion (i.e. info -> data
     and data -> info).  the mapping(s) may not be obvious.  it could
     be that revisiting / refining one's current mapping(s) could lead
     to improvements.  it might be that coming up with and examining
     concrete examples could help in this process.  it may not be the
     case that the programming language has "types" that capture
     exactly what is desired for the function's inputs and output(s)
     (e.g. there is typically no built-in support for even numbers;
     also see clojure's spec system).

  2. in many cases, the function is likely to need a name, so at least
     some initial version may need to be settled on.  specific details
     about inputs and output(s) need to be decided on as well (in
     order for code to execute).  a purpose statement gives another
     view (in human language) of what the function is supposed to
     accomplish.  the function stub gives an opportunity at
     externalizing details which can then be perceived instead of just
     imagined.

  3. to express examples (which will eventually be executed), some
     amount of step 2 needs to be carried out.  examples are
     externalizations of specific invocations along with the
     corresponding expected output(s).  typical invocations and
     "border" / "edge" / "corner" cases can be illustrated via
     examples.  the process of spelling these out may reveal errors or
     unnoticed bits from steps 1 and/or 2.

  4. a certain amount of the structure of the function(s) may be
     determined / guided based on the structure of the inputs and
     outputs of the function.  these "constraints" can be expressed in
     the function template.  in many cases, the template can make the
     remaining "fill in the blank" work easier, though it may be good
     to have the "rainfall problem" in mind.

  6. the implementation needs to be completed before the tests can be
     executed.

  7. testing can generate evidence regarding whether the
     implementation behaves as expected, though the tests themselves
     being code may also contain errors.

## misc

* [matthias felleisen's slides from racketcon
  2011](https://con.racket-lang.org/2011/matthias-slides.pdf)

