---
ID: 1273
post_title: '04 &#8211; Clase String: Representando una cadena'
author: Víctor Cuervo
post_date: 2017-04-10 10:54:10
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1273
published: false
nombreforo:
  - Java
urlforo:
  - http://www.dudasprogramacion.com/java/
urlejemplos:
  - >
    http://lineadecodigo.com/categoria/java/feed/
urlvideo:
  - PLLVIhySQmrVbjCFPla5c0OIp6iNWfM-hq
urlmanual:
  - http://www.manualweb.net/tutorial-java/
urltest:
  - http://www.testprogramacion.com/java
urlcurso:
  - http://www.aulaprogramacion.com/java/
gitfolder:
  - java
---
<!--TOC-->Una cadena de texto no deja de ser más que la sucesión de un conjunto de caracteres alfanuméricos, signos de puntuación y espacios en blanco con más o menos sentido.

<p class="texto">
  Podemos encontrarnos desde la archiconocida cadena “Hola Mundo” y la no menos “Mi primera cadena de texto”, pasando por las cadenas de texto personalizadas “Víctor”, “Víctor Cuervo”, las cadenas de depuración “¿Aquí?”, “Paso 1”, “Paso 2”,... hasta las inclasificables “asdf”.
</p>

<p class="texto">
  Todas ellas serán representadas en java con la clase <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> y <a title="StringBuffer" href="http://www.w3api.com/wiki/Java:StringBuffer">StringBuffer</a>. Aunque de momento nos centraremos en la primera.
</p>

<p class="texto">
  Para encontrar la clase <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> dentro de las librerías de <a title="Java" href="http://www.manualweb.net/tutorial-java/">Java</a> tendremos que ir a <span class="codigo"><a title="java.lang.String" href="http://www.w3api.com/wiki/Categor%C3%ADa:Java_Lang">java.lang.String</a></span>
</p>

### Creando una cadena

<p class="texto">
  Para crear una cadena tenemos dos opciones:
</p>

*   Instanciamos la clase [String][1]. Que sería una creación explicita de la clase

<pre>String sMiCadena = new String("Cadena de Texto");</pre>

*   Crear implícitamente la cadena de texto. Es decir, simplemente le asignamos el valor al objeto.

<pre>String sMiCadena = "Cadena de Texto";</pre>

<p class="texto">
  En este caso, <a title="Java" href="http://www.manualweb.net/tutorial-java/">Java</a>, creará un objeto <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> para tratar esta cadena.
</p>

### Crear una cadena vacía

<p class="texto">
  Podemos tener la necesidad de crear una cadena vacía. Puede darse el caso que no siempre sepamos lo que vamos a poner de antemano en la cadena de texto. ¿A quién no le surgen dudas? ;-) ... Fuera de bromas, muchas veces la cadena de texto nos la proporcionará el usuario, otro sistema,....
</p>

<p class="texto">
  Para poder crear la cadena vacía nos bastará con asignarle el valor de "", o bien, utilizar el constructor vacío.
</p>

<pre>String sMiCadena = "";
String sMiCadena = new String();</pre>

### Constructores String

<p class="texto">
  Visto lo visto podemos resumir que tenemos dos tipos de constructores principales de la clase <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a>:
</p>

*   **String(),** <span style="font-weight: normal">q</span><span style="font-weight: normal">ue construirá un objeto <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> sin inicializar.</span>
*   **String(String original),** <span style="font-weight: normal">construye una clase <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> con otra clase <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a> que recibirá como argumento.</span>

<p class="texto">
  Aunque tenemos alguno más que iremos viendo....
</p>

### Volcando una cadena de texto a la consola

<p class="texto">
  Solo nos quedará saber cómo volcar una cadena por pantalla. Esto lo haremos con la clase <span class="codigo"><a title="System.out" href="http://www.w3api.com/wiki/Java:System.out">System.out.println</a></span> que recibirá como parámetro el objeto <a title="String" href="http://www.w3api.com/wiki/Java:String">String</a>.
</p>

<p class="texto">
  Por ejemplo:
</p>

<pre>System.out.println("Mi Cadena de Texto");</pre>

<p class="texto">
  ó
</p>

<pre>String sMiCadena = new String("Mi Cadena de Texto");
System.out.println(sMiCadena);</pre>

 [1]: http://www.w3api.com/wiki/Java:String "String"