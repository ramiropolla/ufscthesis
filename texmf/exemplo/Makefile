NAME=tutorial

all: $(addsuffix .pdf,$(NAME))

%.pdf: %.tex
	pdflatex -halt-on-error $<
	bibtex $(<:.tex=.aux)
	pdflatex -halt-on-error $<
	pdflatex -halt-on-error $<

clean::
	rm -f $(addsuffix .aux,$(NAME))
	rm -f $(addsuffix .log,$(NAME))
	rm -f $(addsuffix .las,$(NAME))
	rm -f $(addsuffix .lof,$(NAME))
	rm -f $(addsuffix .lot,$(NAME))
	rm -f $(addsuffix .lsb,$(NAME))
	rm -f $(addsuffix .toc,$(NAME))
	rm -f $(addsuffix .pdf,$(NAME))
	rm -f $(addsuffix -blx.bib,$(NAME))
	rm -f $(addsuffix .bbl,$(NAME))
	rm -f $(addsuffix .blg,$(NAME))
	rm -f *~
