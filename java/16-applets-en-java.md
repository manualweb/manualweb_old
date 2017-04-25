---
ID: 1296
post_title: 16 – Applets en Java
author: Víctor Cuervo
post_date: 2017-04-10 19:40:56
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/java/applets-en-java/
published: true
nombreforo: Java
urlforo: http://www.dudasprogramacion.com/java/
urlejemplos: http://lineadecodigo.com/categoria/java/feed/
urlvideo: PLLVIhySQmrVbjCFPla5c0OIp6iNWfM-hq
urlmanual: http://www.manualweb.net/tutorial-java/
urltest: http://www.testprogramacion.com/java
urlcurso: http://www.aulaprogramacion.com/java/
gitfolder: java
---

En **Applets en Java** revisaremos: [TOC]

### ¿Qué es un applet?

Un applet es una pequeña aplicación java, la cual esta disponible en un servidor web del cual nos la descargamos y ejecutamos dentro de una página web. Algunas de sus características son:

*   **Tamaño pequeño**, esto es debido a que se requiere su descarga a través de la red. Aunque existen applets de gran tamaño.
*   **Uso de interfaces gráficos**, utiliza las clases AWT y Swing, las cuales dotan al interface del applet de una gran versatilidad y operabilidad para el usuario.
*   ... Podríamos decir que es un componente, ya que va a ir incluido dentro de otras aplicaciones.

### Creando un applet

Lo primero que hay que tener en cuenta es que la definición de los applet se encuentra dentro de la librería

[java.applet][1], la cual deberemos de importar para poder utilizarla. Además necesitaremos de la librería [java.awt][2] que es la que gestionará los recursos gráficos que se incluyan dentro del applet. La librería [java.applet][1] cuenta con una clase abstracta Applet, de la que deberemos de heredar en la clase principal de nuestra aplicación.

<pre>import java.applet.*;
public class miApplet extends Applet {
  //variables y métodos
}</pre>

### Ciclo de vida del applet

Un applet de java pasa por diversos estados:

1.  El applet se carga por primera vez, es decir, se inicializa. Esto sucede cuando el usuario entra en la página por primera vez.
2.  Seguidamente el applet empieza a funcionar.
3.  En el caso de que el usuario abandone la página, para desaplazarse a otra, lo que se hace es detener al applet, pero no descargarlo de memoria.
4.  Si el usuario recarga la página donde se encuentra el applet, este se descarga de memoria el applet actual y sus recursos asociados. Posteriormente se carga una nueva instancia del applet.
5.  Cuando se cierra el navegador o la aplicación que visualiza el applet, se detiene la ejecución y se libera el applet de memoria. Cada uno de los estados lleva asociado un método:

<pre>public void init ( ) { … }</pre>

Este método se llama cuando se inicializa el applet por primera vez. En este método es aconsejable fijar el tamaño (ancho y alto) del applet. Además se suelen instanciar los elementos que utilice el applet, ya sean botones, cajas de texto, imágenes,...

<pre>public void start ( ) { … }</pre>

Es el método que arranca la ejecución del applet cada vez que se visita, siempre y cuando el applet esté expuesto a la visión del usuario.

<pre>public void stop ( ) { … }</pre>

Para la ejecución del applet. Se ejecuta cuando el applet desaparece de la pantalla.

<pre>public void destroy ( ) { … }</pre>

Destruye el applet cuando este ya no se vaya a utilizar. En este método deberemos de poner a null todas las variables que maneje el applet para que puedan ser descargadas de memoria por el Garbage Collector (GC), que es el encargado de liberar memoria dentro de la JVM (Java Virtual Machine).

> Estos métodos al heredarlos no hacen nada, es por ello que deben de ser sobrecargados para dotarles de funcionalidad. Otros métodos que utiliza el applet son:

<pre>public void paint (Graphics g) { … }</pre>

Este método se ejecuta cada vez que el área de dibujo del applet es refrescada, ya sea porque es la primera vez que se visualiza el applet, porque el usuario ha movido el applet por la pantalla, porque se ha redimensionado el navegador,.... Inicialmente, el área de dibujo es un rectángulo gris.

<pre>public void update (Graphics g ) { … }</pre>

Esta función es la que realmente se llama cuando se refresca el área de dibujo del applet. Lo que hace es limpiar el área de dibujo y llamar a paint. Si estamos realizando aplicaciones que trabajen con gráficos, veremos que esta función habrá que sobrecargarla para que la pantalla no parpadee.

<pre>public void repaint ( ) { … }</pre>

Una llamada a este método fuerza a la actualización del applet, es decir, se llama a su método update.

### Mi primer applet En nuestro primer applet, lógicamente, deberemos de codificar la aplicación que nos muestre la cadena de texto "Hola Mundo". Veamos el código:

<pre>import java.awt.*;
import java.applet.*;

public class miApplet extends Applet {
  public void paint (Graphics g) {
    g.drawString("Hola Mundo",30,30);
  }
}</pre>

### Código HTML de un applet

Para poder visualizar un applet dentro de una página web deberemos de introducir su código

[HTML][3] correspondiente, este se referencia mediante la etiqueta . Esta etiqueta cuenta con una serie de atributos: * **code**, indica el fichero .class que representa el applet. * **height**, indica el alto del área donde se representará el applet. * **width**, representa el ancho del área donde se representa el applet. Veamos el código que cargaría el applet codificado anteriormente: miApplet.html

<pre></pre>

### Utilizar el visor de applets (Appletviewer)

En vez de utilizar un navegador web, podemos visualizar el applet mediante una de las herramientas que se incorpora en el kit de desarrollo de Java SUN. Esta herramienta es el appletviewer. Esta herramienta se ejecutará en línea de comandos. Para poder ver nuestra aplicación deberemos de poner en línea de comandos:

<samp>C:jdk1.4binappletviewer miApplet.html</samp>

 [1]: http://w3api.com/wiki/Categor%C3%ADa:Java_Applet "java.applet"
 [2]: http://w3api.com/wiki/Categor%C3%ADa:Java_AWT "java.awt"
 [3]: http://www.manualweb.net/tutorial-html/ "HTML"
