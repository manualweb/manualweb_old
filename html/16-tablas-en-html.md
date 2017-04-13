---
ID: 1386
post_title: 16 – Tablas en HTML
author: Víctor Cuervo
post_date: 2017-04-12 18:45:40
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/tablas-en-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-tabla/feed/
gitfolder: html
---
### ¿Qué son las tablas en HTML?

Las tablas es el elemento del lenguaje [HTML][1] que utilizaremos para mostrar información de forma agrupada. Ya sea texto, imágenes, vídeos,...

El [elemento table][2] será el que nos ayudará para crear las tablas en [HTML][1].

Un mal uso de las tablas en [HTML][1] es el motivo de maquetación, uso que se dió a las tablas en los principios del lenguaje [HTML][1]. Algo que hoy en día es una mala práctica. Cambiando por un modelo de maquetación apoyado en capas.

### Crear una tabla simple

Para crear una tabla vamos a necesitar conocer, al menos, tres elementos: [table][2], [tr][3] y [td][4]. Si bien existen otros cuantos que nos permitirán ampliar la funcionalidad de las tablas.

El primer elemento es [table][2]. [table][2] es el elemento que representa las tablas y será el que agrupe al resto de elementos. Por lo tanto tiene sus etiquetas de inicio y cierre.

~~~html
<table> … </table>
~~~

Siguiendo con la construcción de la tabla el siguiente elemento que necesitamos es [tr][3]. El [elemento tr][3] representa a una fila de la tabla. Por lo tanto tendremos tantos [elementos tr][3] como filas tenga la tabla.

Así, si queremos tener una tabla de tres filas tendremos un código como el que sigue:

~~~html
<table>
  <tr> … </tr>
  <tr> … </tr>
  <tr> … </tr>
</table>
~~~

El último elemento que necesitamos conocer es [td][4]. El [elemento td][4] es el que representa de una forma unitaria a una celda. Por lo tanto los [elementos tr][3] tendrán tantos [elementos td][4] en su interior como celdas contenga la fila.

El contenido que haya entre los [elementos td][4] será el contenido de la celda.

Una tabla de tres filas por cuatro columnas quedaría de la siguiente forma:

~~~html
<table>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
    <td>Fila 1 Columna 4</td>
  </tr>
  <tr>
    <td>Fila 2 Columna 1</td>
    <td>Fila 2 Columna 2</td>
    <td>Fila 2 Columna 3</td>
    <td>Fila 2 Columna 4</td>
  </tr>
  <tr>
    <td>Fila 3 Columna 1</td>
    <td>Fila 3 Columna 2</td>
    <td>Fila 3 Columna 3</td>
    <td>Fila 3 Columna 4</td>
  </tr>
</table>
~~~

Así con los tres elementos [table][2], [tr][3] y [td][4] tenemos construida nuestra tabla.

Visualmente tendríamos algo así:

<table borde="1" width="100%">
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
    <td>Fila 1 Columna 4</td>
  </tr>
  <tr>
    <td>Fila 2 Columna 1</td>
    <td>Fila 2 Columna 2</td>
    <td>Fila 2 Columna 3</td>
    <td>Fila 2 Columna 4</td>
  </tr>
  <tr>
    <td>Fila 3 Columna 1</td>
    <td>Fila 3 Columna 2</td>
    <td>Fila 3 Columna 3</td>
    <td>Fila 3 Columna 4</td>
  </tr>
</table>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:TABLE
 [3]: http://www.w3api.com/wiki/HTML:TR
 [4]: http://www.w3api.com/wiki/HTML:TD
