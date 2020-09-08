PROJ=proj2

$(PROJ).pdf: $(PROJ).ps
	ps2pdf $(PROJ).ps

$(PROJ).ps: $(PROJ).dvi
	dvips -sPAPERSIZE=a4 $(PROJ).dvi

$(PROJ).dvi: $(PROJ).tex
	latex $(PROJ).tex
	latex $(PROJ).tex

xlazor02.tar.gz:
	tar -czvf xlazor02-fit.tar.gz $(PROJ).tex Makefile

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps $(PROJ).out

pack: xlazor02.tar.gz