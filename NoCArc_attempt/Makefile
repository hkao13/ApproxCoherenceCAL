PAPER = approx_workload
PAPER_AUX = approx_workload.aux
TEX = $(wildcard *.tex)
BIB = ref.bib
FIGS = $(wildcard figures/*.pdf figures/*.png graphs/*.pdf graphs/*.png)

.PHONY: all clean

$(PAPER).pdf: $(TEX) $(BIB) $(FIGS) IEEEtran.cls
	echo $(FIGS)
	pdflatex $(PAPER)
	bibtex $(PAPER_AUX)
	pdflatex $(PAPER)
	pdflatex $(PAPER)

clean:
	rm -f *.aux *.bbl *.blg *.log *.out $(PAPER).pdf
