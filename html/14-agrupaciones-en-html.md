---
ID: 1374
post_title: 14 – Agrupaciones en HTML
author: Víctor Cuervo
post_date: 2017-04-12 18:39:26
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/agrupaciones-en-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-capas/feed/
gitfolder: html
---
Hasta ahora hemos visto cómo insertar diferentes elementos sobre un documento [HTML][1]. Estos elementos se irán mostrando según la secuencia en la que hayamos escrito el documento [HTML][1].

Una de las cosas que tenemos que saber de los elementos html es si son elementos de bloque o elementos de línea.

Un **elemento de bloque** es aquél que una vez utilizado aparece en la siguiente línea y ocupa todo el ancho. Elementos de tipo bloque son los [párrafos p][2], los [formularios form][3], o [las cabeceras hx][4].

Un **elemento en línea** es aquel que se muestra justo a continuación del anterior elemento. Estos elementos serían los [enlaces a][5], [imágenes img][6],...

El lenguaje [HTML][1] nos permite agrupar un conjunto de elementos mediante una agrupación en bloque o una agrupación en línea.

### Agrupaciones en Bloque

Un elemento en bloque siempre empieza con una línea y su tamaño será igual al ancho disponible. El ancho disponible inicialmente es el de la página.

El elemento que nos permite realizar agrupaciones en bloque es el [elemento div][7] o más conocidos como capas. La estructura del [elemento div][7] es:

~~~html
<div>
<!-- Contenido de la Capa -->
</div>
~~~

Los elementos en bloque pueden contener a otros elementos en bloque o bien a otros elementos en línea.

Por ejemplo podríamos agrupar en un bloque el siguiente contenido.

~~~html
<div id=”micapa”>
  <h2>Título del Contenido</h2>
  Este es el contenido del artículo
  <img src=”logo.jpg” />
  <p>Más contenido del artículo</p>
</div>
~~~

### Agrupaciones en Línea

Para poder realizar agrupaciones en línea tenemos el [elemento span][8]. La estructura del [elemento span][8] será:

~~~html
<span> <!-- Contenido --></span>
~~~

Las agrupaciones en línea sólo pueden contener a otros elementos en línea, no a elementos de tipo bloque.

Por ejemplo podríamos tener la siguiente agrupación en línea.

~~~html
<span id=”entrada”>
  <strong>Articulo Nuevo</strong>,
  <em>,12 de marzo de 2016</em>
</span>
~~~

Es muy normal que los agrupadores, ya sean o bien [div][7], o bien [span][8] lleven el [atributo id][9] o [class][10], ya que a posteriori serán manipulados mediante [hojas de estilo CSS][11] utilizando dichos identificadores.

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:P
 [3]: http://www.w3api.com/wiki/HTML:FORM
 [4]: http://www.w3api.com/wiki/HTML:H1
 [5]: http://www.w3api.com/wiki/HTML:A
 [6]: http://www.w3api.com/wiki/HTML:IMG
 [7]: http://www.w3api.com/wiki/HTML:DIV
 [8]: http://www.w3api.com/wiki/HTML:SPAN
 [9]: http://www.w3api.com/wiki/HTML:Id
 [10]: http://www.w3api.com/wiki/HTML:Class
 [11]: http://www.manualweb.net/tutorial-css/
