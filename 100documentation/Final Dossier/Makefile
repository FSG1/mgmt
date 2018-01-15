file = main
output = `basename "$$PWD"`

all: woc

wc:
	pdflatex $(file)
	bibtex $(file)
	pdflatex $(file)
	pdflatex $(file)
	mv "$(file).pdf" "$(output).pdf"

woc:
	pdflatex $(file)
	pdflatex $(file)
	mv "$(file).pdf" "$(output).pdf"

count:
	texcount -merge -sum -total $(file).tex

clean:
	rm -f *.log *.lof *.lot *.toc *~ *.aux *.fls *.out *.bbl *.blg *.hst *.ver *.lol *.synctex.gz *.bcf *.run.xml $(file).pdf
	rm -f content/*.log content/*~ content/*.aux content/*.out
	rm -f base/*.log base/*~ base/*.aux base/*.out base/*.bbl base/*.blg
	rm -f appendix/*.log appendix/*~ appendix/*.aux appendix/*.out
