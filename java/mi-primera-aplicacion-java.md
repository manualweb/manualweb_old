---
ID: pdte
post_title: '01 &#8211; Mi primera aplicación Java'
author: Víctor Cuervo
post_date: 2017-04-10 12:01
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/java/mi-primera-aplicacion-java/
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
<!--TOC-->

### Empezando con Java Me siento ante el ordenador y pienso que voy a escribir mi primera aplicación Java. ¿Cómo? ¿Qué necesito? ¿Por dónde empiezo?...... (las dudas me asaltan). No te preocupes, para eso estamos nosotros. La verdad es que cualquier libro que se precie empezaría con una introducción tediosa de las características del lenguaje que vamos a estudiar. Yo no voy ha hacer eso. No porque este en contra de las introducciones, sino porque me encuentro incapaz de escribir, por el momento, una. Si bien, no me quito de la mete la idea de explicar las características del lenguaje java, las cuales, nos aclararan un poco más las sutilezas de este lenguaje. Antes de crear mi primer programa en Java deberé de asegurarme que tengo en el equipo el siguiente software:

*   Un editor de textos (Por ejemplo, el bloc de notas de Windows, [Wim][1], [AM-Notebook][2], [Win32Pad][3], [EditPad Lite][4], [NotePad2][5],...)
*   El compilador de Java Supongo que el primero, por descontado, lo tendréis a mano. O, al menos, algo similar. Para los usuarios avanzados en el tema les dejare utilizar el UltraEdit y similares. El compilador de java será el que nos permita transformar nuestro código fuente en programas ejecutables. O.... bueno, podríamos decir que en algo similar a programas ejecutables. Ya veremos en que. Para instalarnos el compilador deberemos de descargárnosle de la web de SUN (que son los que se inventaron esto del Java, aunque eso es historia de otro tema). A día de hoy podemos bajarnos la versión 6 del compilador desde

