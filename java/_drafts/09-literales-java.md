---
ID: 1541
post_title: 09 – Literales Java
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1541
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
### ¿Qué son los literales Java?

Los valores literales son aquellos que podemos asignar a las variables. Dependiendo del tipo de variable podremos asignar unos valores u otros.

### Literales de enteros

Los enteros que podemos utilizar serán **byte**, **short**, **int** y **long**. Los literales que les asignemos siempre será un número entero.

<pre><code class="java">byte variableByte = 12;
short variableShort = 12;
int variableInt = 12;
long variableLong = 12;
</code></pre>

Si bien para el caso del tipo **long** podemos crear literales de enteros que acaben en L (mayúscula o minúscula, aunque por legilibilidad se recomienda la primera)

<pre><code class="java">long variableLong = 12D;
</code></pre>

Hay otros valores que pueden ser manejados por los literales enteros, para cuando representemos el número en diferentes bases. Por ejemplo cuando los manejemos como binarios o hexadecimales. Para este caso habrá que manejar literales de enteros que tengan dicho formato.

<pre><code class="java">int variableBinaria = 011010;
int variableHexadecimal = 0x1a;
</code></pre>

### Literales de decimales

Los dos tipos de datos de decimales que podemos manejar son **float** y **double**. Para estos casos la representación del literal de decimales serán con separación de un punto entre la parte entera y la parte decimal.

<pre><code class="java">float variableFloat = 12.2;
double variableDouble = 12.2;
</code></pre>

De igual manera podemos utilizar las letras F o f para el tipo de dato **float** y D o d para el tipo de dato **double**. Siempre, por legilibilidad se recomienda la letra en mayúsculas.

<pre><code class="java">float variableFloat = 12.2F;
double variableDouble = 12.2D;
</code></pre>

### Literales de caracteres y cadenas

Tanto los caracteres del tipo de dato **char**, como las cadenas del tipo de datos **String** contienen caracteres Unicode UTF-16.

Los caracteres UTF-16 se pueden escribir directamente en la cadena o si nuestro editor de textos no nos permite el manejo de esa codificación los podemos poner escapados en el formato.

<pre><code class="java">'uCODIGOUNICODE'
</code></pre>

Por ejemplo la letra como la ñ se escaparía de la siguiente forma:

<pre><code class="java">'u00F1'
</code></pre>

Para utilizarla en una cadena de texto “España” podríamos poner

<pre><code class="java">String pais = "Espau00F1a";
</code></pre>

Para los caracteres utilizaremos comillas simples para delimitarlos, mientras que para las cadenas utilizaremos comillas dobles.

<pre><code class="java">char variableChar = ‘a’;
String variableString = “cadena”;
</code></pre>

Además en las cadenas podemos utilizar una serie de secuencias de escape, las cuales empiezan por una barra invertida y siguen con un modificador:

| Secuencia | Significado       |
| --------- | ----------------- |
| b         | retroceso         |
| t         | tabular la cadena |
| n         | salto de línea    |
| f         | form feed         |
| r         | retorno de carro  |
| \'        | comilla simple    |
| \"        | comilla doble     |
| \\        | barra invertida   |

### Literales subrayados

A partir de la versión 1.7 de [Java][1] se puede utilizar el subrayado para realizar separaciones entre números para una mejor visualización.

A todos los efectos el valor del número es como si no existiese el carácter de subrayado.

<pre><code class="java">long tarjetaCredito = 1234_5678_9012_3456L;
long mascaraBinaria = 0b11010010_01101001_10010100_10010010;
</code></pre>

No podremos utilizar el literal de subrayado al principio o final del número, alrededor de un punto decimal, ni entre el número y un literal de entero o decimal (D, F o L).

 [1]: http://www.manualweb.net/tutorial-java/