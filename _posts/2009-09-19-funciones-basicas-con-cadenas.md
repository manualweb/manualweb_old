---
ID: 114
post_title: '05 &#8211; Funciones básicas con cadenas'
author: Víctor Cuervo
post_date: 2009-09-19 20:22:20
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/java/funciones-basicas-con-cadenas/
published: true
nombreforo:
  - Java
urlcharla:
  - https://www.facebook.com/groups/java.es/
urlcurso:
  - >
    http://www.aulaprogramacion.com/mod/page/view.php?id=11
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/java/
urlmanual:
  - http://www.manualweb.net/tutorial-java/
---
<!--TOC-->
Una vez que hemos visto <a title="Crear una cadena de texto" href="http://www.manualweb.net/java/clase-string-representando-una-cadena/">lo sencillo que es crear una cadena de texto</a> vamos a echar un vistazo a los métodos que nos permiten manipular la cadena de texto.

Si tuviésemos que ordenar dichos métodos podríamos llegar a la siguiente división:
<ul>
	<li>Información básica de la cadena</li>
	<li>Comparación de Cadenas</li>
	<li>Búsqueda de caracteres</li>
	<li>Búsqueda de subcadenas</li>
	<li>Manejo de subcadenas</li>
	<li>Manejo de caracteres</li>
	<li>Conversión a String: valueOf()</li>
</ul>
<h3>Información básica de la cadena</h3>
<strong><a title=".length()" href="http://www.w3api.com/wiki/Java:String.length()">.length()</a></strong>
Nos devuelve el tamaño que tiene la cadena.

<strong><a title="charAt" href="http://www.w3api.com/wiki/Java:String.charAt()">char charAt(int index)</a></strong>
Devuelve el carácter indicado como índice. El primer carácter de la cadena será el del índice 0. Junto con el método <span class="codigo"><a title=".length()" href="http://www.w3api.com/wiki/Java:String.length()">.length()</a></span><span> podemos recuperar todos los caracteres de la cadena de texto.</span>

Hay que tener cuidado. Ya que si intentamos acceder a un índice de carácter que no existe nos devolverá una excepción <span class="codigo"><a title="IndexOutOfBoundsException" href="http://www.w3api.com/wiki/Java:IndexOutOfBoundsException">IndexOutOfBoundsException</a></span>.
<h3>Comparación de Cadenas</h3>
Los métodos de comparación nos sirven para comparar si dos cadenas de texto son iguales o no. Dentro de los métodos de comparación tenemos los siguientes:

<strong><a title=".equals()" href="http://www.w3api.com/wiki/Java:String.equals()">boolean equals(Object anObject)</a></strong>
Nos permite comparar si dos cadenas de texto son iguales. En el caso de que sean iguales devolverá como valor "true". En caso contrario devolverá "false".

Este método tiene en cuenta si los caracteres van en mayúsculas o en minúsculas. Si queremos omitir esta validación tenemos dos opciones. La primera es convertir las cadenas a mayúsculas o minúsculas con los métodos <span class="codigo"><a title=".toUpperCase()" href="http://www.w3api.com/wiki/Java:String.toUpperCase()">.toUpperCase()</a></span> y <span class="codigo"><a title="toLowerCase" href="http://www.w3api.com/wiki/Java:String.toLowerCase()">.toLowerCase()</a></span> respectivamente. Métodos que veremos más adelante.

La segunda opción es utilizar el método <span class="codigo"><a title=".equalsIgnoreCase()" href="http://www.w3api.com/wiki/Java:String.equalsIgnoreCase()">equalsIgnoreCase()</a></span> que omite si el carácter está en mayúsculas o en minúsculas.

<strong><a title="equalsIgnoreCase" href="http://www.w3api.com/wiki/Java:String.equalsIgnoreCase()">boolean equalsIgnoreCase(String anotherString)</a></strong>
Compara dos cadenas de caracteres omitiendo si los caracteres están en mayúsculas o en minúsculas.

<strong><a title=".compareTo" href="http://www.w3api.com/wiki/Java:String.compareTo()">int compareTo(String anotherString)</a></strong>
Este método es un poco más avanzado que el anterior, el cual, solo nos indicaba si las cadenas eran iguales o diferentes

En este caso compara a las cadenas léxicamente. Para ello se basa en el valor Unicode de los caracteres.

Se devuelve un entero menor de 0 si la cadena sobre la que se parte es léxicamente menor que la cadena pasada como argumento. Si las dos cadenas son iguales léxicamente se devuelve un 0. Si la cadena es mayor que la pasada como argumento se devuelve un número entero positivo.

