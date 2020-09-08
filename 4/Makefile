PROJ=proj4

$(PROJ).pdf: $(PROJ).ps
	ps2pdf $(PROJ).ps

$(PROJ).ps: $(PROJ).dvi
	dvips -sPAPERSIZE=a4 $(PROJ).dvi

$(PROJ).dvi: $(PROJ).tex $(PROJ).bib
	latex $(PROJ).tex
	bibtex $(PROJ).aux
	latex $(PROJ).tex
	latex $(PROJ).tex


xlazor02.tar.gz:
	tar -czvf xlazor02-fit.tar.gz $(PROJ).tex $(PROJ).bib Makefile czechiso.bst

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps $(PROJ).out $(PROJ).bbl $(PROJ).blg

pack: xlazor02.tar.gz