[http://java.sun.com/javase/downloads/index.jsp][6]. De ella nos podemos bajar el kit de desarrollo (Java SE Development Kit) y el entorno de ejecución (Java SE Runtime Environment). La descarga del software la tendremos que hacer desde el SUN Download Manager. <p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/sun_download_manager.png"><img class="size-full wp-image-199 aligncenter" title="sun_download_manager" src="http://www.manualweb.net/wp-content/uploads/2009/09/sun_download_manager.png" alt="sun_download_manager" width="382" height="235" /></a>
</p>

### Proceso de instalación En el proceso de instalación deberemos de introducir algunos datos como el directorio de instalación del compilador y las partes del software que queremos instalar. Entre estas partes podremos elegir las herramientas de desarrollo, el código fuente, las demos y el entorno de ejecución. Es recomendable instalar todas. Más vale que sobre a que falte.

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/java_install.png"><img class="size-full wp-image-204 aligncenter" title="java_install" src="http://www.manualweb.net/wp-content/uploads/2009/09/java_install.png" alt="java_install" width="303" height="231" /></a>
</p>

### Hola Mundo Ahora que tenemos todo el entorno de desarrollo instalado nos lanzamos a desarrollar, ni más, ni menos, que nuestra primera aplicación Java. Lógicamente, nuestra primera aplicación no podría ser otra que “Hola Mundo”. Por si algún despistado todavía no se ha enterado de que va esta aplicación, decirle, simplemente, que es mostrar por pantalla la frase “Hola Mundo”. Complejo, ¿verdad?. El código de nuestra aplicación es el siguiente:

<pre lang="java">public class MiPrimeraAplicacion {
  public static void main (String[] args) {
    System.out.println("Hola Mundo");
  }
}</pre> Este fichero lo guardaremos como

**MiPrimeraAplicacion.java**. Este será nuestro fichero con el código fuente. Deberemos de tener cuidado en cómo escribimos el nombre del fichero ya que Java es un lenguaje sensible a mayúsculas, es decir, que no es lo mismo (ya lo dice Alejandro Sanz) poner miprimeraaplicacion o MiprimeraAplicacion o MIPRIMERAAPLICACION o ... El nombre del fichero deberá de coincidir con el nombre de la clase principal.
<pre>public class MiPrimeraAplicacion &lt;--&gt; MiPrimeraAplicacion.java</pre> La verdad es que a estas alturas de la película no nos vamos a centrar en que significa cada una de las líneas de código. Si bien, no es que haya que ser muy listo, para, al menos, darnos cuenta de que con la sentencia System.out.println se pueden volcar contenidos a la pantalla del ordenador.

### Compilando mi aplicación El compilador de java se llama javac (la c es de compilador, claro). Este no deja de ser un programa ejecutable como otro cualquiera. Para encontrarle y no utilizar las funciones de búsqueda de Windows, podemos dirigirnos a

<pre>C:\Program Files\Java\jdk1.6.0_16\bin</pre> Suponiendo que lo hemos instalado en la unidad C:. E incluso, podemos arriesgarnos a ejecutar el programa.

<pre>C:\Program Files\Java\jdk1.6.0_16\bin\javac</pre>

<p style="text-align: left;">
  A si que veremos algo así por pantalla...
</p>

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/javac.png"><img class="size-full wp-image-207 aligncenter" title="javac" src="http://www.manualweb.net/wp-content/uploads/2009/09/javac.png" alt="javac" width="398" height="323" /></a>
</p> Uff....vaya cantidad de opciones... Para compilar mi aplicación deberé de poner por consola lo siguiente...

<pre>C:\Program Files\Java\jdk1.6.0_16\bin\javac MiPrimeraAplicacion.java</pre> Esta ejecución supone que tenemos el código fuente en el mismo directorio que el compilador, si bien, eso no será lo más corriente. Para poder ejecutar el compilador en cualquier directorio de nuestra máquina deberemos de insertar el directorio donde se ubica el compilador en la variable de entorno PATH. Para ello escribiremos lo siguiente....

<pre>SET PATH = %PATH%;C:\Program Files\Java\jdk1.6.0_16\bin\</pre> Ahora podremos ejecutar el compilador desde cualquier sitio. Así, debería de funcionarnos lo siguiente...

<pre>C:\WORK\Ejemplos1\javac MiPrimeraAplicacion.java</pre>

<p style="text-align: left;">
  Si es que tenemos el código fuente en el directorio C:\WORK\Ejemplos1. La salida por pantalla será la siguiente...
</p>

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/javac2.jpg"><img class="size-full wp-image-208 aligncenter" title="javac2" src="http://www.manualweb.net/wp-content/uploads/2009/09/javac2.jpg" alt="javac2" width="399" height="80" /></a>
</p>

<p style="text-align: left;">
  Vamos que si no nos dice nada de nada es que lo hemos hecho muy bien. En el caso de que hubiéramos metido la pata saldrían cosas como las siguientes...
</p>

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/javacError.jpg"><img class="size-full wp-image-209 aligncenter" title="javacError" src="http://www.manualweb.net/wp-content/uploads/2009/09/javacError.jpg" alt="javacError" width="399" height="98" /></a>
</p> Esto es que el nombre de la clase y del fichero no existe. Múltiples errores se nos pueden producir.

### Ejecutando mi aplicación Una vez que hemos ejecutado correctamente la compilación, sorpresa, no obtenemos un fichero ejecutable, es decir, un .EXE. Y es que llegados a este punto debemos de ver una de las características del lenguaje Java (Si hubiera realizado una introducción no me pasaría esto). Java es un lenguaje multiplataforma. Una de las frases más celebres que proclaman todos los adeptos de Java es

*"write once, run anywhere”*. Esto quiere decir que, una vez creado el fichero fuente y compilado, el resultado (llamémoslo, de momento, nuestro pseudo-fichero ejecutable) lo podemos ejecutar en cualquier otro ordenador. Revisemos algún concepto sobre compiladores. En un proceso de compilación normal seguimos los siguientes pasos: <img class="aligncenter size-full wp-image-210" title="flujo" src="http://www.manualweb.net/wp-content/uploads/2009/09/flujo.jpg" alt="flujo" width="535" height="117" /> Esto nos viene a decir que si yo compilo un programa, por ejemplo, en C, en mi máquina Windows 2000 sobre una plataforma Intel Pentium 4. Solo va a funcionar en maquinas con esa configuración. Si yo llevo mi programa a una máquina con UNIX en una plataforma Solaris no me va a funcionar. ¿Qué hace java para que eso pueda hacerse?. Java, más en concreto los lenguajes interpretados, el compilador genera un código intermedio (más o menos legible). En el caso de Java, el código intermedio se llama Byte Codes. Este código no es dependiente ni del sistema operativo ni de la máquina en el cual lo ejecutamos. En un segundo paso, un interprete, ejecutará dichos Byte Codes en la plataforma que queramos. Es decir, que el interprete ya es especifico del sistema operativo y de la plataforma de ejecución. El esquema quedaría de la siguiente forma... <img class="aligncenter size-full wp-image-211" title="flujo2" src="http://www.manualweb.net/wp-content/uploads/2009/09/flujo2.jpg" alt="flujo2" width="535" height="117" /> <p style="text-align: left;">
  Centrándonos, nuevamente, en nuestra aplicación, encontraremos un fichero .class que será el fichero con los Byte Codes. Hagamos un dir...
</p>

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/dir.jpg"><img class="size-full wp-image-212 aligncenter" title="dir" src="http://www.manualweb.net/wp-content/uploads/2009/09/dir.jpg" alt="dir" width="399" height="130" /></a>
</p> El interprete de dichos ByteCodes se llama java. Lo podemos encontrar en el mismo directorio en el que se encontraba el compilador.

<pre>C:\Program Files\Java\jdk1.6.0_16\bin\</pre> Volvamos a arriesgarnos y ejecutemos el compilador. Recordad que al tener el directorio en la variable de entorno PATH podremos estar en cualquier directorio.

<pre>C:\j2sdk1.4.2_03\bin\java</pre> Este, tiene más opciones que el compilador...

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/javaexe.jpg"><img class="size-full wp-image-213 aligncenter" title="javaexe" src="http://www.manualweb.net/wp-content/uploads/2009/09/javaexe.jpg" alt="javaexe" width="399" height="197" /></a>
</p> Para ejecutar nuestra aplicación escribiremos

<pre>C:\WORK\Ejemplos1\java MiPrimeraAplicacion</pre> Ahhhhhhhhhhhhhhh............ ya me lo he cargado ... Exception in thread “main” java.lang.NoClassDefFoundError ¡y yo con estos pelos! Es normal que la primera vez que ejecutemos nos pueda suceder esto. A si que no nos preocupemos. Esto sucede debido a que el interprete java busca los ficheros .class en los directorios que define la variable de entorno CLASSPATH. Es por ello que si queremos ejecutar una clase que esta en el directorio actual deberemos de tener, al menos, dicho directorio en la variable de entorno. Cuando escribamos aplicaciones más grandes utilizaremos clases creadas por Java, a si que deberemos de tener en el CLASSPATH la ruta de dichas clases. Para solucionar todo este embrollo podemos escribir lo siguiente.

<pre>Set CLASSPATH=.</pre> Notar que el punto hace referencia al directorio actual. Si tu eres una de esas personas que no puede dejar nada fuera de control, te recomiendo que te leas el documento

[Microsoft Windows Installation (32-bit)][7] . Todo lo que siempre quisiste saber sobre la variable CLASSPATH y nunca te atreviste a preguntar. :-) Ahora, ya si que podremos ejecutar nuestra aplicación...
<pre>C:\WORK\Ejemplos1\java MiPrimeraAplicacion</pre> Al fin, el resultado esperado...

<p style="text-align: center;">
  <a href="http://www.manualweb.net/wp-content/uploads/2009/09/MiPrimeraAplicacion.jpg"><img class="size-full wp-image-214 aligncenter" title="MiPrimeraAplicacion" src="http://www.manualweb.net/wp-content/uploads/2009/09/MiPrimeraAplicacion.jpg" alt="MiPrimeraAplicacion" width="398" height="64" /></a>
</p>

 [1]: http://www.vim.org/download.php#pc "Wim"
 [2]: http://aignes.com/notebook.htm "AM-Notebook"
 [3]: http://www.gena01.com/win32pad "Win32Pad"
 [4]: http://www.editpadpro.com/editpadlite.html "EditPadLite"
 [5]: http://www.flos-freeware.ch/notepad2.html "NotePad2"
 [6]: http://java.sun.com/javase/downloads/index.jsp "Descargar Compilador Java"
 [7]: http://java.sun.com/javase/6/webnotes/install/jdk/install-windows.html "Microsoft Windows Installation"
