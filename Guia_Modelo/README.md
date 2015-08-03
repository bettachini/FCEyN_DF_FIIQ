Como componer una guia con este modelo
--------------------------------------

En primer lugar es necesario hacer una copia local de los archivos de formato
especificos. El archivo `tex` de la guia debe componerse siguiendo los 
lineamientos generales descriptos a continuacion.

Declaraciones iniciales
-----------------------

El documento `tex` esta encabezado por la eleccion de la clase asociada,
en este caso

    \documentclass[laboratorio]{clase_guias}

para generar una guia de laboratorio. Para generar una guia de problemas, la
opcion es 

    \documentclass[problemas]{clase_guias}

Definiendo el titulo y numero de la guia
----------------------------------------

El numero de la guia practica se especifica haciendo

    \def \practnum {5}

si se desea especificar que se trata de la guia numero 5. 

El titulo completo de la guia se especifica mediante el comando

    \def \practica {Frecuencia de resonancia de un circuito RLC}

La clase provee la posibilidad de declarar un titulo alternativo mas corto,
que sera utilizado automaticamente si, al procesar el documento, el compilador
de LaTeX detecta que el titulo completo es demasiado largo para el encabezado
(header) de pagina. Para suministrar la version 'corta' del titulo, basta 
con declarar 

    \def \practcur {Circuito RLC}

Estas definiciones se realizan **antes** de introducir el 
`\begin{document}`. 

Definiendo el objetivo y las tematicas  de la guia
--------------------------------------------------

**Luego** del `\begin{document}` y **antes** del `\maketitle` de rigor, 
la definicion del objetivo de la guia y de las tematicas en ella abordadas se
realiza mediante:

    \objetivo{Medir la frecuencia de resonancia de un circuito RLC. 
              \tematicas{Resonancia, circuito RLC} }

Observense dos cosas:
- `\tematicas` queda definido **dentro** de `\objetivo`. 
- El argumento de tematicas no requiere de punto final.

Habiendo definido el objetivo y las tematicas, puede pedirse la construccion
del titulo mediante el comando usual `\maketitle`.

Acerca del cuerpo de la guia
----------------------------

A continuacion el cuerpo de la guia se define en la forma usual, y se dispone
de todos los comandos de LaTeX habituales: `\begin{section}`, etc.  

Incorporar la bibliografia sugerida o de referencia
---------------------------------------------------

La bibliografia sugerida o de referencia puede incorporarse al final del 
cuerpo de la guia, aun cuando dichas referencias no hayan sido citas 
explicitamente en el cuerpo. Esto se logra haciendo

    \nocite{Alonso1998, Crawford1994, Purcell1988}

Ya sea que se utilice esta forma o la usual `\cite{Alonso1988}` en el texto,
la inclusion de la bibliografia se hace en la forma usual mediante

    \bibliographystyle{babunsrt}
    \bibliography{Referencias}

La primera linea emplea el estilo bibliografico `babunsrt`, asociado al 
paquete `babelbib`, que permite customizar el texto de la bibliografia a
cualquier idioma (en este caso, el español). El estilo `babunsrt` es el 
equivalente del `unsrt` estandar. 

Finalmente, la segunda linea apunta al archivo `Referencias.bib` que lista
y nuclea **todas** las referencias asociadas a la totalidad de las guias.

Entornos adicionales provistos por la clase
-------------------------------------------

Hasta el momento la clase provee los siguientes entornos adicionales, 
- `problema`
- `sabermas`

sabermas
--------
La idea es emplear este entorno para motivar al estudiante a leer conceptos
mas avanzados asociados a esta guia. Para hacer uso del entorno, se emplea la
construccion habitual

    \begin{sabermas}
    ...
    \end{sabermas}

problema
--------
Este entorno sirve para las guias de problemas. Admite ademas un campo
de titulo para el ejercicio. La sintaxis es:

    \begin{problema}{Titulo del problema (opcional)}
        Un auto se mueve a 10 km/h. Calcule la distancia que habra recorrido
        en 1 hora. 
    \end{problema}






