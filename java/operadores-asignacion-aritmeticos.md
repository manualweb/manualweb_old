---
ID: pdte
post_title: 10.01 – Operadores de Asignacion y Aritméticos
author: Víctor Cuervo
post_date: 2017-05-02 18:11
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/java/operadores-asignacion-artimeticos/
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

## Operadores de Asignación y Aritméticos

<a name="asignacion"></a>
### Operador de Asignación

El operador [Java][1] más sencillo es el **operador de asignación**. Mediante este operador se asigna un valor a una variable. El operador de asignación es el símbolo igual.

La estructura del operador de asignación es:

~~~java
variable = valor;
~~~

Así podemos asignar valores a variables de tipo entero, cadena,...

~~~java
int numero = 3;
String cadena = “Hola Mundo”;
double decimal = 4.5;
boolean verdad = true;
~~~

<a name="aritmeticos"></a>
### Operadores Aritméticos

Los operadores aritméticos en [Java][1] son los operadores que nos permiten realizar operaciones matemáticas: ***suma, resta, multiplicación, división y resto***.

Los operadores aritméticos en [Java][1] son:

|Operador|Descripción|
|--|--|
|+|Operador de Suma. Concatena cadenas para la suma de String|
|-|Operador de Resta|
|*|Operador de Multiplicación|
|/|Operador de División|
|%|Operador de Resto|


Los operadores aritméticos en [Java][1] los utilizaremos entre dos literales o variables y el resultado, normalmente lo asignaremos a una variable o bien lo evaluamos.

~~~java
variable = (valor1|variable1) operador (valor2|variable2);
~~~

Así podemos tener los siguientes usos en el caso de que queramos asignar su valor.

~~~java
suma = 3 + 7;             // Retorna 10
resta = 5 - 2;		        // Retorna 3
multiplicación = 3 * 2;	  // Retorna 6
división = 4 / 2;		      // Retorna 2
resto = 5 % 3;		        // Retorna 2
~~~

Ten en cuenta que pueden ser valores o variables:

~~~java
suma = vble1 + 3;		// Sumamos 3 al valor de la variable vble1
resta = vble1 - 4;	// Restamos 4 al valor de la variable vble1
...
~~~~

O podríamos utilizarlo en una condición

~~~java
if (variable > suma + 3) { … }
~~~

En este caso no asignamos el resultado de la suma a una variable, solo lo evaluamos.


[1]: http://www.manualweb.net/tutorial-java/
