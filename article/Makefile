LATEX = latex
DVIPS = dvips
PSPDF = ps2pdf13 -sPAPERSIZE=a4 -dPDFSETTINGS=/prepress
PAPERNAME = p_mmz2022ijcai-camera-ready
OPTIONS = -shell-escape

.PHONY: 	clean
.PHONY:	okular
.PHONY:	edit


all:		$(PAPERNAME).tex
		pdflatex $(OPTIONS) $(PAPERNAME)	
		bibtex $(PAPERNAME)
		pdflatex $(OPTIONS) $(PAPERNAME)
		pdflatex $(OPTIONS) $(PAPERNAME)


clean:
	rm -f *~ *.aux *.bak *.flc *.log *.bbl *.blg *.dvi *.idx *.ilg *.ind *.lof *.lot *.not *.toc $(PAPERNAME).ps $(PAPERNAME).pdf *.nav *.out *.snm *.zip *.backup *.tdo *.abs

see:
	evince $(PAPERNAME).pdf &

edit:
	gedit *tex &

texstudio:
	texstudio $(PAPERNAME).tex &
