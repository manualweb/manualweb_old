# Tutorial Java

| | |
|---|---|
|autor:|[Víctor Cuervo](http://www.victorcuervo.com)|
|versión:|v0.2|
|fecha:|2017-05-02 18:43|
|url:|http://www.manualweb.net/tutorial-java/|
|github:|https://github.com/victorcuervo/manualweb/tree/master/java|

> Disclamer

## Índice
1. Introducción a Java
2. Historia de Java
3. Tecnologías Java
4. Instalar Java
5. Mi primera aplicación Java

## Introducción a java
[Java][1] es un lenguaje de programación de propósito general, tipado, orientado a objetos,... que permite el desarrollo desde aplicaciones básicas, pasando por aplicaciones empresariales hasta aplicaciones móviles.

[Java][1] nacía como un lenguaje de programación que pudiese ser multiplataforma y multidispositivo, bajo el paradigma *"Write Once Run Anywhere" (WORA)*

De esta forma un programa [Java][1] escrito una vez podemos ejecutarle sobre diferentes plataformas, siendo soportados los sistemas operativos Windows, MacOs y UNIX. Y a su vez en diferentes tipos de dispositivos.

Para poder seguir este paradigma la compilación de un programa [Java][1] no genera código fuente, si no que genera **bytecodes**. Estos **bytecodes** son interpretados por una máquina virtual o **JVM (Java Virtual Machine)**. Dicha máquina ya está escrita para cada uno de los sistemas operativos en cuestión.

### Características del lenguaje Java

Dentro de las características del lenguaje [Java][1] encontramos:

#### Independiente de Plataforma

Cuando compilamos código fuente [Java][1] no se genera código máquina específico, si no que se generan **bytecodes**, los cuales son interpretados por la **Java Virtual Machine (JVM)**, posibilitando que un mismo código fuente pueda ser ejecutado en múltiples plataformas.

#### Orientado a Objetos

Cualquier elemento del lenguaje [Java][1] es un objeto. Dentro de los objetos se encapsulan los datos, los cuales son accedidos mediante métodos.

#### Sencillo

[Java][1] está enfocado para ser un lenguaje fácil de aprender. Simplemente se deberán de entender los conceptos básicos de la programación orientada a objetos (POO).

#### Seguro

Es seguro ya que los programas se ejecutan dentro de la **Java Virtual Machine (JVM)** en un formato de *"caja de arena"*, de tal manera que no pueden acceder a nada que esté fuera de ella.

Tiene una validación sobre los **bytecodes** para comprobar que no hay códigos de fragmento ilegal.

#### Arquitectura Neutral

Independientemente de que se ejecute en una arquitectura de 32bits o de 64bits. En [Java][1] los tipos de datos siempre ocupan lo mismo.

#### Portable

[Java][1] no tiene nada que dependa de la plataforma, lo cual le hace que sea portable a diferentes plataformas.

#### Robusto

El lenguaje [Java][1] intenta controlar las situaciones de error en los procesos de compilación y de ejecución, reduciendo de esta manera el riesgo de fallo.

Además [Java][1] realiza el control total de la memoria alocándola y retirandola mediante un **garbage colletor**, de tal manera que no podemos utilizar punteros para acceder a ella.

#### Multi-hilo

[Java][1] nos permite la programación concurrente, de tal manera que un único programa puede abrir diferentes hilos de ejecución.

#### Interpretado

Los **bytecodes** son interpretados en tiempo real a código máquina.

#### Alto Rendimiento

[Java][1] ofrece compiladores Just-In-Time que permiten tener un alto rendimiento.

#### Distribuido

El lenguaje [Java][1] está pensando para ser ejecutado en arquitecturas distribuidas, como pueda ser Internet.

## Historia de Java

### Los Inicios de Java

El lenguaje [Java][1] fue desarrollado en sus inicios por [James Gosling][2], en el año 1991. Inicialmente [Java][1] era conocido como **Oak** o **Green**.

La primera versión del lenguaje [Java][1] es publicada por [Sun Microsystems][3] en 1995. Y es en la versión del lenguaje JDK 1.0.2, cuando pasa a llamarse [Java][1], corría el año 1996.

En las primeras versiones de *[Java][1] 1.1, 1.2 y 1.3* es en la que el lenguaje va tomando forma, con la inclusión de tecnologías como **JavaBeans**, **JDBC** para el acceso a base de datos, **RMI** para las invocaciones en remoto, **Collections** para la gestión de múltiples estructuras de datos o **AWT** para el desarrollo gráfico, entre otros.

### Java Community Process (JCP)

La versión *[Java][1] 1.4* pasa a ser la primera versión gestionada por la comunidad mediante el **Java Community Process (JCP)**.

Se trabaja con **Java Specification Requests (JSRs)** que son las nuevas funcionalidades que se busca que tenga el lenguaje.

*[Java][1] 1.4* se liberaba como [JSR 59][4], corría el año 2002. ALgunas de las características que contenía eran: **librería NIO** para IO no bloqueante, **JAXP** para el procesado de [XML][5] y [XSLT][6] o el **API para preferencias**.

### Java 5

En 2004 se estaba trabajando con la versión *[Java][1] 1.5*, pero con vistas a reflejar el nivel de madurez de la plataforma [Java][1] se renombra a *[Java][1] 5*.

A partir de este momento se identifica el JDK con la versión 1.x, mientras que la plataforma [Java][1] sigue con la nueva política de versionado.

Así JDK 1.5 corresponde con *[Java][1] 5* , JDK 1.6 corresponde con *[Java][1] 6* ,... y así sucesivamente.

Dentro de *[Java][1] 5* podemos encontrar el uso de **genéricos**, el **autoboxing/unboxing** entre tipos de datos primitivos y sus clases, el uso de **enumerados** y la aparición del bucle `for-each`.

### Java 6

En el año 2006 aparece la versión *[Java][1] 6* en la que podíamos encontrar cosas como el **soporte de lenguajes de script**, facilidades para la exposición y consumo de webservices mediante **JAX-WS**, nuevos tipos de drivers con **JDBC 4** y la versión 2 de **JAXB**.

### Java como Open Source

Una de las cosas que sucede en noviembre 2006 es que [Sun Microsystems][3] lo convierte en Open Source mediante una licencia GNU General Public License (GPL).

Dando lugar en mayo 2008 a lo que se conoce como [OpenJDK][7], con OpenJDK 6.

### Java 7

Llegado julio de 2011 ve la luz *[Java][1] 7*, la cual trae como novedades el **soporte de lenguajes dinámicos**, dotando a la JVM de un soporte de mútiples lenguajes y una **nueva librería I/O para el manejo de ficheros**.

También aparecen cosas menores, pero muy útiles como el **manejo de String dentro de la validación en una estructura switch** o la capacidad de **poner subrayados en los números para que se puedan leer mejor**.

### Versión actual: Java 8

La última versión de Java distribuida es *[Java][1] 8*, aparecida en marzo de 2014.

Entre las características de *[Java][1] 8* tenemos el **soporte expresiones Lambda y uso de Streams**, que permiten un estilo más funcional para los programas [Java][1]. Dentro de este enfoque más funcional también aparecen las **transformaciones MapReduce**.

Ve la luz el *Proyecto Nashorn* para disponer de un engine [Javascript][8] y así poder incluir este lenguaje dentro de las aplicaciones [Java][1].

Otras cosas son un **nuevo API Date y Time** y la inclusión de **JavaFX 8** dentro de la JDK de [Java][1].

### Java 9

Aunque en el roadmap se esperaba que *[Java][1] 9* estuviera disponible para el 2016, los problemas de seguridad encontrados dentro de la plataforma han causado que se vaya demorando.

La fecha prevista para disponer de *[Java][1] 9* es julio 2017.

Dentro de esta versión podremos encontrar el *Project Jigsaw* que establece la **modularización de la JDK**, el **Java Shell** con el que podremos trabajar e interactuar al *estilo RELP (Read–eval–print loop)*, soporte para **http 2.0** y [algunas cosas más][9]

## Tecnologías Java

Dentro de [Java][1] existen diferentes tecnologías de desarrollo, cada una enfocada a un fin diferente, ya sea la base del lenguaje [Java][1], [Java][1] para el ámbito empresarial, [Java][1] para el desarrollo de aplicaciones móviles,...

Cada una de las tecnologías de desarrollo del lenguaje [Java][1] contiene:

1.  Java Virtual Machine (JVM)
2.  API de desarrollo de la plataforma

La aplicación se ejecuta dentro de la *Java Virtual Machine (JVM)* y tiene capacidad de accerder al API, que son las librerías con funcionalidades que nos ofrece [Java][1].

Las tecnologías que existen en la **plataforma [Java][1]** son:

*   Java SE
*   Java EE
*   Java ME
*   Java Card

### Java SE

Java SE es la plataforma estándar y objetivo de este tutorial sobre [Java][1] en la cual se recogen todas las funcionalidades básicas del lenguaje.

Dentro de estas funcionalidades básicas de [Java][1] encontramos: el uso de **colecciones**, acceso a ficheros con **Java IO y NIO** y bases de datos con **JDBC**, librerías para el desarrollo de aplicaciones de escritorio o web como **Swing** o **JavaFX**, librerías para la **fecha y hora**, posibilidad de crear aplicaciones **multi-hilo**, capacidades para realizar **conexiones en red**, manejo de contenido **[XML][5]**... incluso incluye la base de datos **Java DB** para el uso en memoria.

Si estás empezando con [Java][1] lo más normal es que te bajes las librerías de Java SE.

Puedes consultar [todo el contenido de Java SE][10].

### Java EE

Java EE se crea para poder realizar aplicaciones empresariales con [Java][1]. De esta forma se dota a Java EE con capacidades de desarrollo de aplicaciones de servidor con tecnologías como **Servlets**, **JSP** o **EJB**.

Java EE nos permite realizar el desarrollo de servicios, ya sean WSDL (con **JAX-WS**), REST (con **JAX-RS**), o la creación de **websockets**.

Además ofrece un API de persistencia de objetos con **JPA**, capacidades de mensajería con **Java Message**, de email con **Java Mail** o gestión de **procesos batch**.

Puedes consultar [todo el contenido de Java EE][11].

### Java ME

Java ME es la implementación de [Java][1] que nace para la creación de aplicaciones móviles.

Si bien con el paso del tiempo se ha ido enfocando más para el desarrollo de dispositivos *IoT (Internet of Things)*: televisiones, sensores, impresoras,...

Así, dentro de Java ME podemos encontrar:

*   **Java TV**, para el desarrollo de aplicaciones en TV o en dispositivos multimedia.
*   **Java Embedded**, que nos permite crear diferentes perfiles de desarrollo de "aplicaciones incrustadas", que además no tienen interface gráfica.

Puedes encontrar [más información sobre lo que es Java ME][12]

### Java Cards

Es la tecnología de [Java][1] que nos sirve para el desarrollo de aplicaciones que vayan a ir en tarjetas inteligentes, aquellas que llevan un chip y poca capacidad de procesamiento y memoria.

Puedes [leer más sobre Java Cards][13] y las capacidades que ofrece.

## Instalar Java

Para instalarnos el compilador [Java][1] lo primero que deberemos de hacer es descargarlo de la web de Oracle. A día de hoy (*abril 2017*) podemos [bajarnos la versión **Java 8** del compilador desde la web de Oracle][14].

De ella nos podemos bajar el kit de desarrollo (**Java SE Development Kit**) y el entorno de ejecución (**Java SE Runtime Environment**).

> Es importante que si vamos a desarrollar con [Java][1] nos descarguemos el **Java SE Development Kit**

### Proceso de instalación

En el proceso de instalación deberemos de introducir algunos datos como el directorio de instalación del compilador y las partes del software que queremos instalar.

Entre estas partes podremos elegir las *herramientas de desarrollo*, *el código fuente*, *las demos* y el *entorno de ejecución*. Es recomendable instalar todas. Más vale que sobre a que falte.

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/java-install.png" alt="Instalar Kit Desarrollo Java" class="img-responsive" />

Una vez que hayamos confirmado, la instalación empieza a ejecutarse la instalación, por lo que nos aparecerá un progreso de instalación.

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/java-install-progress.png" alt="Instalar Java Progreso" class="img-responsive" />

Cuando se termine la instalación, el programa nos sacará una ventana en la que podremos ver que se ha instalado correctamente y nos permite lanzar los siguientes pasos para empezar con [Java][1]

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/java-install-finish.png" alt="Instalar Kit Desarrollo Java Finalizado" class="img-responsive" />

Ahora podremos ir al directorio en el cual nos ha realizado la instalación. En nuestro caso en:

<samp>C:Program FilesJavajdk1.8.0_131bin</samp>

Y podemos ejecutar un javac, que es el nombre del compilador, para ver que se ha instalado correctamente.

Podremos ver que por pantalla nos aparece algo así:

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/java-install-check.png" alt="Comprobar Instalación Kit Desarrollo" class="img-responsive" />

Ya tendremos el kit de desarrollo de [Java][1] correctamente instalado.

## Mi Primera Aplicación Java

### Primeros Pasos

Empezando con [Java][1] Me siento ante el ordenador y pienso que voy a escribir mi primera aplicación [Java][1]. ¿Cómo? ¿Qué necesito? ¿Por dónde empiezo?...... (las dudas me asaltan). No te preocupes, para eso estamos nosotros.

Antes de crear mi primer programa en [Java][1] deberé de asegurarme que tengo en el equipo el siguiente software:

*  **Un editor de textos** (Por ejemplo, el bloc de notas de Windows, [Wim][15], [AM-Notebook][16], [Win32Pad][17], [EditPad Lite][18], [NotePad2][19],...)

* **El compilador de Java**

Supongo que el primero, por descontado, lo tendréis a mano. O, al menos, algo similar. Para los usuarios avanzados en el tema les dejare utilizar el **Atom**, **Sublime** y similares.

El compilador de [Java][1] será el que nos permita transformar nuestro código fuente en programas ejecutables. O.... bueno, podríamos decir que en algo similar a programas ejecutables. Ya veremos en que.

Siguiendo los pasos que se explican en el artículo [Cómo instalar Java][20] podremos tener nuestro entorno preparado para poder desarrollar nuestra primera aplicación [Java][1]

### Hola Mundo en Java

Ahora que tenemos todo el entorno de desarrollo instalado nos lanzamos a desarrollar, ni más, ni menos, que nuestra primera aplicación Java.

Lógicamente, nuestra primera aplicación no podría ser otra que “Hola Mundo”. Por si algún despistado todavía no se ha enterado de que va esta aplicación, decirle, simplemente, que es mostrar por pantalla la frase “Hola Mundo”. Complejo, ¿verdad?.

El código de nuestra primera aplicación [Java][1] es el siguiente:

~~~java
public class MiPrimeraAplicacion {
  public static void main (String[] args) {
    System.out.println("Hola Mundo");
  }
}
~~~

El fichero lo guardaremos como **MiPrimeraAplicacion.java**. Este será nuestro fichero con el código fuente.

> Deberemos de tener cuidado en cómo escribimos el nombre del fichero ya que [Java][1] es un **lenguaje sensible a mayúsculas**, es decir, que no es lo mismo poner miprimeraaplicacion o MiprimeraAplicacion o MIPRIMERAAPLICACION o ... El nombre del fichero deberá de coincidir con el nombre de la clase principal.

<pre>public class MiPrimeraAplicacion &lt;--&gt; MiPrimeraAplicacion.java</pre>

La verdad es que a estas alturas de la película no nos vamos a centrar en que significa cada una de las líneas de código.

Si bien, no es que haya que ser muy listo, para, al menos, darnos cuenta de que con la sentencia [System.out.println][22] se pueden volcar contenidos a la pantalla del ordenador.

### Uso del compilador javac

El compilador de [Java][1] se llama **javac** (la c es de compilador, claro). Este no deja de ser un programa ejecutable como otro cualquiera.

En el caso de estar en un sistema operativo Windows, el compilador suele estar instalado (si hemos seguido la instalación por defecto) en:

<samp>C:\\Program Files\\Java\\jdk1.8.0_51.jdk\\bin</samp>

Si estamos trabajando con un MacOS podemos ejecutar el comando.

<kbd>/usr/libexec/java_home</kbd>

El cual nos indicará en qué directorio se encuentra instalado [Java][1].

Lo que ya podemos aventurarnos a ejecutar el compilador. Para ello ejecutaremos el programa:

<kbd>javac</kbd>

Al ejecutar el compilador veremos por pantalla algo así:

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/javac.png" alt="Opciones JavaC" class="img-responsive"/>

Uff... vaya cantidad de opciones... No te preocupes por ellas, ya que para compilar mi aplicación deberé de poner por consola lo siguiente...

<kbd>javac MiPrimeraAplicacion.java</kbd>

Esta ejecución supone que tenemos el código fuente en el mismo directorio que el compilador, si bien, eso no será lo más corriente.

### Configurando en Path para Java

Para poder ejecutar el compilador en cualquier directorio de máquinas Windows deberemos de insertar el directorio donde se ubica el compilador en la **variable de entorno PATH**.

Para ello, escribiremos lo siguiente....

<kbd>SET PATH = %PATH%;C:\\Program Files\\Java\\jdk1.8.0_51.jdk\\bin</kbd>

Ahora podremos ejecutar el compilador desde cualquier sitio. Así, debería de funcionarnos lo siguiente...

<kbd>C:\\WORK\\Ejemplos1\\javac MiPrimeraAplicacion.java</kbd>

### Compilando mi primera aplicación Java

Si hemos compilado de forma correcta nuestro programa, simplemente la respuesta por pantalla será la siguiente:

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/javac-compilar.png" alt="Compilar Mi Primera Aplicación Java" class="img-responsive"/>

Vamos que si no nos dice nada de nada es que lo hemos hecho muy bien. En el caso de que hubiéramos metido la pata saldrían cosas como las siguientes...

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/javac-error-compilacion.png" alt="Error al compilar Mi Primera Aplicación Java" class="img-responsive"/>

Esto es que el nombre de la clase y del fichero no existe. Múltiples errores se nos pueden producir.

### Ejecutando mi aplicación

Una vez que hemos ejecutado correctamente la compilación, sorpresa, no obtenemos un fichero ejecutable, es decir, un .exe o similar. Si no que obtenemos un fichero **.class**. En este caso obtendremos un fichero **MiPrimeraAplicacion.class**.

[Java][1] es un lenguaje multiplataforma que está construido bajo el principio de *"write once, run anywhere”*. Esto quiere decir que, una vez creado el fichero fuente y compilado, el resultado (llamémoslo, de momento, nuestro pseudo-fichero ejecutable) lo podemos ejecutar en cualquier otro ordenador.

Revisemos algún concepto sobre compiladores. En un proceso de compilación normal seguimos los siguientes pasos:

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/flujo-compilacion.png" alt="Flujo de Compilacion" class="img-responsive"/>

Esto nos viene a decir que si yo compilo un programa, por ejemplo, en C, en mi máquina Windows 8.1 sobre una plataforma Intel. Solo va a funcionar en maquinas con esa configuración.

Si yo llevo mi programa a una máquina con UNIX en una plataforma Solaris no me va a funcionar. ¿Qué hace [Java][1] para que eso pueda hacerse?.

[Java][1], más concreto, en los lenguajes interpretados, el compilador genera un código intermedio (más o menos legible).

En el caso de [Java][1], el código intermedio se llama **bytecodes**. Este código no es dependiente ni del sistema operativo ni de la máquina en el cual lo ejecutamos.

En un segundo paso, un interprete, ejecutará dichos **bytecodes** en la plataforma que queramos. Es decir, que el interprete ya es especifico del sistema operativo y de la plataforma de ejecución.

El esquema quedaría de la siguiente forma...

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/flujo-compilacion-java.png" alt="Flujo de Compilación Java" class="img-responsive"/>

Centrándonos, nuevamente, en nuestra aplicación, encontraremos un fichero **MiPrimeraAplicacion.class** que será el fichero con los **bytecodes**.

El programa que va a ejecutar dichos **bytecodes** es java. Este programa está en el mismo directorio en el que estaba el compilador.

Volvamos a arriesgarnos y ejecutemos el compilador. Recordad que al tener el directorio en la variable de entorno PATH podremos estar en cualquier directorio.

<kbd>java</kbd>


Este, tiene más opciones que el compilador...

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/java.png" alt="Opciones Java" class="img-responsive"/>

Para ejecutar nuestra aplicación escribiremos

<kbd>java MiPrimeraAplicacion</kbd>

Ahhhhhhhhhhhhhhh............ ya me lo he cargado ... **Exception in thread “main” java.lang.NoClassDefFoundError** ¡y yo con estos pelos!

Es normal que la primera vez que ejecutemos nos pueda suceder esto. A si que no nos preocupemos.

Esto sucede debido a que el interprete java busca los ficheros .class en los directorios que define la variable de entorno **CLASSPATH**.

Es por ello que si queremos ejecutar una clase que esta en el directorio actual deberemos de tener, al menos, dicho directorio en la variable de entorno.

Cuando escribamos aplicaciones más grandes utilizaremos clases creadas por Java, a si que deberemos de tener en el CLASSPATH la ruta de dichas clases. Para solucionar todo este embrollo podemos escribir lo siguiente.

<kbd>set CLASSPATH=.</kbd>

Notar que el punto hace referencia al directorio actual.

Si tu eres una de esas personas que no puede dejar nada fuera de control, te recomiendo que te leas el documento [JDK Installation for Microsoft Windows][21] . Todo lo que siempre quisiste saber sobre la variable **CLASSPATH** y nunca te atreviste a preguntar. :-)

