---
ID: 1549
post_title: >
  10.03 – Operadores Igualdad y
  Relacionales
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1549
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
Los operadores de igualdad y relacionales en [Java][1] son aquellos que nos permiten comparar el contenido de una variable contra otra atendiendo a si son variables con un valor igual o distinto o bien si los valores son mayores o menores.

El listado de operadores de igualdad y relacionales en [Java][1] es:

| Operador | Descripción       |
| -------- | ----------------- |
| ==       | igual a           |
| !=       | no igual a        |
| >        | mayor que         |
| >=       | mayor o igual que |
| <        | menor que         |
| <=       | menor o igual que |

### Operadores de Igualdad

Mediante los operadores de igualdad podemos comprobar si dos valores son iguales **(operador ==)** o diferentes **(operador !=)**.

La estructura de los **operadores de igualdad** es la siguiente:

<pre><code class="java">vble1 == vble2
vble1 != vble2
</code></pre>

Podemos utilizar estos operadores de igualdad en [Java][1] de la siguiente forma:

<pre><code class="java">int vble1 = 5;
int vble2 = 3;

if (vble1 == vble2)
  System.out.println(“Las variables son iguales”);

if (vble1 != vble2)
  System.out.println(“Las variables son distintas”);
</code></pre>

### Operadores relacionales

Permiten comprobar si un valor es mayor que **(operador >)**, menor que **(operador <)**, mayor o igual que **(>=)** y menor o igual que **(<=)**.

Al final el operador lo valida entre dos valores o variables con la estructura:

<pre><code class="java">vble1 &gt; vble2
vble1 &lt; vble2
vble1 &lt;= vble2
vble1 &lt;= vble2
</code></pre>

De esta forma podemos tener un código fuente que nos ayude a realizar estas validaciones de relación:

<pre><code class="java">int vble1 = 5;
int vble2 = 3;

if (vble1 &gt; vble2)
  System.out.println(“La variable 1 es mayor que la variable 2”);

if (vble1 &lt; vble2)
  System.out.println(“La variable 1 es menor que la variable 2”);

if (vble1 &gt;= vble2)
  System.out.println(“La variable 1 es mayor o igual que la variable 2”);

if (vble1 &lt;= vble2)
  System.out.println(“La variable 1 es menor o igual que la variable 2”);
</code></pre>

 [1]: http://www.manualweb.net/tutorial-java/