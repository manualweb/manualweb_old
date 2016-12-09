---
ID: 236
post_title: '03 &#8211; Applets en Java'
author: Víctor Cuervo
post_date: 2010-05-23 23:27:19
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/java/applets-en-java/
published: true
nombreforo:
  - Java Applet
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/java-applet
urlcharla:
  - https://www.facebook.com/groups/java.es/
urlcurso:
  - >
    http://www.aulaprogramacion.com/mod/page/view.php?id=11
urlmanual:
  - http://www.manualweb.net/tutorial-java/
---
<!--TOC-->
<h3>¿Qué es un applet?</h3>
Un applet es una pequeña aplicación java, la cual esta disponible en un servidor web del cual nos la descargamos y ejecutamos dentro de una página web.

Algunas de sus características son:
<ul>
	<li><strong>Tamaño pequeño</strong>, esto es debido a que se requiere su descarga a través de la red. Aunque existen applets de gran tamaño.</li>
	<li><strong>Uso de interfaces gráficos</strong>, utiliza las clases AWT y Swing, las cuales dotan al interface del applet de una gran versatilidad y operabilidad para el usuario.</li>
	<li>...</li>
</ul>
Podríamos decir que es un componente, ya que va a ir incluido dentro de otras aplicaciones.
<h3>Creando un applet</h3>
Lo primer que hay que tener en cuenta es que la definición de los applet se encuentra dentro de la librería <a title="java.applet" href="http://w3api.com/wiki/Categor%C3%ADa:Java_Applet">java.applet</a>, la cual deberemos de importar para poder utilizarla. Además necesitaremos de la librería <a title="java.awt" href="http://w3api.com/wiki/Categor%C3%ADa:Java_AWT">java.awt</a> que es la que gestionará los recursos gráficos que se incluyan dentro del applet.

La librería <a title="java.applet" href="http://w3api.com/wiki/Categor%C3%ADa:Java_Applet">java.applet</a> cuenta con una clase abstracta Applet, de la que deberemos de heredar en la clase principal de nuestra aplicación.
<pre lang="java">import java.applet.*;
public class miApplet extends Applet {
  //variables y métodos
}</pre>
<h3>Ciclo de vida del applet</h3>
Un applet de java pasa por diversos estados:
<ol>
	<li>El applet se carga por primera vez, es decir, se inicializa. Esto sucede cuando el usuario entra en la página por primera vez.</li>
	<li>Seguidamente el applet empieza a funcionar.</li>
	<li>En el caso de que el usuario abandone la página, para desaplazarse a otra, lo que se hace es detener al applet, pero no descargarlo de memoria.</li>
	<li>Si el usuario recarga la página donde se encuentra el applet, este se descarga de memoria el applet actual y sus recursos asociados. Posteriormente se carga una nueva instancia del applet.</li>
	<li>Cuando se cierra el navegador o la aplicación que visualiza el applet, se detiene la ejecución y se libera el applet de memoria.</li>
</ol>
Cada uno de los estados lleva asociado un método:
<pre lang="java">public void init ( ) { … }</pre>
Este método se llama cuando se inicializa el applet por primera vez. En este método es aconsejable fijar el tamaño (ancho y alto) del applet. Además se suelen instanciar los elementos que utilice el applet, ya sean botones, cajas de texto, imágenes,...
<pre lang="java">public void start ( ) { … }</pre>
Es el método que arranca la ejecución del applet cada vez que se visita, siempre y cuando el applet esté expuesto a la visión del usuario.
<pre lang="java">public void stop ( ) { … }</pre>
Para la ejecución del applet. Se ejecuta cuando el applet desaparece de la pantalla.
<pre lang="java">public void destroy ( ) { … }</pre>
Destruye el applet cuando este ya no se vaya a utilizar. En este método deberemos de poner a null todas las variables que maneje el applet para que puedan ser descargadas de memoria por el Garbage Collector (GC), que es el encargado de liberar memoria dentro de la JVM (Java Virtual Machine).
<blockquote>Estos métodos al heredarlos no hacen nada, es por ello que deben de ser sobrecargados para dotarles de funcionalidad.</blockquote>
Otros métodos que utiliza el applet son:
<pre lang="java">public void paint (Graphics g) { … }</pre>
Este método se ejecuta cada vez que el área de dibujo del applet es refrescada, ya sea porque es la primera vez que se visualiza el applet, porque el usuario ha movido el applet por la pantalla, porque se ha redimensionado el navegador,.... Inicialmente, el área de dibujo es un rectángulo gris.
<pre lang="java">public void update (Graphics g ) { … }</pre>
Esta función es la que realmente se llama cuando se refresca el área de dibujo del applet. Lo que hace es limpiar el área de dibujo y llamar a paint. Si estamos realizando aplicaciones que trabajen con gráficos, veremos que esta función habrá que sobrecargarla para que la pantalla no parpadee.
<pre lang="java">public void repaint ( ) { … }</pre>
Una llamada a este método fuerza a la actualización del applet, es decir, se llama a su método update.
<h3>Mi primer applet</h3>
En nuestro primer applet, lógicamente, deberemos de codificar la aplicación que nos muestre la cadena de texto "Hola Mundo". Veamos el código:
<pre lang="java">import java.awt.*;
import java.applet.*;

public class miApplet extends Applet {
  public void paint (Graphics g) {
    g.drawString("Hola Mundo",30,30);
  }
}</pre>
<h3>Código HTML de un applet</h3>
Para poder visualizar un applet dentro de una página web deberemos de introducir su código <a title="HTML" href="http://www.manualweb.net/tutorial-html/">HTML</a> correspondiente, este se referencia mediante la etiqueta .

Esta etiqueta cuenta con una serie de atributos:
<ul>
	<li><strong>code</strong>, indica el fichero .class que representa el applet.</li>
	<li><strong>height</strong>, indica el alto del área donde se representará el applet.</li>
	<li><strong>width</strong>, representa el ancho del área donde se representa el applet.</li>
</ul>
Veamos el código que cargaría el applet codificado anteriormente:

miApplet.html
<pre lang="html4strict"></pre>
<h3>Utilizar el visor de applets (Appletviewer)</h3>
En vez de utilizar un navegador web, podemos visualizar el applet mediante una de las herramientas que se incorpora en el kit de desarrollo de Java SUN. Esta herramienta es el appletviewer. Esta herramienta se ejecutará en línea de comandos. Para poder ver nuestra aplicación deberemos de poner en línea de comandos:
<pre>C:\jdk1.4\bin\appletviewer miApplet.html</pre>