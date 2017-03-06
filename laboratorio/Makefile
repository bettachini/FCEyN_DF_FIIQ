# Makefile para las guias de laboratorio.
#     - Permite compilar guia a guia o bien todas las guias.
#     - Elimina automaticamente los subproductos de la compilacion.
#
# Ultima modificacion: Victor Bettachini 02/17

all: 
	@make electrostatica
	@make ohm # No por ahora
	@make liquidos
	@make magnetismo
	@make induccion
	@make rc
	@make rlc
	@make yRLC
	@make cuerda
	@make acusticas
	@make interferencia
	@make difraccion
	@make redes
	@make polarizacion
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

electrostatica: electrostatica.tex
	latexmk -pdf electrostatica.tex
	@make clean

ohm: ohm.tex
	latexmk -pdf ohm.tex	
	@make clean

liquidos: liquidos.tex
	latexmk -pdf liquidos.tex
	@make clean

magnetismo: magnetismo.tex
	latexmk -pdf magnetismo.tex
	@make clean

induccion: induccion.tex
	latexmk -pdf induccion.tex
	@make clean

rc: rc.tex
	latexmk -pdf rc.tex
	@make clean

rlc: rlc.tex
	latexmk -pdf rlc.tex
	@make clean

yRLC: y_rlc.tex
	latexmk -pdf y_rlc.tex
	@make clean

cuerda: cuerda.tex
	latexmk -pdf cuerda.tex
	@make clean

acusticas: acusticas.tex
	latexmk -pdf acusticas.tex
	@make clean

interferencia: interferencia.tex
	latexmk -pdf interferencia.tex
	@make clean

difraccion: difraccion.tex
	latexmk -pdf difraccion.tex
	@make clean

redes: redes.tex
	latexmk -pdf redes.tex
	@make clean

polarizacion: polarizacion.tex
	latexmk -pdf polarizacion.tex
	@make clean

clean:
	@rm -f *.log *.aux *.bbl *.blg *.idx *.toc *.out *.fdb_latexmk *.fls *.pytxcode
	@rm -rf pythontex-files-Apunte_I_Diferencia_de_Fase

clean-all:
	@make clean
	@rm -f *.pdf 
