---
ID: 727
post_title: '05 &#8211; Sintaxis del HTML'
author: Víctor Cuervo
post_date: 2016-04-07 12:00:19
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/sintaxis-del-html/
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
En la sintaxis del HTML hablamos sobre:

[TOC]

<span style="font-weight: 400;">Dentro del </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> vamos a encontrar diferentes estructuras que deberemos de diferenciar. En primer lugar están </span><b>los elementos</b><span style="font-weight: 400;"> que es la principal estructura del lenguaje y los que conforman las páginas web.</span>

<span style="font-weight: 400;">A su vez los elementos contendrán </span><b>atributos</b><span style="font-weight: 400;">. Los atributos dan más especificidad al comportamiento de los elementos, permitiendo parametrizarlos.</span>
<h3><b>Los elementos HTML</b></h3>
<span style="font-weight: 400;">Los elementos </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> son los que configuran la estructura de la página. También son llamados en algunos sitios como etiquetas, derivado del tema del lenguaje de marcado. Si bien su nombre correcto es el de elementos.</span>

<span style="font-weight: 400;">Todo elemento se encierra entre los símbolos <strong>menor que &lt;</strong> y <strong>mayor que &gt;</strong>:</span>
<pre><span style="font-weight: 400;">&lt;elemento&gt;</span></pre>
<span style="font-weight: 400;">Dentro de los elementos </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> encontramos dos tipos:</span>
<ul>
	<li style="font-weight: 400;"><span style="font-weight: 400;">Elementos que tienen un inicio y un cierre</span></li>
	<li style="font-weight: 400;"><span style="font-weight: 400;">Elementos únicos</span></li>
</ul>
<span style="font-weight: 400;">Los </span><b>elementos que tienen un inicio y un cierre</b><span style="font-weight: 400;"> permiten tener a otros elementos u otro contenido anidado, es decir, a otros elementos o directamente texto. La estructura de los elementos de inicio y cierre es la siguiente:</span>
<pre><span style="font-weight: 400;">&lt;elemento&gt; contenido| subelementos &lt;/elemento&gt;</span></pre>
<span style="font-weight: 400;">Como podemos apreciar el elemento de cierre se precede de una barra invertida.</span>

<span style="font-weight: 400;">Algunos de estos elementos son </span><a href="http://www.w3api.com/wiki/HTML:P"><span style="font-weight: 400;">p</span></a><span style="font-weight: 400;">, </span><a href="http://www.w3api.com/wiki/HTML:DIV"><span style="font-weight: 400;">div</span></a><span style="font-weight: 400;">, </span><a href="http://www.w3api.com/wiki/HTML:UL"><span style="font-weight: 400;">ul</span></a><span style="font-weight: 400;">,...</span>

<span style="font-weight: 400;">En el caso de los elementos únicos, estos no permiten anidar contenido y aparecen de forma aislada. Su estructura es la siguiente:</span>
<pre><span style="font-weight: 400;">&lt;elemento /&gt;</span></pre>
<span style="font-weight: 400;">Como podemos apreciar la barra invertida se encuentra al final y dentro del elemento. Algún ejemplo de estos elementos es </span><a href="http://www.w3api.com/wiki/HTML:IMG"><span style="font-weight: 400;">img</span></a><span style="font-weight: 400;">, </span><a href="http://www.w3api.com/wiki/HTML:BR"><span style="font-weight: 400;">br</span></a><span style="font-weight: 400;">,...</span>
<h3><b>Atributos en HTML</b></h3>
<span style="font-weight: 400;">Los elementos pueden ser parametrizados mediante los atributos. Los atributos siguen la estructura nombre/valor y se deberán de poner antes del cierre del elemento.</span>

<span style="font-weight: 400;">La estructura de definición de los atributos es la siguiente:</span>
<pre><span style="font-weight: 400;">&lt;elemento atributo=”valor”&gt;</span></pre>
<span style="font-weight: 400;">El valor del atributo estará delimitado mediante comillas simples o comillas dobles.</span>
<h3><b>Entidades en HTML</b></h3>
<span style="font-weight: 400;">Otra estructura que nos podemos encontrar dentro de una página </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> son las entidades. Las entidades <strong>empiezan por un ampersand &amp;</strong>, seguidas del <strong>código de la entidad</strong> -que puede ser numérico o alfanumérico- y <strong>finalizan en un punto y coma ;</strong></span>

<span style="font-weight: 400;">La estructura de una entidad en </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> será la siguiente:</span>
<pre><span style="font-weight: 400;">&amp;código;</span></pre>
<span style="font-weight: 400;">Las entidades nos sirven para representar símbolos que son parte de la estructura del lenguaje, como es el caso de los símbolos mayor y menor. O símbolos específicos de un determinado juego de caracteres, cómo podrían ser símbolos de monedas o caracteres especiales.</span>
<pre>&amp;lt;      representa &lt;
&amp;gt;      representa &gt;
&amp;quot;    representa ‘
&amp;eur;     representa €</pre>
<span style="font-weight: 400;">Ya hablaremos en detalle sobre ellas más adelante.</span>
<h3><b>Comentarios en HTML</b></h3>
<span style="font-weight: 400;">Para poder insertar un comentario dentro de las páginas </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> deberemos de utilizar la siguiente estructura:</span>
<pre lang="html4strict"><!-- comentario --></pre>
El comentario puede tener varias líneas de texto.
<pre lang="html4strict"><!-- esto es 
         un comentario --></pre>
<h3><b>Normas de codificación en un documento HTML</b></h3>
<span style="font-weight: 400;">Existen una serie de normas de codificación que hay que conocer y seguir dentro del lenguaje </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> a la hora de crear nuestras páginas web.</span>
<h4><b>No sensible a mayúsculas</b></h4>
<span style="font-weight: 400;">El lenguaje </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> no es sensible a mayúsculas. Es decir, que da igual que escribamos nuestros elementos y atributos en mayúsculas y/o minúsculas.</span>

<span style="font-weight: 400;">Si bien, por convenio, </span><b>se recomienda que tanto los elementos como los atributos sean escritos en minúsculas</b><span style="font-weight: 400;">.</span>
<h4><b>Espacios en blanco</b></h4>
<span style="font-weight: 400;">Si insertamos un espacio en blanco dentro de nuestra página se generará un espacio en blanco dentro de la visualización. Si bien si juntamos varios espacios en blancos, </span><b>estos solo generarán un único espacio en blanco</b><span style="font-weight: 400;">.</span>

<span style="font-weight: 400;">Lo mismo ocurre si insertamos una o varias tabulaciones. Estas solo generan un único espacio en blanco. Si queremos crear un conjunto de espacios en blanco seguidos deberemos de utilizar la entidad: </span>
<pre lang="html4strict">&nbsp;</pre>
<span style="font-weight: 400;">Cada vez que insertemos esta entidad generamos un espacio en blanco.</span>
<h4><b>Saltos de línea</b></h4>
<span style="font-weight: 400;">Los saltos de línea que insertemos dentro de la página web no tienen ningún efecto de cara a la renderización del contenido. Por lo tanto, un salto de línea en el código no genera nada.</span>

Si queremos insertar un salto de línea dentro de nuestra página web deberemos de utilizar el elemento
<pre lang="html4strict"><br/></pre>