---
ID: 252
post_title: '02 &#8211; Estructuras Selectivas'
author: Víctor Cuervo
post_date: 2010-05-28 21:33:10
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/vbscript/estructuras-selectivas/
published: true
nombreforo:
  - VBScript
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/vbscript
---
<!--TOC-->
Dentro de VBScript nos encontraremos con 2 tipos de estructuras selectivas: if-then-else y case. Las estructuras selectivas nos sirven para discernir el hacer una cosa u otra en base a una o varias condiciones.
<h3>If-Then-Else</h3>
Esta estructura selectiva nos permite elegir entre dos alternativas atendiendo a una condición. Veamos las diferentes formas de expresar la estrucutra:

En el caso de que solo necesitemos evaluar un caso:
<pre lang="vbscript">IF condicion(es) THEN
  accion(es)
END IF</pre>
En el caso de que queramos expresar las dos condiciones:
<pre lang="vbscript">IF condicion(es) THEN
  accion(es)
ELSE
  accion(es)
END IF</pre>
Incluso podemos anidar varias estructuras selectivas:
<pre lang="vbscript">IF condicion(es) THEN
  accion(es)
ELSE IF condicion(es) THEN
  accion(es)
END IF</pre>
<h3>Case</h3>
Esta segunda estructura selectiva podremos realizar diferentes acciones atendiendo a diferentes condiciones. Es decir, que sería como una anidación de estructuras selectivas if. Su estructura será la siguiente:
<pre lang="vbscript">SELECT CASE expresion
CASE valor1
  accion(es)
CASE valor2
  accion(es)
...
CASE ELSE
  accion(es)
END SELECT</pre>
Dependiendo del valor que tome la expresión realizaremos unas u otras acciones. En el caso de que el valor de la expresión no este recogido en el subconjunto de case se realizarán las acciones del case else.
<h3>Ejemplos de Código relacionados</h3>