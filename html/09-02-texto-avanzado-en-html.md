---
ID: 1388
post_title: 09.02 – Texto avanzado en HTML
author: Víctor Cuervo
post_date: 2017-04-12 00:30:49
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/texto-avanzado-en-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-texto/feed/
gitfolder: html
---
<a name="abbr"></a>
### Abreviaturas y acrónimos

Cuando estamos escribiendo un texto es posible que nos encontremos con partes que sean abreviadas o partes que sean acrónimos.

Aunque abreviatura y acrónimo suenan similares, estas, tienen su pequeña diferencia. **Una abreviatura es un tipo de abreviación que consiste en la representación gráfica reducida de una palabra mediante la supresión de letras finales o centrales**, y que suele cerrarse con punto; p. ej., afmo. por afectísimo; Dir.a por directora; íd. por ídem; SS. MM. por Sus Majestades; D. por don.

Mientras que **acrónimo es un tipo de sigla que se pronuncia como una palabra**; p. ej., o(bjeto) v(olante) n(o) i(dentificado).

De esta forma en el lenguaje [HTML][1] nos encontramos con el [elemento abbr][2] para las abreviaturas y el [elemento acronym][3] para los acrónimos. Si queremos insertar una abreviatura:

~~~html
<abbr title="Director">Dir.</abbr> Juan de la Espina
<abbr title="Sus Majestades">SS. MM.</abbr> los Reyes de España
<abbr title="Calle">C.</abbr> del Pez nº40
~~~

En el caso de la abreviatura **se suele acompañar por un atributo title**, el cual nos ofrece el texto completo que representa la abreviatura.

Y si queremos insertar un acrónimo podemos escribir lo siguiente:

~~~html
<acronym title="Objeto Volante No Identificado">OVNI</acronym></pre>
~~~

De igual forma que con el [elemento abbr][2], en el [elemento acronym][3] encontramos [el atributo title][4], el cual, en este caso, nos dirá que significan las siglas del acrónimo.

Otro atributo que solemos encontrar en estos elementos es el [atributo lang][5], el cual hace referencia al idioma en el que está escrita la abreviatura o el acrónimo.

<a name="pre"></a>
### Textos preformateados
Ya hemos visto que a la hora de insertar texto en un documento [HTML][1] da igual poner muchos espacios o saltos de línea, ya que siempre serán ignorados.

Si bien, el lenguaje [HTML][1] nos ofrece el [elemento pre][6]. El [elemento pre][6] permite representar el texto tal cual es escrito, respetando sus espacios y saltos de línea. Acaba representando fielmente lo que hayamos insertado.

La estructura del [elemento pre][6] es:

~~~html
<pre>Texto Preformateado</pre>
~~~

De esta forma podríamos escribir lo siguiente:

~~~html
<pre>Esto es un texto
que está preformateado

y por lo tanto  --->   mantiene los espacios
                       y saltos de línea.</pre>
~~~

Que en pantalla nos mostrará:

<pre>Esto es un texto
que está preformateado

y por lo tanto  --->   mantiene los espacios
                       y saltos de línea.</pre>

<a name="insdel"></a>
### Notas de cambios en los documentos

Hay que pensar que [HTML][1] fue pensado para compartir documentos electrónicos. Es por ello que el contenido de dichos documentos electrónicos iría avanzando en las revisiones que fuesen teniendo. Por lo tanto habría contenido nuevo y contenido eliminado.

A tal respecto el lenguaje HTML nos ofrece dos elementos. El primero es el [elemento ins][7], este elemento sirve para indicar que el contenido es nuevo y que sustituye a un contenido que hayamos definido mediante el [elemento del][8].

La estructura del [elemento ins][7] y del [elemento del][8] es sencilla:

~~~html
<del>contenido eliminado</del>
<ins>contenido nuevo</ins>
~~~

Por ejemplo podríamos encontrarnos el siguiente código en un documento HTML utilizando el [elemento ins][7] y el [elemento del][8]:

~~~html
Los hechos sucedieron en Madrid, el pasado día <del>26</del><ins>28</ins> de febrero.
~~~

<a name="codigo"></a>

### Manejando código fuente en HTML

Otra de las cosas para las que el lenguaje

[HTML][1] fue pensando es el compartir código fuente, es decir, código informático.

Para poder cubrir esta necesidad nos ofrece un conjunto de elementos que representan semántica relacionada con el mundo de la computación.

Así tenemos.

*   **code**, para insertar código fuente.
*   **kbd**, para representar entradas de información por teclado.
*   **samp**, para mostrar las salidas por consola de información.
*   **var**, para definir las variables de un programa.

La estructura de los elementos

[code][9], [kbd][10], [samp][11] y [var][12] es la misma:

     código fuente
    <kbd> entrada teclado </kbd>
    <samp> salida por consola </samp>
    <var> variable </var>


Así podríamos encontrarnos el siguiente ejemplo HTML que usase estos cuatro elementos:

<pre>El programa en Java se ejecuta mediante <kbd>java Saludo</kbd>. Lo que hará este código es ejecutar el siguiente programa.

<code>public class Saludo {
public static void main(String[] args)  {
   System.out.println("Hola"+ args[1]);
 }
}</code>

Dependiendo del valor que le demos a la variable <var>args</var> nos aparecerá un saludo u otro.
Así si ejecutamos como <kbd>java Saludo Esther</kbd> por pantalla nos mostrará
<samp>Hola Esther</samp></pre>

<a name="cite"></a>

### Fuente o referencia de una cita

Aunque ya hemos visto que tenemos los elementos

[blockquote][13] y [q][14] para crear citas en [HTML][1], el lenguaje [HTML][1] nos ofrece otro elemento para establecer una referencia o fuente de una cita. Este es el [elemento cite][15].

La estructura del [elemento cite][15] sería:

<pre><cite>Fuente</cite></pre>

Hay que indicar que este elemento no es para representar la cita, si no la fuente o referencia origen de la cita.

Por ejemplo podríamos escribir lo siguiente con el

[elemento cite][15]:

<pre><cite>La sombra del ciprés es alargada</cite>, empieza diciendo “Yo nací en Ávila, la vieja ciudad de las murallas…”</pre>

<a name="dfn"></a>

### Definiciones

Otro de los elementos que nos ofrece el lenguaje

[HTML][1] es el [elemento dfn][16], este elemento es utilizado para marcar un término que va a ser definido dentro de un contenido.

La estructura del [elemento dfn][16] es la siguiente:

<pre><dfn>término</dfn></pre>

Podemos utilizarlo de la siguiente forma:

<pre>Un <dfn>gabán</dfn> es capote con mangas, y a veces con capilla.</pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:ABBR
 [3]: http://www.w3api.com/wiki/HTML:ACRONYM
 [4]: http://www.w3api.com/wiki/HTML:Title
 [5]: http://www.w3api.com/wiki/HTML:Lang
 [6]: http://www.w3api.com/wiki/HTML:PRE
 [7]: http://www.w3api.com/wiki/HTML:INS
 [8]: http://www.w3api.com/wiki/HTML:DEL
 [9]: http://www.w3api.com/wiki/HTML:CODE
 [10]: http://www.w3api.com/wiki/HTML:KBD
 [11]: http://www.w3api.com/wiki/HTML:SAMP
 [12]: http://www.w3api.com/wiki/HTML:VAR
 [13]: http://www.w3api.com/wiki/HTML:BLOCKQUOTE
 [14]: http://www.w3api.com/wiki/HTML:Q
 [15]: http://www.w3api.com/wiki/HTML:CITE
 [16]: http://www.w3api.com/wiki/HTML:DFN
