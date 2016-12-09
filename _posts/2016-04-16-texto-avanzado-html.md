---
ID: 766
post_title: '09.02 &#8211; Texto avanzado en HTML'
author: Víctor Cuervo
post_date: 2016-04-16 12:00:52
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/texto-avanzado-html/
published: true
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
<a name="abbr"></a><h3>Abreviaturas y acrónimos</h3>
Cuando estamos escribiendo un texto es posible que nos encontremos con partes que sean abreviadas o partes que sean acrónimos.

Aunque abreviatura y acrónimo suenan similares, estas, tienen su pequeña diferencia. <b>Una abreviatura es un tipo de abreviación que consiste en la representación gráfica reducida de una palabra mediante la supresión de letras finales o centrales</b>, y que suele cerrarse con punto; p. ej., afmo. por afectísimo; Dir.a por directora; íd. por ídem; SS. MM. por Sus Majestades; D. por don.

Mientras que <b>acrónimo es un tipo de sigla que se pronuncia como una palabra</b>; p. ej., o(bjeto) v(olante) n(o) i(dentificado).

De esta forma en el lenguaje <a href="http://www.manualweb.net/tutorial-html/">HTML</a> nos encontramos con el <a href="http://www.w3api.com/wiki/HTML:ABBR">elemento abbr</a> para las abreviaturas y el <a href="http://www.w3api.com/wiki/HTML:ACRONYM">elemento acronym</a> para los acrónimos.

Si queremos insertar una abreviatura:

<pre lang="html4strict"><abbr title="Director">Dir.</abbr> Juan de la Espina
<abbr title="Sus Majestades">SS. MM.</abbr> los Reyes de España
<abbr title="Calle">C.</abbr> del Pez nº40</pre>

En el caso de la abreviatura <b>se suele acompañar por un atributo title</b>, el cual nos ofrece el texto completo que representa la abreviatura.

Y si queremos insertar un acrónimo podemos escribir lo siguiente:

<pre lang="html4strict"><acronym title="Objeto Volante No Identificado" lang="ES-es">OVNI</acronym></pre>

De igual forma que con el <a href="http://www.w3api.com/wiki/HTML:ABBR">elemento abbr</a>, en el <a href="http://www.w3api.com/wiki/HTML:ACRONYM">elemento acronym</a> encontramos <a href="http://www.w3api.com/wiki/HTML:Title">el atributo title</a>, el cual, en este caso, nos dirá que significan las siglas del acrónimo.

Otro atributo que solemos encontrar en estos elementos es el <a href="http://www.w3api.com/wiki/HTML:Lang">atributo lang</a>, el cual hace referencia al idioma en el que está escrita la abreviatura o el acrónimo.

<a name="pre"></a><h3>Textos preformateados</h3>
Ya hemos visto que a la hora de insertar texto en un documento <a href="http://www.manualweb.net/tutorial-html/">HTML</a> da igual poner muchos espacios o saltos de línea, ya que siempre serán ignorados.

Si bien, el lenguaje <a href="http://www.manualweb.net/tutorial-html/">HTML</a> nos ofrece el <a href="http://www.w3api.com/wiki/HTML:PRE">elemento pre</a>. El <a href="http://www.w3api.com/wiki/HTML:PRE">elemento pre</a> permite representar el texto tal cual es escrito, respetando sus espacios y saltos de línea. Acaba representando fielmente lo que hayamos insertado.

La estructura del <a href="http://www.w3api.com/wiki/HTML:PRE">elemento pre</a> es:

<pre lang="html4strict"><pre> Texto Preformateado &lt;/pre></pre>

De esta forma podríamos escribir lo siguiente:

<pre lang="html4strict"><pre>Esto es un texto
que está preformateado

y por lo tanto  --->   mantiene los espacios
y saltos de línea.&lt;/pre></pre>

Que en pantalla nos mostrará:
<pre>Esto es un texto
que está preformateado

y por lo tanto  --->   mantiene los espacios
                              y saltos de línea.</pre>

<a name="insdel"></a><h3>Notas de cambios en los documentos</h3>
Hay que pensar que <a href="http://www.manualweb.net/tutorial-html/">HTML</a> fue pensado para compartir documentos electrónicos. Es por ello que el contenido de dichos documentos electrónicos iría avanzando en las revisiones que fuesen teniendo. Por lo tanto habría contenido nuevo y contenido eliminado.

A tal respecto el lenguaje HTML nos ofrece dos elementos. El primero es el <a href="http://www.w3api.com/wiki/HTML:INS">elemento ins</a>, este elemento sirve para indicar que el contenido es nuevo y que sustituye a un contenido que hayamos definido mediante el <a href="http://www.w3api.com/wiki/HTML:DEL">elemento del</a>.

