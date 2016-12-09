---
ID: 805
post_title: '14 &#8211; Agrupaciones en HTML'
author: Víctor Cuervo
post_date: 2016-04-21 12:00:07
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/agrupaciones-html/
published: true
urlejemplos:
  - >
    http://lineadecodigo.com/tag/html-capas/feed/
nombreforo:
  - HTML
urlforo:
  - http://dudasprogramacion.com/html
urlmanual:
  - http://www.manualweb.net/tutorial-html/
urltest:
  - http://www.testprogramacion.com/html
urlcurso:
  - >
    http://www.aulaprogramacion.com/curso-html/
urlcharla:
  - >
    https://www.facebook.com/groups/html5.es/
urlvideo:
  - PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
---
<span style="font-weight: 400;">Hasta ahora hemos visto cómo insertar diferentes elementos sobre un documento </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;">. Estos elementos se irán mostrando según la secuencia en la que hayamos escrito el documento </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;">.</span>

Una de las cosas que tenemos que saber de los elementos html es si son elementos de bloque o elementos de línea.

<span style="font-weight: 400;">Un </span><b>elemento de bloque</b><span style="font-weight: 400;"> es aquél que una vez utilizado aparece en la siguiente línea y ocupa todo el ancho. Elementos de tipo bloque son los </span><a href="http://www.w3api.com/wiki/HTML:P"><span style="font-weight: 400;">párrafos p</span></a><span style="font-weight: 400;">, los </span><a href="http://www.w3api.com/wiki/HTML:FORM"><span style="font-weight: 400;">formularios form</span></a><span style="font-weight: 400;">, o </span><a href="http://www.w3api.com/wiki/HTML:H1"><span style="font-weight: 400;">las cabeceras hx</span></a><span style="font-weight: 400;">.</span>

<span style="font-weight: 400;">Un </span><b>elemento en línea</b><span style="font-weight: 400;"> es aquel que se muestra justo a continuación del anterior elemento. Estos elementos serían los </span><a href="http://www.w3api.com/wiki/HTML:A"><span style="font-weight: 400;">enlaces a</span></a><span style="font-weight: 400;">, </span><a href="http://www.w3api.com/wiki/HTML:IMG"><span style="font-weight: 400;">imágenes img</span></a><span style="font-weight: 400;">,...</span>

<span style="font-weight: 400;">El lenguaje </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> nos permite agrupar un conjunto de elementos mediante una agrupación en bloque o una agrupación en línea.</span>

<h3>Agrupaciones en Bloque</h3>
<span style="font-weight: 400;">Un elemento en bloque siempre empieza con una línea y su tamaño será igual al ancho disponible. El ancho disponible inicialmente es el de la página.</span>

<span style="font-weight: 400;">El elemento que nos permite realizar agrupaciones en bloque es el </span><a href="http://www.w3api.com/wiki/HTML:DIV"><span style="font-weight: 400;">elemento div</span></a><span style="font-weight: 400;"> o más conocidos como capas. La estructura del </span><a href="http://www.w3api.com/wiki/HTML:DIV"><span style="font-weight: 400;">elemento div</span></a><span style="font-weight: 400;"> es:</span>

<pre lang="html4strict"><div>
<!-- Contenido de la Capa -->
</div></pre>

<span style="font-weight: 400;">Los elementos en bloque pueden contener a otros elementos en bloque o bien a otros elementos en línea.</span>

<span style="font-weight: 400;">Por ejemplo podríamos agrupar en un bloque el siguiente contenido.</span>

<pre lang="html4strict"><div id=”micapa”>
  <h2>Título del Contenido</h2>
  Este es el contenido del artículo
  <img src=”logo.jpg” />
  <p>Más contenido del artículo</p>
</div></pre>

<h3>Agrupaciones en Línea</h3>
<span style="font-weight: 400;">Para poder realizar agrupaciones en línea tenemos el </span><a href="http://www.w3api.com/wiki/HTML:SPAN"><span style="font-weight: 400;">elemento span</span></a><span style="font-weight: 400;">. La estructura del </span><a href="http://www.w3api.com/wiki/HTML:SPAN"><span style="font-weight: 400;">elemento span</span></a><span style="font-weight: 400;"> será:</span>

<pre lang="html4strict"><span> <!-- Contenido --></span></pre>

<span style="font-weight: 400;">Las agrupaciones en línea sólo pueden contener a otros elementos en línea, no a elementos de tipo bloque.</span>

<span style="font-weight: 400;">Por ejemplo podríamos tener la siguiente agrupación en línea.</span>

<pre lang="html4strict"><span id=”entrada”>
  <strong>Articulo Nuevo</strong>,
  <em>,12 de marzo de 2016</em>
</span></pre>

<span style="font-weight: 400;">Es muy normal que los agrupadores, ya sean o bien </span><a href="http://www.w3api.com/wiki/HTML:DIV"><span style="font-weight: 400;">div</span></a><span style="font-weight: 400;">, o bien </span><a href="http://www.w3api.com/wiki/HTML:SPAN"><span style="font-weight: 400;">span</span></a><span style="font-weight: 400;"> lleven el </span><a href="http://www.w3api.com/wiki/HTML:Id"><span style="font-weight: 400;">atributo id</span></a><span style="font-weight: 400;"> o </span><a href="http://www.w3api.com/wiki/HTML:Class"><span style="font-weight: 400;">class</span></a><span style="font-weight: 400;">, ya que a posteriori serán manipulados mediante </span><a href="http://www.manualweb.net/tutorial-css/"><span style="font-weight: 400;">hojas de estilo CSS</span></a><span style="font-weight: 400;"> utilizando dichos identificadores.</span>