---
ID: 260
post_title: '01 &#8211; Introducción al VBScript'
author: Víctor Cuervo
post_date: 2010-05-28 22:44:11
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/vbscript/introduccion-al-vbscript/
published: true
nombreforo:
  - VBScript
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/vbscript
---
<!--TOC-->
VBScript es un subconjunto de Visual Basic for Applications. Es un lenguaje script cuyo uso se extiende tanto en páginas web de maquinas cliente como en páginas activas de servidor (ASP), si bien, es en este segundo caso, donde adquiere mayor importancia.
<h3>Comentarios</h3>
Para introducir un comentario deberemos de usar la apostrofe ' o bien la palabra REM.
<pre lang="vbscript">REM Esto es un comentario
' Esto es un comentario</pre>
<h3>Tipos de Datos</h3>
Lo primero que debemos de indicar es que en VBScript no es necesario darle un tipo a la variable. Es decir, podremos tener variables sin tipo a las cuales podremos asignarles cualquier valor. Estas variables serían de tipo variant.

Los tipos básicos que tiene VBScript son:
<ul>
	<li><strong>Byte</strong>, enteros entre 0 y 255</li>
	<li><strong>Integer</strong>, enteros entre -32.786 y 32.767</li>
	<li><strong>Long</strong>, enteros entre -2.147.483.648 y 2.147.483.647</li>
	<li><strong>Single</strong>, números reales de precisión simple</li>
	<li><strong>Double</strong>, números reales de doble precisión</li>
	<li><strong>Currency</strong>, cifras monetarias</li>
	<li><strong>Date</strong>, fechas entre 01/01/100 y 31/12/9999</li>
	<li><strong>String</strong>, cadenas de hasta 2 millones de caracteres</li>
	<li><strong>Boolean</strong>, valor booleano. Puede tomar true o false.</li>
	<li><strong>Null</strong>, valor nulo. No contiene nada.</li>
	<li><strong>Empty</strong>, es el tipo que toma una variable variant cuando está sin inicializar (0 si es numérica y "" si es cadena).</li>
	<li><strong>Error</strong>, sería el tipo error.</li>
</ul>
Existen una serie de funciones que nos servirán para ver cual es el tipo de las variables. Estas funciones son:
<ul>
	<li><strong>IsEmpty (variable)</strong>, devuelve True si la variable es de tipo Empty</li>
	<li><strong>IsError (variable)</strong>, devuelve True si la variable es de tipo Error.</li>
	<li><strong>IsNull (variable)</strong>, devuelve True si la variable es de tipo Null.</li>
	<li><strong>IsNumeric (variable)</strong>, devuelve True si la variable es un número de cualquier tipo.</li>
	<li><strong>IsObject (variable)</strong>, devuelve True si la variable pertenece al tipo Object.</li>
</ul>
Si bien, existe una función que devuelve el tipo de la variable, independientemente del tipo que esta sea. Esta función es <strong>vartype (variable)</strong>. Los posibles valores que puede devolver son:
<ul>
	<li>0-Null</li>
	<li>1-Empty</li>
	<li>2 -Integer</li>
	<li>3-Long</li>
	<li>4-Single</li>
	<li>5-Double</li>
	<li>6-Currency</li>
	<li>7-Date</li>
	<li>8-String</li>
	<li>9-Objeto de automatización</li>
	<li>10-Error</li>
	<li>11-Boolean</li>
	<li>12-Variant</li>
	<li>13-Objeto de acceso a datos</li>
	<li>17-Byte</li>
	<li>8192-Array</li>
</ul>
También tenemos unas funciones que nos van a ayudar a cambiar el tipo de las variables. Estas son las funciones de conversión:
<ul>
	<li><strong>CBool (variable),</strong> convierte la variable en booleana. Si la variable vale 0 se convertirá en true. Otro valor se convertira en false.</li>
	<li><strong>CByte (variable),</strong> convierte la variable en Byte.</li>
	<li><strong>CInt (variable), </strong>convierte la variable en Integer.</li>
	<li><strong>CLng (variable)</strong>, convierte la variable en Long.</li>
	<li><strong>CSng (variable)</strong>, convierte la variable en Single.</li>
	<li><strong>CDbl (variable)</strong>, convierte la variable en Double.</li>
	<li><strong>CCur (variable)</strong>, convierte la variable en Currency.</li>
	<li><strong>CDate (variable)</strong>, convierte la variable en Date.</li>
	<li><strong>CStr (variable)</strong>, convierte la variable en String.</li>
</ul>
<h3>Variables</h3>
Para declarar una variable lo haremos de la siguiente manera:
<pre lang="vbscript">DIM nombre_variable1, nombre_variable2,..., nombre_variableN</pre>
Los nombres de las variables deben de comenzar por una letra, no pueden contener el carácter punto y no deben de exceder de 255 caracteres.

El ámbito de las variables será global a todos el código script de la página, o bien local si la variable ha sido declarada en un procedimiento.
<h3>Constantes</h3>
Para declarar una constante deberemos de hacerlo de la siguiente manera:
<pre>CONST nombre_constante = valor</pre>
El valor que se le asigne a la variable no podrá alterarse.
<h3>Ejemplos de código relacionados</h3>
<ul>
	<li><a title="Como definir una variable en VBScript" href="http://lineadecodigo.com/vbscript/como-definir-una-constante-en-vbscript/">Cómo definir una constante en VBScript</a></li>
	<li><a title="Comentar código en VBScript" href="http://lineadecodigo.com/vbscript/comentar-codigo-en-vbscript/">Comentar código en VBScript</a></li>
</ul>