---
ID: 1557
post_title: 12 – Sentencias de Control
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1557
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
Un programa en [Java][1] se ejecuta en orden desde la primera sentencia hasta la última.

Si bien existen las **sentencias de control de flujo** las cuales permiten alterar el fujo de ejecución para tomar decisiones o repetir sentencias.

Dentro de las **sentencias de control de flujo** tenemos las siguientes:

*   Sentencias de decisión
*   Sentencias de bucle
*   Sentencias de ramificación

### Sentencias de Decisión

Son sentencias que nos permiten tomar una decisión para poder ejecutar un bloque de sentencias u otro.

Las sentencias de decisión son: `if-then-else` y `switch`.

Mediante `if-then-else` podremos evaluar una decisión y elegir por un bloque u otro.

<pre><code class="java">if (expresion) {
  // Bloque then
} else {
  // Bloque else
}
</code></pre>

Mientras que con `switch` podremos evaluar múltiples decisiones y ejecutar un bloque asociado a cada una de ellas.

<pre><code class="java">switch (expresion) {
  case valor1:
    bloque1;
    break;
  case valor2:
    bloque2;
    break;
  case valor3:
    bloque3;
    break;
  …
  default:
      bloque_por_defecto;
}
</code></pre>

### Sentencias de Bucle

Las **sentencias de bucle** nos van a permitir ejecutar un bloque de sentencias tantas veces como queramos, o tantas veces como se cumpla una condición.

En el momento que se cumpla esta condición será cuando salgamos del bucle.

Las sentencias de bucle en [Java][1] son: `while`, `do-while` y `for`.

En el caso de la sentencia `while` tenemos un bucle que se ejecuta mientas se cumple la condición, pero puede que no se llegue a ejecutar nunca, si no se cumple la condición la primera vez.

<pre><code class="java">while (expresion) {
  bloque_sentencias;
}
</code></pre>

Por otro lado, si utilizamos `do-while`, lo que vamos a conseguir es que el bloque de sentencias se ejecute, al menos, una vez.

<pre><code class="java">do {
  bloque_sentencias;
} while (expresion)
</code></pre>

La sentencia `for` nos permite escribir toda la estructura del bucle de una forma más acotada. Si bien, su cometido es el mismo.

<pre><code class="java">for (sentencias_inicio;expresion;incremento) {
  bloque_sentencias;
}
</code></pre>

### Sentencias de ramificación

Las **sentencias de ramificación** son aquellas que nos permiten romper con la ejecución lineal de un programa.

El programa se va ejecutando de forma lineal, sentencia a sentencia. Si queremos romper esta linealidad tenemos las **sentencias de ramificación**.

Las **sentencias de ramificación** en [Java][1] son: `break` y `continue`.

En el caso de `break` nos sirve para salir de bloque de sentencias, mientras que `continue` sirve para ir directamente al siguiente bloque.

 [1]: http://www.manualweb.net/tutorial-java/