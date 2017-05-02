---
ID: 1545
post_title: 10.05 – Operadores de Bit
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1545
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
Otros de los operadores que nos ofrece el lenguaje Java son los **operadores de bit**. Estos nos permiten manejar números binarios. Los número binarios podremos operarlos de dos formas. Por un lado de forma que el cálculo se haga bit a bit, bien sea realizando operaciones de AND, OR,... Y por otro desplazamiento de bits.

Veamos en detalle qué operadores hay para el manejo bit a bit y qué operadores hay para el desplazamiento de bits.

| Operador | Descripción                               |
| -------- | ----------------------------------------- |
| &        | Operador bits AND                         |
| ^        | Operador bits OR exclusivo (XOR)          |
| |        | Operador bits OR inclusivo                |
| ~        | Operador Negación Bits (NOT)              |
| <<       | Operador desplazamiento izquierda         |
| >>       | Operador desplazamiento derecha           |
| >>>      | Operador desplazamiento derecha sin signo |

### Operadores de Bit a Bit

La estructura de los operadores de bit a bit es la siguiente

<pre><code class="java">(valor_binario1) & (valor_binario2)
(valor_binario1) ^ (valor_binario2)
(valor_binario1) | (valor_binario2)
</code></pre>

#### Operador AND

El **operador de bit AND** lo que hace es multiplicar los bits de las dos cadenas. Las multiplicaciones de bits dan como resultado que 1 x 1 siempre es 1 y que 1 x 0 y 0 x 0 siempre da 0. El tamaño de la cadena resultado siempre es el mismo al tamaño de las cadenas.

Así de la siguiente operación:

<pre><code class="java">0101 & 0011
</code></pre>

Tendremos que el resultado es:

<pre><code class="java">0101 AND    (decimal 5)
0011          (decimal 3)
--------
0001          (decimal 1)
</code></pre>

#### Operador OR

En el caso del **OR inclusivo (operador |)** lo que se hace es multiplicar los bits asumiendo que 1 multiplicado por 1 o por 0, siempre es 1. Mientras que la única multiplicación que da 0 es 0 x 0.

Así la operación:

<pre><code class="java">(0101) | (0011)
</code></pre>

Dará como resultado:

<pre><code class="java">0101 OR (decimal 5)
0011        (decimal 3)
--------
0111        (decimal 7)
</code></pre>

#### Operador XOR

Para el caso del **OR exclusivo (operador ^) conocido como XOR**. La multiplicación de bits será 1 para los casos 1 x 0 y 0 x 1. Las multiplicaciones 1 x 1 y 0 x 0 siempre darán como resultado 0.

De esta forma si tenemos la operación:

<pre><code class="java">(0101) ^ (0011)
</code></pre>

El resultado que encontraremos será:

<pre><code class="java">0101 XOR    (decimal 5)
0011          (decimal 3)
--------
0110          (decimal 6)
</code></pre>

#### Operador NOT

El **operador de negación de bits** nos permite invertir el contenido de bits de una cadena. De tal manera que invierte los bits convirtiendo los 1 en 0 y los 0 en 1.

En este caso la estructura será:

<pre><code class="java">~ (valor)
</code></pre>

Así podríamos tener la sentencia:

<pre><code class="java">~ (0111)
</code></pre>

La cual se traduciría en:

<pre><code class="java">0111 NOT    (decimal 7)
--------
1000          (decimal 8)
</code></pre>

### Operadores de Desplazamiento de Bits

Los **operadores de desplazamiento de bits** permiten mover los bits dentro de la cadena. La estructura de estos operadores es la siguiente:

<pre><code class="java">(valor_binario1) &lt;&lt; (valor_binario2)
(valor_binario1) &gt;&gt; (valor_binario2)
(valor_binario1) &gt;&gt;&gt; (valor_binario2)
</code></pre>

#### Operador Desplazamiento a Izquierdas

En el caso del desplazamiento a izquierdas, desplaza el valor_binario1 a izquierdas tantas veces como indique el valor_binario2. Los bits se mueven a la izquierda y se añaden tantos ceros como indique el valor_binario 2.

De esta forma el código:

<pre><code class="java">(0011) &lt;&lt; (0001) // Desplaza 0011 una vez dando 110
(0011) &lt;&lt; (0011) // Desplaza 0011 tres veces dando 11000
</code></pre>

#### Operador Desplazamiento a Derechas

Es exactamente igual al operador de desplazamiento a izquierdas, pero con la diferencia que mete dígitos por la izquierda y va eliminado el último dígito.

Si tiene que meter un 1 o tiene que meter un 0 dependerá del valor del bit del signo. Si el valor del bit de signo es positivo (0), lo que hace es insertar 0. Si el valor del bit de signo es negativo (1), lo que hace es insertar 1.

Los ceros o unos a insertar los determinará el valor_binario2 y serán sobre el valor_binario1.

De esta forma podemos ver los códigos

<pre><code class="java">(1100) &gt;&gt; (0001) // Desplaza 1100 una vez dando 0110
(1000) &gt;&gt; (0011) // Desplaza 1100 tres veces dando 0001
</code></pre>

Si manipulamos decimales lo que hacemos es dividir el número por 2 tantas veces como indique su desplazamiento.

<pre><code class="java">12 &gt;&gt; 1     // Sería 12 / 2 = 6
12 &gt;&gt; 2 // Sería 12 / 2 = 6; 6/2 = 3
</code></pre>

Si manejamos valores negativos. Por ejemplo de un elemento Byte (8 bits, con el primero como signo)

<pre><code class="java">1110 0011 &gt;&gt; 0011   // Desplaza tres a la izquierda dejando 1111 1100
</code></pre>

#### Operador Desplazamiento a Derechas sin signo

Es como el operador desplazamiento a derechas pero no tiene en cuenta el signo. Por lo cual siempre mete ceros por la izquierda.

Este operador sería más utilizado si manejamos valores binarios para ejecutar un desplazamiento de bits.

Así podríamos ver el siguiente código:

<pre><code class="java">1110 0011 &gt;&gt;&gt; 0011  // Desplaza tres a la izquierda dejando 0001 1100
</code></pre>