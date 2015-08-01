# Makefile para las guias de laboratorio.
#     - Permite compilar guia a guia o bien todas las guias.
#     - Elimina automaticamente los subproductos de la compilacion.
#
# Pablo Cobelli - Ultima modificacion: Agosto de 2015

all: 
	@make G01
	@make G11
	@echo " "
	@echo "Todas las guias fueron compiladas con exito."
	@make clean
	
G01: Guia_01_Electrostatica.tex
	pdflatex Guia_01_Electrostatica.tex

G02: Guia_02_Ley_de_Ohm.tex
	pdflatex Guia_02_Ley_de_Ohm.tex

G03: Guia_03_Magnetismo.tex
	pdflatex Guia_03_Magnetismo.tex

G04: Guia_04_Induccion.tex
	pdflatex Guia_04_Induccion.tex

G05: Guia_05_Circuito_RC.tex
	pdflatex Guia_05_Circuito_RC.tex

G06: Guia_06_Circuito_RLC.tex
	pdflatex Guia_06_Circuito_RLC.tex

G07: Guia_07_Ondas_en_una_cuerda.tex
	pdflatex Guia_07_Ondas_en_una_cuerda.tex

G08: Guia_08_Ondas_acusticas.tex
	pdflatex Guia_08_Ondas_acusticas.tex

G09: Guia_09_Interferencia.tex
	pdflatex Guia_09_Interferencia.tex

G10: Guia_10_Difraccion.tex
	pdflatex Guia_10_Difraccion.tex

G11: Guia_11_Redes_de_difraccion.tex
	pdflatex Guia_11_Redes_de_difraccion.tex

G12: Guia_12_Polarizacion.tex
	pdflatex Guia_12_Polarizacion.tex

clean:
	@rm -f *.log *.aux *.bbl *.blg *.idx *.toc *.out

clean-all:
	@rm -f *.pdf *.log *.aux *.bbl *.blg *.idx *.toc *.out
