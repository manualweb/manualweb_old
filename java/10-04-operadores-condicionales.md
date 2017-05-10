---
ID: 1547
post_title: 10.04 – Operadores Condicionales
author: Víctor Cuervo
post_date: 2017-05-10 12:00:40
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/java/operadores-condicionales/
published: true
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
Los operadores condicionales en [Java][1] son aquellos que evalúan dos expresiones booleanas.

Dentro de los operadores condicionales en [Java][1] tenemos:

| Operador   | Descripción               |
| ---------- | ------------------------- |
| &&         | Operador condicional AND  |
|            | | Operador condicional OR |
| ?:         | Operador Ternario         |
| instanceof | Operador instanceof       |

### Operadores Condicionales

La estructura de los operadores condicionales en [Java][1] es:

<pre><code class="java">(expresión_booleana1 && expresión_booleana2)
(expresión_booleana1 || expresión_booleana2)
</code></pre>

En el caso del **operador condicional AND** el resultado será **true** siempre y cuando las dos expresiones evaluadas sean **true**. Si una de las expresiones es **false** el resultado de la expresión condicional AND será **false**.

Para el **operador condicional OR** el resultado será **true** siempre que alguna de las dos expresiones sea **true**.

Los operadores booleanos funcionan mediante la ***evaluación por cortocircuito***. Es decir, que dependiendo del valor de la expresión 1 puede que no sea necesario evaluar la expresión 2.

Para el caso del **operador condicional AND**, si la primera expresión es **false** ya devuelve **false** sin evaluar la segunda expresión. Y en el caso del **operador condicional OR** si la primera expresión es **true** ya devuelve **true** sin evaluar la segunda expresión.

Podríamos ver el uso de los operadores condicionales en el siguiente código:

<pre><code class="java">int vble1 = 5;
int vble2 = 3;

if ((vble1 == 5) && (vble2 ==3))
  System.out.println(“Las dos variables mantienen sus valores iniciales”);

if ((vble1 == 5) || (vble2 ==3))
  System.out.println(“Al menos una variable mantiene su valor inicial”);
</code></pre>

### Operador Ternario

El **operador ternario** es otro de los operadores condicionales. Es una forma reducida de escribir un **if-then-else**. El **operador ternario** es representado mediante el símbolo **?:**

La estructura del operador ternario es:

<pre><code class="java">(expresion)?valor_true:valor_false;
</code></pre>

En el caso de que la expresión tenga un valor de **true** se retorna el valor indicado después del cierre de interrogación (?) Y si la expresión tiene un valor de **false** se retorna el valor que esté después de los dos puntos (:).

El **operador ternario** se suele utilizar para decidir que valor asignar. Un ejemplo de código del operador ternario sería:

<pre><code class="java">int vble1 = 5;
int vble2 = 4;
int mayor;

mayor = (vble1 &gt; vble2)?vble1:vble2;

System.out.println(“El mayor de los dos numeros es “ + mayor);
</code></pre>

Vemos que si la variable 1 es mayor que la variable 2 guardaremos el valor de la variable 1 en la variable mayor. En caso contrario se guardaría el valor de la variable 2, ya que en ese caso sería la mayor.

### Operador instanceof

El **operador instanceof** es un operador especial para los objetos. Mediante el **operador instanceof** podemos comprobar si un objeto es de una clase concreta.

La estructura del **operador instanceof** es:

<pre><code class="java">objeto instanceof clase
</code></pre>

El operador instanceof devolverá true siempre y cuando el objeto sea del tipo clase o de alguna de las clases de las que herede.

Así podríamos definir una secuencia de clases:

<pre><code class="java">class Poligono {}
interface Figura {}
class Triangulo extends Poligono implements Figura {}
</code></pre>

Ahora definimos un par de objetos:

<pre><code class="java">Poligono p = new Poligono();
Triangulo t = new Triangulo();
</code></pre>

Podemos, mediante el uso del **operador instanceof**, comprobar que t es instancia de tipo Triangulo, Poligono y Figura. Mientras que p es instancia de tipo Polígono, pero no de Triangulo, ni Figura.

<pre><code class="java">System.out.println("p es instancia de ");
if (p instanceof Poligono)
  System.out.println("Poligono");
if (p instanceof Triangulo)
    System.out.println("Triangulo");
if (p instanceof Figura)
    System.out.println("Figura");

System.out.println("t es instancia de ");
if (t instanceof Poligono)
    System.out.println("Poligono");
if (t instanceof Triangulo)
    System.out.println("Triangulo");
if (t instanceof Figura)
    System.out.println("Figura");
</code></pre>

 [1]: http://www.manualweb.net/tutorial-java/