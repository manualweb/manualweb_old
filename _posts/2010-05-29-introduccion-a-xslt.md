---
ID: 280
post_title: Introducción a XSLT
author: Víctor Cuervo
post_date: 2010-05-29 00:23:26
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/xslt/introduccion-a-xslt/
published: true
nombreforo:
  - XSLT
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/extensible-stylesheet-language-transformations-xslt
---
<!--TOC-->
<h3>Qué es XSLT</h3>
<a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSLT</a> o <a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSL Transformations</a> es la parte más importante del lenguaje <a title="XSL" href="http://www.manualweb.net/tutorial-xsl/">XSL (eXtensible StyleSheet Language)</a>. La función de <a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSLT</a> es la de transformar documentos <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> en documentos <a title="xhtml" href="http://www.manualweb.net/tutorial-xhtml/">XHTML</a> u otros documentos <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a>. El W3C es el encargado de la definición de especificación <a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSLT</a>.

<a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSLT</a> se basa en XPath para realizar la búsqueda de información a través del documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a>. XPath son cadenas que son expresiones regulares, las cuales hacen referencia a alguna estructura dentro del documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a>.

El proceso de transformación se basa en plantillas. Dichas plantillas identifican una estructura a partir de la cual realizar la transformación (con XPath), así como las acciones a realizar con dicha estructura: recorrerla, obtener el dato de la etiqueta, el valor de alguno de sus atributos, contar cuantos elementos tiene la etiqueta anidados,...

Además, para poder aplicar las transformaciones, necesitaremos asociar el documento de transformación al documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> receptor de la misma.

Antes de empezar a aprender más cosas sobre <a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSLT</a> sería recomendable que tuvieses algún conocimiento sobre <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a>.
<h3>HTML versus XML+XSLT</h3>
A diferencia del lenguaje <a title="HTML" href="http://www.manualweb.net/tutorial-html/">HTML</a>, donde cada una de sus etiquetas lleva asociada una representación gráfica, el <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> identifica datos, los cuales no tienen representación gráfica asociada.

Cuando definimos una tabla en <a title="HTML" href="http://www.manualweb.net/tutorial-html/">HTML</a> (la etiqueta <a title="Table" href="http://w3api.com/wiki/HTML:TABLE">table</a>), sabemos que las herramientas que interpreten el documento <a title="HTML" href="http://www.manualweb.net/tutorial-html/">HTML</a>, normalmente los navegadores web, pintarán la tabla. De una forma u otra visualizaremos la tabla en nuestra pantalla.

Si bien, si tenemos un documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a>, donde podemos tener definida la etiqueta &lt;libro&gt;, está no tendrá ninguna representación gráfica asociada. Es por ello que si visualizamos nuestro documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> con alguna herramienta, esta, mostrará el contenido de la etiqueta, pero sin ninguna representación.

Es en este punto donde entra el lenguaje <a title="XSLT" href="http://www.manualweb.net/tutorial-xslt/">XSLT</a>. Y es que este lenguaje permite transformar el susodicho documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> en otro formato, el resultado de la transformación será el que lleve la representación gráfica.
<h3>Ejemplos de transformaciones</h3>
Así, podemos tener múltiples transformaciones del documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> en otros documentos de distintos lenguajes: <a title="xhtml" href="http://www.manualweb.net/tutorial-xhtml/">XHTML</a>, <a title="svg" href="http://www.manualweb.net/tutorial-svg/">SVG</a>, <a title="VRML" href="http://www.manualweb.net/tutorial-vrml/">VRML</a>,... Por ejemplo, un documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> que tuviese una lista de números podría ser transformado en: una tabla o lista de hitos con dicho listado en <a title="HTML" href="http://www.manualweb.net/tutorial-html/">HTML</a>, en un gráfico de líneas con <a title="svg" href="http://www.manualweb.net/tutorial-svg/">SVG</a> o podrían ser las alturas de figuras 3D con <a title="VRML" href="http://www.manualweb.net/tutorial-vrml/">VRML</a>.

Veamos cómo serían dichas transformaciones:
<h4>XML original</h4>
<pre lang="xml"> 2
 4
 6
 8</pre>
<h4>XML transformado en HTML</h4>
<pre lang="html4strict">
<table>
<tbody>
<tr>
<th>Datos</th>
</tr>
<tr>
<td>2</td>
</tr>
<tr>
<td>4</td>
</tr>
<tr>
<td>6</td>
</tr>
<tr>
<td>8</td>
</tr>
</tbody>
</table>
</pre>
<h4>XML transformado en SVG</h4>
<h4>XML transformado en VRML</h4>
<pre lang="vrml">#VRML V2.0 utf8
 Box {
  size 2 4 6
}</pre>
En estos ejemplos, vemos que los datos de partida de un documento <a title="XML" href="http://www.manualweb.net/tutorial-xml/">XML</a> son utilizados como contenido de otros documentos que tienen representaciones gráficas y pasan a ser valores de los mismos. En el documento <a title="HTML" href="http://www.manualweb.net/tutorial-html/">HTML</a> son datos de una tabla, en el documento <a title="svg" href="http://www.manualweb.net/tutorial-svg/">SVG</a> son las coordenadas de una línea y en el documento <a title="VRML" href="http://www.manualweb.net/tutorial-vrml/">VRML</a> son las dimensiones de un cubo.