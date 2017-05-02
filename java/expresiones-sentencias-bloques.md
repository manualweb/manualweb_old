---
ID: pdte
post_title: 11 – Expresiones, sentencias y bloques
author: Víctor Cuervo
post_date: 2017-05-02 18:14
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/java/expresiones-sentencias-bloques/
published: false
nombreforo: Java
urlforo: http://www.dudasprogramacion.com/java/
urlejemplos: http://lineadecodigo.com/categoria/java/feed/
urlvideo: PLLVIhySQmrVbjCFPla5c0OIp6iNWfM-hq
urlmanual: http://www.manualweb.net/tutorial-java/
urltest: http://www.testprogramacion.com/java
urlcurso: http://www.aulaprogramacion.com/java/
gitfolder: java
---
Un programa en [Java][1] se compone de un conjunto de sentencias que se ejecutan para resolver un problema. Las sentencias son el elemento básico de ejecución de los programa [Java][1].

A parte de las sentencias, en un programa [Java][1] nos encontraremos con expresiones y bloques.

### Expresiones

Una expresión es un conjunto de variables, operadores e invocaciones de métodos que se construyen para poder ser evaluadas retornando un resultado.

Ejemplos de expresiones son:

~~~java
int valor = 1;
if (valor 1 > valor2) { … }
~~~

Cuando tengamos expresiones de evaluación complejas es recomendable que utilicemos paréntesis para saber cual es el orden de ejecución de operaciones.

Ya que si tenemos una expresión como

~~~java
2 + 10 / 5
~~~

No será la misma si ponemos

~~~java
(2 + 10) / 5	ó	2 + (10 / 5)
~~~

En el caso de no utilizar paréntesis se ejecutará el orden de preferencia de operadores. En este caso la división tiene más preferencia que la suma.

### Sentencias

Una sentencia es la unidad mínima de ejecución de un programa. Un programa se compone de conjunto de sentencias que acaban resolviendo un problema. **Al final de cada una de las sentencias encontraremos un punto y coma (;)**.

Tenemos los siguientes tipos de sentencias.

#### Sentencias de declaración

~~~java
int valor = 2;
~~~

#### Sentencias de asignación

~~~java
valor = 2;
~~~

#### Sentencias de incremento o decremento

~~~java
valor++;
~~~

#### Invocaciones a métodos

~~~java
System.out.println(“Hola Mundo”);
~~~

#### Creaciones de objetos

~~~java
Circulo miCirculo = new Circulo(2,3);
~~~

#### Sentencias de control de flujo

~~~java
if (valor>1) { … }
~~~

### Bloques

Un bloque es un conjunto de sentencias los cuales están delimitados por llaves.

~~~java
if (expresión) {
	// Bloque 1
} else {
	// Bloque 2
}
~~~

[1]: http://www.manualweb.net/tutorial-java/
