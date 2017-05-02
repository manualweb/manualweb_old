---
ID: 1555
post_title: 12.02 – Setencias de Bucle
author: Víctor Cuervo
post_date: 2017-05-02 17:34:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1555
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
Las **sentencias de bucle** nos van a permitir ejecutar un bloque de sentencias tantas veces como queramos, o tantas veces como se cumpla una condición.

Las **sentencias de bucle** en [Java][1] son: `while`, `do-while` y `for`.

### while

La estructura repetitiva `while` realiza una primera evaluación antes de ejecutar el bloque. Si la expresión es `true` pasa a ejecutar de forma repetida el bloque de sentencias.

Cada vez que termina de ejecutar el bloque de sentencias vuelve a evaluar la expresión. Si la expresión sigue siendo `true` vuelve a ejecutar el bloque. En el caso de que la expresión sea `false` se saldrá del bucle.

Es por ello que dentro del bloque de sentencias *deberán de existir sentencias que modifiquen la evaluación de la expresión, ya que de no hacerse se podría entrar en un bucle infinito*.

La estructura de la sentencia `while` es la siguiente:

<pre><code class="java">while (expresion) {
  bloque_sentencias;
}
</code></pre>

Los casos de uso de una sentencia repetitiva `while` son variados, pero principalmente se utiliza para recorrer estructuras de datos o tener contadores.

Por ejemplo podemos realizar un contador de 1 a 10 de la siguiente forma:

<pre><code class="java">int contador = 1;
while (contador &lt;= 10) {
  System.out.println(contador);
  contador++;
}
</code></pre>

### do-while

En el caso de la estructura repetitiva `do-while` el funcionamiento es el mismo que el de `while`. Pero con una diferencia, primero se ejecuta el bloque de sentencias y luego se evalua la expresión. Por lo tanto siempre se ejecutará, al menos una vez, el bloque de sentencias.

La estructura de la sentencia `do-while` es:

<pre><code class="java">do {
  bloque_sentencias;
} while (expresion)
</code></pre>

Al igual que anteriormente, en el bloque de sentencias deberemos de modificar alguna de las condiciones de la expresión para poder salir del bucle.

Un ejemplo claro del bucle `do-while` sería el ejemplo en el que le pedimos al usuario que introduzca números por teclado, los cuales mostraremos en forma de eco por pantalla, hasta que introduzca el cero. En ese caso saldremos del bucle.

Utilizaremos la estructura `do-while` en vez de la `while` ya que al menos vamos a pedirle al usuario un número.

El código sería el siguiente:

<pre><code class="java">Scanner reader = new Scanner(System.in);        
int iNumero;

do {
    System.out.println("Introduce carácter por consola");
    iNumero = reader.nextInt();
    System.out.println(iNumero);
} while (iNumero &lt;&gt; 0);
</code></pre>

En el caso de haberlo realizado con un bucle `while` tendríamos que repetir la captura y salida de datos. Veamos como quedaría para que puedas ver las diferencias.

<pre><code class="java">Scanner reader = new Scanner(System.in);        
int iNumero;

System.out.println("Introduce carácter por consola");
iNumero = reader.nextInt();
System.out.println(iNumero);

while (iNumero &lt;&gt; 0) {
  System.out.println("Introduce carácter por consola");
  iNumero = reader.nextInt();
  System.out.println(iNumero);
}
</code></pre>

### for

Otra de las sentencias repetitivas que tenemos, a parte de los bucles `while` y `do-while`, es la sentencia `for`.

La sentencia `for` tiene la característica de que tiene bien definido el inicio del bloque, la evaluación de la expresión, el incremento de valor y el bloque de sentencias.

La estructura del bucle `for` es:

<pre><code class="java">for (sentencias_inicio;expresion;incremento) {
  bloque_sentencias;
}
</code></pre>

Tanto las sentencias_inicio, expresión como incremento son opcionales y pueden estar o no. Aunque normalmente aparecerán en la estructura.

Esta estructura la podríamos reproducir mediante una sentencia while de la siguiente forma:

<pre><code class="java">sentencias_inicio;
while (expresion) {
  bloque_sentencias;
  incremento;
}
</code></pre>

Las funcionalidades en las que utilizaremos la sentencia `for` serán las mismas que las sentencias `while` y `do-while`, que serán contadores, recorrer estructuras,...

Si queremos definir un contador de 1 a 10 mediante una sentencia `for` utilizaremos el siguiente código:

<pre><code class="java">for (int x=1;x&lt;=10;x++=) {
  System.out.println(“Valor del contador: “ + x);
}
</code></pre>

En pantalla obtendremos el siguiente resultado:

<samp>Valor del contador: 1 Valor del contador: 2 Valor del contador: 3 Valor del contador: 4 Valor del contador: 5 Valor del contador: 6 Valor del contador: 7 Valor del contador: 8 Valor del contador: 9 Valor del contador: 10</samp>

 [1]: http://www.manualweb.net/tutorial-java/