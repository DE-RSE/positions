TEX := pdflatex -halt-on-error

TEXDEPS := $(wildcard *.tex) $(wildcard *.bib)
FIGDEPS := $(wildcard ../figs/*)

all: manuscript.pdf

manuscript.pdf: manuscript.tex Makefile $(TEXDEPS) $(FIGDEPS)
	$(TEX) $< && bibtex manuscript && $(TEX) $< && $(TEX) $<

clean:
	rm -f *.aux *.log *.out *.bbl *.blg *.soc *.loc *.glo *.ist *.xwm *.fdb_latexmk *.fls *.synctex.gz *.nlo
	rm -f manuscript.pdf
