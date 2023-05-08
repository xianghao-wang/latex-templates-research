# author: Pascal Bercher
#         pascal.bercher@anu.edu.au
#         https://comp.anu.edu.au/people/pascal-bercher
#         https://bercher.net
# date: 14.9.2022
#

1on1Mainfile = mainfile-1on1
4on1Mainfile = mainfile-4on1
1on1 = "\\input{$(1on1Mainfile)}"
4on1 = "\\input{$(4on1Mainfile)}"

# time-consuming compilation: compile sufficiently
# often for references and label updates
1on1: 1on1-complete
1on1-complete:
	pdflatex -jobname=1on1 $(1on1)
	biber 1on1
	pdflatex -jobname=1on1 $(1on1)
	pdflatex -jobname=1on1 $(1on1)
	pdflatex -jobname=1on1 $(1on1)

# quick compilation: compile just once!
1on1-quick:
	pdflatex -jobname=1on1 $(1on1)

# time-consuming compilation: compile sufficiently
# often for references and label updates
4on1: 4on1-complete
4on1-complete:
	pdflatex -jobname=4on1 $(4on1)
	biber 4on1
	pdflatex -jobname=4on1 $(4on1)
	pdflatex -jobname=1on1 $(1on1)
	pdflatex -jobname=4on1 $(4on1)

# quick compilation: compile just once!
4on1-quick:
	pdflatex -jobname=4on1 $(4on1)

# do everything! But sufficiently often
all: all-complete
all-complete: 1on1-complete 4on1-complete

# do everything! But quickly
all-quick: 1on1-quick 4on1-quick

clear: clean
clean:
	-rm -f *.aux *.log *.dvi *.ps *.nav *.out *.snm *.backup *.bak *.toc *~ *.bbl *.blg *.toc *.run.xml *-blx.bib *.bcf *.synctex.gz *.vrb *.pdfpc *.fls *.fdb_latexmk *.tce
