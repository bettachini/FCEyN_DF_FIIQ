# Makefile para las guias de laboratorio.
#     - Permite compilar guia a guia o bien todas las guias.
#     - Elimina automaticamente los subproductos de la compilacion.
#
# Pablo Cobelli - Ultima modificacion: Enero de 2016

all: 
	@make G01
	# @make G02 # No por ahora
	@make G02b
	@make G03
	@make G04
	@make G05
	@make G06
	@make G07
	@make G08
	@make G09
	@make G10
	@make G11
	@make G12
	@echo " "
	@echo "Todas las guias fueron compiladas con exito."
	@make clean

A01: Apunte_I_Diferencia_de_Fase.tex
	# (!) NOTA: 
	#     Requiere tener instalado PythonTex; ya que los graficos son
	#     generados por python on-the-fly.
	pdflatex Apunte_I_Diferencia_de_Fase.tex
	pythontex Apunte_I_Diferencia_de_Fase.tex
	pdflatex Apunte_I_Diferencia_de_Fase.tex
	@make clean

G01: Guia_01_Electrostatica.tex
	latexmk -pdf -silent Guia_01_Electrostatica.tex
	@make clean

G02: Guia_02_Ley_de_Ohm.tex
	latexmk -pdf -silent Guia_02_Ley_de_Ohm.tex
	@make clean

G02b: Guia_02b_Conduccion_Liquidos.tex
	latexmk -pdf -silent Guia_02b_Conduccion_Liquidos
	@make clean

G03: Guia_03_Magnetismo.tex
	latexmk -pdf -silent Guia_03_Magnetismo.tex
	make clean

G04: Guia_04_Induccion.tex
	latexmk -pdf -silent Guia_04_Induccion.tex
	make clean

G05: Guia_05_Circuito_RC.tex
	latexmk -pdf -silent Guia_05_Circuito_RC.tex
	make clean

G06: Guia_06_Circuito_RLC.tex
	latexmk -pdf -silent Guia_06_Circuito_RLC.tex
	make clean

G07: Guia_07_Ondas_en_una_cuerda.tex
	latexmk -pdf -silent Guia_07_Ondas_en_una_cuerda.tex
	make clean

G08: Guia_08_Ondas_Acusticas.tex
	latexmk -pdf -silent Guia_08_Ondas_Acusticas.tex
	make clean

G09: Guia_09_Interferencia.tex
	latexmk -pdf -silent Guia_09_Interferencia.tex
	make clean

G10: Guia_10_Difraccion.tex
	latexmk -pdf -silent Guia_10_Difraccion.tex
	make clean

G11: Guia_11_Redes_de_difraccion.tex
	latexmk -pdf -silent Guia_11_Redes_de_difraccion.tex
	make clean

G12: Guia_12_Polarizacion.tex
	latexmk -pdf -silent Guia_12_Polarizacion.tex
	make clean

clean:
	@rm -f *.log *.aux *.bbl *.blg *.idx *.toc *.out *.fdb_latexmk *.fls *.pytxcode
	@rm -rf pythontex-files-Apunte_I_Diferencia_de_Fase

clean-all:
	@make clean
	@rm -f *.pdf 