Ahora, ya si que podremos ejecutar nuestra aplicación. Al fin, el resultado esperado...

<img src="https://github.com/manualweb/manualweb/raw/master/java/images/java-mi-primera-aplicacion.png" alt="Ejecutando Mi Primera Aplicación Java" class="img-responsive"/>


[1]: http://www.manualweb.net/tutorial-java/ "Manual Java"
[2]: https://www.linkedin.com/in/jamesgosling/
[3]: https://en.wikipedia.org/wiki/Sun_Microsystems
[4]: https://www.jcp.org/en/jsr/detail?id=59
[5]: http://www.manualweb.net/tutorial-xml/ "Manual XML"
[6]: http://www.manualweb.net/tutorial-xslt/ "Manual XSLT"
[7]: http://openjdk.java.net/
[8]: http://www.manualweb.net/tutorial-javascript/ "Manual Javascript"
[9]: http://blog.takipi.com/5-features-in-java-9-that-will-change-how-you-develop-software-and-2-that-wont/
[10]: http://www.oracle.com/technetwork/java/javase/tech/index.html
[11]: http://www.oracle.com/technetwork/java/javaee/tech/index.html
[12]: http://www.oracle.com/technetwork/java/embedded/javame/index.html
[13]: http://www.oracle.com/technetwork/java/embedded/javacard/documentation/index.html
[14]: https://java.com/en/download/ "Descargar Compilador Java"
[15]: http://www.vim.org/download.php#pc "Wim"
[16]: http://aignes.com/notebook.htm "AM-Notebook"
[17]: http://www.gena01.com/win32pad "Win32Pad"
[18]: http://www.editpadpro.com/editpadlite.html "EditPadLite"
[19]: http://www.flos-freeware.ch/notepad2.html "NotePad2"
[20]: http://www.manualweb.net/java/instalar-java/
[21]: https://docs.oracle.com/javase/8/docs/technotes/guides/install/windows_jdk_install.html#CHDEBCCJ "JDK Installation for Microsoft Windows"
[22]: http://www.w3api.com/wiki/Java:System.out
