REPORT=paper1
LATEX=pdflatex
DVIPS=dvips
PS2PDF=ps2pdf
ACROREAD=open
BIBTEX=bibtex
RMTEX=rm -f *.dvi *.aux *.log *.ps *.blg 

SRCS=$(wildcard *.tex)
REFS=$(wildcard *.bib)
FIGS=$(wildcard FIGURES/*)

all: $(REPORT).pdf

$(REPORT).pdf: $(SRCS) $(REFS) $(FIGS) 
	$(LATEX) $(REPORT)
	$(BIBTEX) $(REPORT)
	$(LATEX) $(REPORT)
	$(LATEX) $(REPORT)
	$(ACROREAD) $(REPORT).pdf &

pdf: $(REPORT).pdf

