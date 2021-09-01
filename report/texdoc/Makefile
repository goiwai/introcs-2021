.PHONY: all clean

LATEX_COMPILER = platex
LATEX_COMPILER_FLAGS = -interaction=errorstopmode -etex -src-specials -shell-escape
DVIPDF = dvipdfmx
DVIPDF_FLAGS = -V 6
FIGS = $(wildcard *.png)

all: report.pdf

report.pdf: report.tex $(FIGS)
	$(LATEX_COMPILER) $(LATEX_COMPILER_FLAGS) $<
	$(LATEX_COMPILER) $(LATEX_COMPILER_FLAGS) $<
	$(DVIPDF) $(DVIPDF_FLAGS) -o $@ $(basename $<).dvi

clean:
	$(RM) $(wildcard *.log) $(wildcard *.out) $(wildcard *.mw) $(wildcard *.toc) $(wildcard *.aux) $(wildcard *.dvi) $(wildcard *.blg) $(wildcard *.bbl) $(wildcard *.pdf)
