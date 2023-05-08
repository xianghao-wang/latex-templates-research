Let's call this version 1.00. :)
Just in case I make any changes at a later point...

A few notes about this:

- The presentation is written in a way that you can easily create a handout in which 4 slides
  are printed on one page. You just need to call the makefile with a different argument.

- If you work with overlays (e.g., tikz graphics that gradually expand), you will benefit from
  a special macro that allows to easily specify which slide number should go into the handout.
  For an explanation, open the AmnestyInternational.sty and search for "Fancy Handouts".

- The sty file (configured in a configuration file) supports one author as well as two authors
  (see the example PDFs). To choose one over the other, just set the argument of the package
  (called AmnestyInternational) accordingly.

- To compile it, just call the make script. Just "make" will compile only the standard slides
  multiple times, making sure all references are resolved correctly. Just compiling once might
  not do the job. You have those options:
  make 1on1: identical to just "make". see above
  make 1on1-quick: just compiles once. Much quicker, but references might be wrong.
  make 4on1: also a complete (long) compilation, but for the handout (4 on 1)
  make 4on1-quick: just compiles once, but for the handout.
  make all: 1on1 4on1
  make all-quick: 1on1-quick 4on1-quick

- If you have any ideas how this template (including its macros) or even
  its readme can be improved, just reach out to me.

Pascal
pascal.bercher@anu.edu.au
