---
ID: 1551
post_title: 10 – Operadores Java
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1551
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
Los operadores [Java][1] son un conjunto de símbolos que nos permiten realizar operaciones (valga la redundancia) sobre las variables que hayamos definido en nuestro programa.

Mediante los operadores [Java][1] podremos hacer cosas como *asignar un valor a una variable*.

<pre><code class="java">int numero = 3;
</code></pre>

Podremos *sumar un valores a una variable*:

<pre><code class="java">suma = 2 + 3;
</code></pre>

*Incrementar en uno el valor de una variable* de forma sencilla:

<pre><code class="java">valor = x++;
</code></pre>

Saber si *dos valores son iguales o distintos*:

<pre><code class="java">if (x == y) {}
if (x != y) {}
</code></pre>

Permitirnos *comparar valores booleanos*, para tomar una decisión:

<pre><code class="java">if (valor1 && valor2){}
</code></pre>

E incluso *manipular datos binarios*:

<pre><code class="java">(0101) | (0011)
</code></pre>

### Listado de Operadores Java

Los operadores [Java][1] que podemos utilizar en nuestros programas serán los siguientes:

| Operador             | Precedencia                             |
| -------------------- | --------------------------------------- |
| postfix              | expr++ expr--                           |
| unary                | ++expr --expr +expr -expr ~ !           |
| multiplicative       | * / %                                   |
| additive             | + -                                     |
| shift                | << >> >>>                               |
| relational           | < > <= >= instanceof                    |
| equality             | == !=                                   |
| bitwise AND          | &                                       |
| bitwise exclusive OR | ^                                       |
| bitwise inclusive OR | |                                       |
| logical AND          | &&                                      |
| logical OR           | ||                                      |
| ternary              | ? :                                     |
| assignment           | = += -= *= /= %= &= ^= |= <<= >>= >>>=| |

### Tipos de Operadores Java

Para poder entrar en detalle dentro de los operadores [Java][1] vamos a verlos agrupados de la siguiente forme:

*   [Operador de asignación][2]
*   [Operadores aritméticos][3]
*   [Operadores unarios][4]
*   [Operadores igualdad y relacionales][5]
*   [Operadores condicionales][6]
*   [Operadores de bit][7]

 [1]: http://www.manualweb.net/tutorial-java/
 [2]: http://www.manualweb.net/java/operador-asignacion-aritmeticos/#asignacion
 [3]: http://www.manualweb.net/java/operadores-asignacion-artimeticos/#aritmeticos
 [4]: http://www.manualweb.net/java/operadores-unarios/
 [5]: http://www.manualweb.net/java/operadores-igualdad-relacionales/
 [6]: http://www.manualweb.net/java/operadores-condicionales/
 [7]: http://www.manualweb.net/java/operadores-bit/