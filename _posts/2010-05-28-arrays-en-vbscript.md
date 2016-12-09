---
ID: 273
post_title: '03 &#8211; Arrays en VBScript'
author: Víctor Cuervo
post_date: 2010-05-28 23:22:57
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/vbscript/arrays-en-vbscript/
published: true
nombreforo:
  - VBScript
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/vbscript
---
[TOC]
<h3>Declarar un Array</h3>
Para declarar un array en VBScript bastará con declarar una variable que tenga un rango, el cual establecerá el tamaño del array. Cada rango será una dimensión del array, así un array con dos dimensiones será una matriz. El límite de dimensiones en VBScript es de 60.

Veamos como se declara un array:
<pre>DIM miArray (3)
DIM miMatriz (2,10)</pre>
Cuando estamos declarando un array de x posiciones, este, tiene como tamaño x+1. En los casos anteriores tendrían una longitud de 4 en el primero y 3,11 en el segundo de los casos.

Para acceder a un determinado elemento del array lo haremos de la siguiente forma:
<pre>miArray(posicion)
'Si se tratase de una matriz
miArray(posicion,posicion)</pre>
Ya sea para mostrar su valor:
<pre>document.write (miArray(posicion))</pre>
o para modificarlo:
<pre>miArray(posicion) = valor</pre>
<h3>Recorriendo el Array</h3>
Para mostrar todo el contenido de un array nos podemos ayudar de alguna sentencia de control de flujo repetitiva. Veamos como mostrarlo mediante un bucle for.
<pre>for x=0 to UBound(miArray)
  document.write(miArray(x))
next</pre>
Para controlar el tamaño del array utilizamos la función <a title="UBound()" href="http://w3api.com/wiki/VBScript:Ubound">UBound(array)</a>.
<h3>Arrays de múltiples tipos</h3>
Una de las características principales de los arrays en VBScript es que estos pueden albergar datos de diferentes tipos. Es decir, no tenemos que declarar un array ded Strings o de enteros, sino que el array puede contener strings y entreros al mismo tiempo.

Así podriamos tener el siguiente código:
<pre>miArray(0) = "Cadena"
miArray(1) = 4
miArray(2) = #16/09/1976#
miArray(3) = true</pre>
<h3>Redimensionar un Array</h3>
La segunda de las características de los arrays es que pueden ser redimensionados, es decir, que podemos cambiar el tamaño del array una vez que este ha sido declarado. Solo se podrán redimensionar los arrays que se hayan declarado sin dimensión.

Para redimensionar un array utilizaremos la sentencia redim. La redimensión puede ser tanto para aumentar como para disminuir su tamaño.
<pre>DIM miArray()
REDIM miArray(2)</pre>
Si redimensionamos el array tal cual, perderemos su contenido. Para evitar esto utilizaremos la clausula preserve.
<pre>REDIM PRESERVE miArray(2)</pre>
<h3>Ejemplos de Código relacionados</h3>
<ul>
	<li><a title="Recorrer una matriz en VBScript" href="http://lineadecodigo.com/vbscript/recorrer-una-matriz-en-vbscript/">Recorrer una matriz en VBScript</a></li>
	<li><a title="Redimensionar un array con VBScript" href="http://lineadecodigo.com/vbscript/redimensionar-un-array-con-vbscript/">Redimensionar un array con VBScript</a></li>
</ul>