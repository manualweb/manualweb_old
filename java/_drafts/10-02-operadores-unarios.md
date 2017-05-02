---
ID: 1553
post_title: 10.02 – Operadores Unarios
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1553
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
Los operadores unarios son aquellos que solo requieren un operando para funcionar.

Los **operadores** unitarios que tenemos en [Java][1] son:

| Operador | Descripción                                                      |
| -------- | ---------------------------------------------------------------- |
| +        | Operador unario suma. Indica un número positivo.                 |
| -        | Operador unario resta. Niega una expresión.                      |
| ++       | Operador de incremento. Incrementa el valor en 1.                |
| --       | Operador de decremento. Decrementa el valor en 1.                |
| !        | Operador de complemento lógico. Invierte el valor de un booleano |

### Operadores unarios suma o resta

Los operadores unitarios de suma o resta son muy sencillos de utilizar. En el caso del operador unitario suma su uso es redundante. Con el operador unitario resta podemos invertir un valor.

Por ejemplo podríamos tener el siguiente código:

<pre><code class="java">int valor = 2;
System.out.println(-valor); // Imprimirá por pantalla un -2
</code></pre>

### Operadores de incremento y decremento

Los operadores de incremento se pueden aplicar como prefijo o como sufijo.

<pre><code class="java">++ variable;
variable ++;
-- variable;
variable --;
</code></pre>

En todos los casos el valor de la variable acabará con una unidad más (para el operador de incremento) o con una unidad menos (para el operador de decremento).

Si bien si están participando en una asignación hay que tener cuidado en si utilizamos el operador como prefijo o como sufijo.

En el caso de utilizarlo como prefijo el valor de asignación será el valor del operando más el incremento de la unidad. Y si lo utilizamos como sufijo se asignará el valor del operador y luego se incrementará la unidad sobre el operando.

Es más sencillo verlo en código:

<pre><code class="java">suma = ++vble1;
</code></pre>

Sería lo mismo que poner

<pre><code class="java">vble1 = vble1 + 1;
suma = vble1;
</code></pre>

Mientras que si escribimos:

<pre><code class="java">suma = vble1++;
</code></pre>

Sería lo mismo que poner:

<pre><code class="java">suma = vble1;
vble1 = vble1 + 1;
</code></pre>

Exactamente lo mismo le sucede al operador de decremento, pero restando una unidad.

### Operador de complemento lógico

El operador de complemento lógico sirve para negar un valor lógico. Se suele utilizar delante de una operación de evaluación booleana. Normalmente en sentencias de decisión o bucles.

La estructura es:

<pre><code class="java">! (expresión)
</code></pre>

Si la expresión era un **true** la convierte en **false** y si era **false** la convierte en **true**.

Podemos verlo en el siguiente ejemplo:

<pre><code class="java">int vble1 = 2;
int vble2 = 3;

if !(vble1 &gt; vble2)
    System.out.println(“variable 1 es más pequeña que la variable 2);
</code></pre>

Como podemos observar el valor de la expresión evaluada es convertido.

 [1]: http://www.manualweb.net/tutorial-java/