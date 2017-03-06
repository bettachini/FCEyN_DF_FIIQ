Acerca de las guias
===================

Guias de Laboratorio
--------------------
Estas guias de laboratorio estan escritas en LaTeX. 

Listado de guias disponibles
----------------------------

- electrostatica: campo eléctrico en cuba.
- liquidos: conducción en cuba electrolítica con NaCl.
- ohm: Circuitos de corriente continua, curvas I-V, leyes de Ohm, Kirchhoff, Thévenin.
- magnetismo: leyes de Ampère y de Biot-Savart.
- induccion: fuerza electromotríz inducida y ley de Faraday.
- rc: transitorios de carga y descarga de un circuito RC.
- rlc: resonancia en serie y paralelo.
- cuerda: ondas estacionarias en una cuerda.
- acusticas: tubo de Kundt.
- interferencia: biprisma de Fresnel.
- difraccion: aberturas, obstaculos.
- redes: de difraccion, espectro de la lampara de sodio.
- polarizacion: ley de Malus, polarización por reflexión.


Acerca del nuevo diseño de figuras
----------------------------------
Lo que sigue son unos lineamientos generales para la reformulacion de las
figuras asociadas a las guias de laboratorio.

- Figuras en formato vectorial.
- Los medidores de magnitudes electricas (voltimetro, amperimetro, etc.)
  que aparecen en las figuras deben dibujarse en forma esquematica de acuerdo
  a su funcionalidad y **no** a su apariencia fisica. 
- Figuras simples ocupan una sola columna; figuras con complejidad media a alta
  ocupan todo el ancho del texto.
- Las figuras asociadas a diagramas circuitales son confeccionadas con
  `circuitikz`.

Acerca de la bibliografia de referencia
---------------------------------------

La bibliografia de referencia esta listada en el archivo `Referencias.bib` que 
es comun a todas las guias. Toda referencia adicional debera cargarse en dicho 
archivo.


Como compilar estas guias manualmente
-------------------------------------

Los comandos para procesar *manualmente* estas guias con LaTeX 
son los habituales: `pdflatex` y `bibtex`. Opcionalmente, puede utilizarse el
comando 

    latexmk -pdf -silent Nombre_de_la_guia.tex

que compila con tantas pasadas de `pdflatex` y `bibtex` como sea necesario. 
Esta es la estrategia utilizada para compilar automaticamente las fuentes 
(ver a continuacion).

Compilacion automatica de las guias usando Makefile
---------------------------------------------------

Las guias pueden compilarse en forma automatica usando el Makefile 
disponible junto con las fuentes.

El comando para compilacion de una unica guia, supongamos la numero 4, es:

    make G04

notese el cero antepuesto al cuatro. Para compilar la guia 10 hacemos

    make G10

Si se desean compilar todas las guias, el comando es:

    make all


Como citar la bibliografia de referencia
----------------------------------------

Para citar fuentes bibliograficas en el listado de referencias (al final de 
la guia) sin haberlas citado explicitamente en el cuerpo de la guia, incluir
el comando

    \nocite{codigo_referencia}

donde `codigo_referencia` es el *key* hacia la referencia deseada, que debe
existir en el archivo de bibliografia. Este comando debe incluirse en la 
fuente `tex` **antes** del llamado a la bibliografia. Varias citas pueden
incluirse utilizando el mismo comando, separando las *keys* con comas. 
Cabe recordar que 

    \nocite{*}

tiene el efecto de citar todas las referencias bibliograficas disponibles en el
archivo `Referencias.bib`.

Bibliografia para las guias de laboratorio
------------------------------------------
- Purcell, Electricidad y magnetismo.
- Crawford, Ondas.
- Alonso & Finn, Fisica.
- Jenkins & White, Fundamentals of optics.
- Hetch & Zajac, Optica.
- Rodriguez Trelles, Temas de electricidad y magnetismo.
- Reitz, Milford & Christy, Fundamentos de la teoria electromagnetica.
- Sears, Ford & Freedman, Fisica universitaria. 