Pero que es esto de “mayor, menor o igual léxicamente”. Para describirlo lo veremos con un pequeño ejemplo.
<pre lang="java">s1 = "Cuervo"
s2 = "Cuenca"
s1.compareTo(s2);</pre>
Compararíamos las dos cadenas. Los tres primeros caracteres son iguales "Cue". Cuando el método llega al 4 carácter tiene que validar entre la r minúscula y la n minúscula. Si utiliza el código Unicode llegará a la siguiente conclusión.
<pre lang="java">r (114) &gt; n(110)</pre>
Y nos devolverá la resta de sus valores. En este caso un 4.

Hay que tener cuidado, porque este método no tiene en cuenta las mayúsculas y minúsculas. Y dichos caracteres, aún siendo iguales, tienen diferentes código. Veamos la siguiente comparación
<pre lang="java">s1 = "CueRvo"
s2 = "Cuervo"
s1.compareTo(s2);</pre>
Nuevamente los tres caracteres iniciales son iguales. Pero el cuarto es distinto. Por un lado tenemos la r minúscula y por otro la r mayúscula. Así:
<pre lang="java">R(82) &lt; r(114)</pre>
¿Qué entero nos devolverá el método compareTo()? ¿-32?

<strong><a title="compareIgnoreCase()" href="http://www.w3api.com/wiki/Java:String.compareToIgnoreCase()">int compareToIgnoreCase(String str)</a></strong>
Este método se comportará igual que el anterior. Pero ignorando las mayúsculas. Todo un alivio por si se nos escapa algún carácter en mayúsculas ;-)

Otros métodos para la comparación de cadenas son:
<pre lang="java">boolean regionMatch( int thisoffset,String s2,int s2offset,int len );
boolean regionMatch( boolean ignoreCase,int thisoffset,String s2, int s2offset,int 1 );</pre>
<h3>Búsqueda de caracteres</h3>
Tenemos un conjunto de métodos que nos permiten buscar caracteres dentro de cadenas de texto. Y es que no nos debemos de olvidar que la cadena de caracteres no es más que eso: una suma de caracteres.

<strong><a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">int indexOf(int ch</a>)</strong>
Nos devuelve la posición de un carácter dentro de la cadena de texto. En el caso de que el carácter buscado no exista nos devolverá un -1. Si lo encuentra nos devuelve un número entero con la posición que ocupa en la cadena.

<strong><a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">int indexOf(int ch, int fromIndex)</a></strong>
Realiza la misma operación que el anterior método, pero en vez de hacerlo a lo largo de toda la cadena lo hace desde el índice (fromIndex) que le indiquemos.

<strong><a title="lastIndexOf()" href="http://www.w3api.com/wiki/Java:String.lastIndexOf()">int lastIndexOf(int ch)</a></strong>
Nos indica cual es la última posición que ocupa un carácter dentro de una cadena. Si el carácter no está en la cadena devuelve un -1.

<strong><a title="lastIndexOf()" href="http://www.w3api.com/wiki/Java:String.lastIndexOf()">int lastIndexOf(int ch, int fromIndex)</a></strong>
Lo mismo que el anterior, pero a partir de una posición indicada como argumento.
<h3>Búsqueda de subcadenas</h3>
Este conjunto de métodos son, probablemente, los más utilizados para el manejo de cadenas de caracteres. Ya que nos permiten buscar cadenas dentro de cadenas, así como saber la posición donde se encuentran en la cadena origen para poder acceder a la subcadena.

Dentro de este conjunto encontramos:

<strong><a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">int indexOf(String str)</a></strong>
Busca una cadena dentro de la cadena origen. Devuelve un entero con el índice a partir del cual está la cadena localizada. Si no encuentra la cadena devuelve un -1.

<strong><a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">int indexOf(String str, int fromIndex)</a></strong>
Misma funcionalidad que <a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">indexOf(String str)</a>, pero a partir de un índice indicado como argumento del método.

<strong><a title="lastIndexOf()" href="http://www.w3api.com/wiki/Java:String.lastIndexOf()">int lastIndexOf(String str)</a></strong>
Si la cadena que buscamos se repite varias veces en la cadena origen podemos utilizar este método que nos indicará el índice donde empieza la última repetición de la cadena buscada.

<strong><a title="lastIndexOf()" href="http://www.w3api.com/wiki/Java:String.lastIndexOf()">lastIndexOf(String str, int fromIndex)</a></strong>
Lo mismo que el anterior, pero a partir de un índice pasado como argumento.

<strong><a title="startsWith()" href="http://www.w3api.com/wiki/Java:String.startsWith()">boolean startsWith(String prefix)</a></strong>
Probablemente mucha gente se haya encontrado con este problema. El de saber si una cadena de texto empieza con un texto específico. La verdad es que este método podía obviarse y utilizarse el <a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">indexOf()</a>, con el cual, en el caso de que nos devolviese un 0, sabríamos que es el inicio de la cadena.

<strong><a href="http://www.w3api.com/wiki/Java:String.startsWith()">boolean startsWith(String prefix, int toffset)</a></strong>
Más elaborado que el anterior, y quizás, y a mi entender con un poco menos de significado que el anterior.

