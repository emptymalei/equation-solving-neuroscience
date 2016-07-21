#
# I grabbed this Makefile from https://github.com/jrjohansson/scientific-python-lectures/blob/master/Makefile
# Modifications are made for our case
#
TEMPLATE=chapter
NOTEBOOKS=Lecture-0-Equation-Solving-in-Neuroscience.ipynb \
#          Lecture-6A-Fortran-and-C.ipynb Lecture-6B-HPC.ipynb \
          Lecture-1-Cable-Equation.ipynb

LATEXFILES=$(NOTEBOOKS:.ipynb=.tex)

.ipynb.tex:
	jupyter nbconvert --to latex --template $(TEMPLATE) $<

all: latexfiles buildpdf

latexfiles:
	for notebook in $(NOTEBOOKS) ; do \
		jupyter nbconvert --to latex --template $(TEMPLATE) $$notebook ; \
	done

buildpdf: latexfiles
	pdflatex Equation-Solving-in-Neuroscience.tex
