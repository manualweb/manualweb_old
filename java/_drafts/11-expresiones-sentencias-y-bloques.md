---
ID: 1539
post_title: 11 – Expresiones, sentencias y bloques
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1539
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
Un programa en [Java][1] se compone de un conjunto de sentencias que se ejecutan para resolver un problema. Las sentencias son el elemento básico de ejecución de los programa [Java][1].

A parte de las sentencias, en un programa [Java][1] nos encontraremos con expresiones y bloques.

### Expresiones

Una expresión es un conjunto de variables, operadores e invocaciones de métodos que se construyen para poder ser evaluadas retornando un resultado.

Ejemplos de expresiones son:

<pre><code class="java">int valor = 1;
if (valor 1 &gt; valor2) { … }
</code></pre>

Cuando tengamos expresiones de evaluación complejas es recomendable que utilicemos paréntesis para saber cual es el orden de ejecución de operaciones.

Ya que si tenemos una expresión como

<pre><code class="java">2 + 10 / 5
</code></pre>

No será la misma si ponemos

<pre><code class="java">(2 + 10) / 5    ó   2 + (10 / 5)
</code></pre>

En el caso de no utilizar paréntesis se ejecutará el orden de preferencia de operadores. En este caso la división tiene más preferencia que la suma.

### Sentencias

Una sentencia es la unidad mínima de ejecución de un programa. Un programa se compone de conjunto de sentencias que acaban resolviendo un problema. **Al final de cada una de las sentencias encontraremos un punto y coma (;)**.

Tenemos los siguientes tipos de sentencias.

#### Sentencias de declaración

<pre><code class="java">int valor = 2;
</code></pre>

#### Sentencias de asignación

<pre><code class="java">valor = 2;
</code></pre>

#### Sentencias de incremento o decremento

<pre><code class="java">valor++;
</code></pre>

#### Invocaciones a métodos

<pre><code class="java">System.out.println(“Hola Mundo”);
</code></pre>

#### Creaciones de objetos

<pre><code class="java">Circulo miCirculo = new Circulo(2,3);
</code></pre>

#### Sentencias de control de flujo

<pre><code class="java">if (valor&gt;1) { … }
</code></pre>

### Bloques

Un bloque es un conjunto de sentencias los cuales están delimitados por llaves.

<pre><code class="java">if (expresión) {
    // Bloque 1
} else {
    // Bloque 2
}
</code></pre>

 [1]: http://www.manualweb.net/tutorial-java/