La estructura del <a href="http://www.w3api.com/wiki/HTML:INS">elemento ins</a> y del <a href="http://www.w3api.com/wiki/HTML:DEL">elemento del</a> es sencilla:

<pre lang="html4strict"><del>contenido eliminado</del>
<ins>contenido nuevo</ins></pre>

Por ejemplo podríamos encontrarnos el siguiente código en un documento HTML utilizando el <a href="http://www.w3api.com/wiki/HTML:INS">elemento ins</a> y el <a href="http://www.w3api.com/wiki/HTML:DEL">elemento del</a>:

<pre lang="html4strict">Los hechos sucedieron en Madrid, el pasado día <del>26</del><ins>28</ins> de febrero.</pre>

<a name="codigo"></a><h3>Manejando código fuente en HTML</h3>
Otra de las cosas para las que el lenguaje <a href="http://www.manualweb.net/tutorial-html/">HTML</a> fue pensando es el compartir código fuente, es decir, código informático.

Para poder cubrir esta necesidad nos ofrece un conjunto de elementos que representan semántica relacionada con el mundo de la computación.

Así tenemos.
<ul>
	<li><b>code</b>, para insertar código fuente.</li>
	<li><b>kbd</b>, para representar entradas de información por teclado.</li>
	<li><b>samp</b>, para mostrar las salidas por consola de información.</li>
	<li><b>var</b>, para definir las variables de un programa.</li>
</ul>
La estructura de los elementos <a href="http://www.w3api.com/wiki/HTML:CODE">code</a>, <a href="http://www.w3api.com/wiki/HTML:KBD">kbd</a>, <a href="http://www.w3api.com/wiki/HTML:SAMP">samp</a> y <a href="http://www.w3api.com/wiki/HTML:VAR">var</a> es la misma:

<pre lang="html4strict"><code> código fuente </code>
<kbd> entrada teclado </kbd>
<samp> salida por consola </samp>
<var> variable </var></pre>

Así podríamos encontrarnos el siguiente ejemplo HTML que usase estos cuatro elementos:

<pre lang="html4strict">El programa en Java se ejecuta mediante <kbd>java Saludo</kbd>. Lo que hará este código es ejecutar el siguiente programa.

<code>public class Saludo {
public static void main(String[] args)  {
   System.out.println("Hola"+ args[1]);
 }
}</code>

Dependiendo del valor que le demos a la variable <var>args</var> nos aparecerá un saludo u otro.
Así si ejecutamos como <kbd>java Saludo Esther</kbd> por pantalla nos mostrará
<samp>Hola Esther</samp></pre>

<a name="cite"></a><h3>Fuente o referencia de una cita</h3>
Aunque ya hemos visto que tenemos los elementos <a href="http://www.w3api.com/wiki/HTML:BLOCKQUOTE">blockquote</a> y <a href="http://www.w3api.com/wiki/HTML:Q">q</a> para crear citas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a>, el lenguaje <a href="http://www.manualweb.net/tutorial-html/">HTML</a> nos ofrece otro elemento para establecer una referencia o fuente de una cita. Este es el <a href="http://www.w3api.com/wiki/HTML:CITE">elemento cite</a>.

La estructura del <a href="http://www.w3api.com/wiki/HTML:CITE">elemento cite</a> sería:

<pre lang="html4strict"><cite>Fuente</cite></pre>

Hay que indicar que este elemento no es para representar la cita, si no la fuente o referencia origen de la cita.

Por ejemplo podríamos escribir lo siguiente con el <a href="http://www.w3api.com/wiki/HTML:CITE">elemento cite</a>:

<pre lang="html4strict"><cite>La sombra del ciprés es alargada</cite>, empieza diciendo “Yo nací en Ávila, la vieja ciudad de las murallas…”</pre>

<a name="dfn"></a><h3>Definiciones</h3>
Otro de los elementos que nos ofrece el lenguaje <a href="http://www.manualweb.net/tutorial-html/">HTML</a> es el <a href="http://www.w3api.com/wiki/HTML:DFN">elemento dfn</a>, este elemento es utilizado para marcar un término que va a ser definido dentro de un contenido.

La estructura del <a href="http://www.w3api.com/wiki/HTML:DFN">elemento dfn</a> es la siguiente:

<pre lang="html4strict"><dfn>término</dfn></pre>

Podemos utilizarlo de la siguiente forma:

<pre lang="html4strict">Un <dfn>gabán</dfn> es capote con mangas, y a veces con capilla.</pre>