<strong><a title="endsWith()" href="http://www.w3api.com/wiki/Java:String.endsWith()">boolean endsWith(String suffix)</a></strong>
Y si alguien se ha visto con la necesidad de saber si una cadena empieza por un determinado texto, no va a ser menos el que se haya preguntado si la cadena de texto acaba con otra.

De igual manera que sucedía con el método <a title="startWith()" href="http://www.w3api.com/wiki/Java:String.startsWith()">startsWith()</a> podríamos utilizar una mezcla entre los métodos <a title="indexOf()" href="http://www.w3api.com/wiki/Java:String.indexOf()">.indexOf()</a> y <a title="length()" href="http://www.w3api.com/wiki/Java:String.length()">.length()</a> para reproducir el comportamiento de <a title="endsWith()" href="http://www.w3api.com/wiki/Java:String.endsWith()">.endsWith()</a>. Pero las cosas, cuanto más sencillas, doblemente mejores.
<h3>Métodos con subcadenas</h3>
Ahora que sabemos como localizar una cadena dentro de otra seguro que nos acucia la necesidad de saber como substraerla de donde está. Si es que no nos podemos estar quietos...

<strong><a title="substring()" href="http://www.w3api.com/wiki/Java:String.substring()">String substring(int beginIndex)</a></strong>
Este método nos devolverá la cadena que se encuentra entre el índice pasado como argumento (beginIndex) hasta el final de la cadena origen.

Así, si tenemos la siguiente cadena:
<pre lang="java">String s = "Víctor Cuervo"</pre>
El método…
<pre lang="java">s.substring(7)</pre>
Nos devolverá “Cuervo”.

<strong><a title="substring()" href="http://www.w3api.com/wiki/Java:String.substring()">String substring(int beginIndex, int endIndex)</a></strong>
Si se da el caso que la cadena que queramos recuperar no llega hasta el final de la cadena origen, que será lo normal, podemos utilizar este método indicando el índice inicial y final del cual queremos obtener la cadena.

Así, si partimos de la cadena...
<pre lang="java">String s = "En un lugar de la mancha...."</pre>
El método...
<pre lang="java">s.substring(6,11)</pre>
Nos devolverá la palabra “lugar”.
<blockquote>Hay que tener especial cuidado ya que es un error muy común el poner como índice final el índice del carácter último de la palabra a extraer. Cuando realmente es el índice + 1 de lo que queramos obtener.</blockquote>
<h3>Manejo de caracteres</h3>
Otro conjunto de métodos que nos permite jugar con los caracteres de la cadena de texto. Para ponerles en mayúsculas, minúsculas, quitarles los espacios en blanco, reemplazar caracteres,....

<strong><a title="toLowerCase()" href="http://www.w3api.com/wiki/Java:String.toLowerCase()">String toLowerCase();</a></strong>
Convierte todos los caracteres en minúsculas.

<strong><a title="toUpperCase()" href="http://www.w3api.com/wiki/Java:String.toUpperCase()">String toUpperCase();</a></strong>
Convierte todos los caracteres a mayúsculas.

<strong><a title="trim()" href="http://www.w3api.com/wiki/Java:String.trim()">String trim();</a></strong>
Elimina los espacios en blanco de la cadena.

<strong><a title="replace()" href="http://www.w3api.com/wiki/Java:String.replace()">String replace(char oldChar, char newChar)</a></strong>
Este método lo utilizaremos cuando lo que queramos hacer sea el remplazar un carácter por otro. Se reemplazarán todos los caracteres encontrados.
<h3>Conversión a String: valueOf()</h3>
Un potente conjunto de métodos de la clase <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> nos permite convertir a cadena cualquier tipo de dato básico: int, float, double,…

Esto es especialmente útil cuando hablamos de números. Ya que en múltiples ocasiones querremos mostrarles como cadenas de texto y no en su representación normal de número.

Así podemos utilizar los siguientes métodos:
<ul>
	<li><a title="valueOf()" href="http://www.w3api.com/wiki/Java:String.valueOf()">String valueOf(boolean b);</a></li>
	<li><a title="valueOf()" href="http://www.w3api.com/wiki/Java:String.valueOf()">String valueOf(int i);</a></li>
	<li><a title="valueOf()" href="http://www.w3api.com/wiki/Java:String.valueOf()">String valueOf(long l);</a></li>
	<li><a title="valueOf()" href="http://www.w3api.com/wiki/Java:String.valueOf()">String valueOf(float f);</a></li>
	<li><a title="valueOf()" href="http://www.w3api.com/wiki/Java:String.valueOf()">String valueOf(double d);</a></li>
	<li><a title="valueOf()" href="http://www.w3api.com/wiki/Java:String.valueOf()">String valueOf(Object obj);</a></li>
</ul>