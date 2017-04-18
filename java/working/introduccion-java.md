

## Introducción al lenguaje Java


Java es un lenguaje de programación de propósito general, orientado a objetos,...


Desarrollado en sus inicios por James Gosling en 1991, e incialmente llamado **Oak** y **Green**.

Publicada su primera versión por Sun Microsystems en 1995.

Noviembre 2006 Sun lo convierte en Open Source mediante una licencia GNU General Public License (GPL)




Java nacía como un lenguaje de programación que pudiese ser multiplataforma y multidispositivo, bajo el paradigma *"Write Once Run Anywhere" (WORA)*

De esta forma un programa Java escrito una vez podemos ejecutarle sobre diferentes plataformas, siendo soportados los sistemas operativos Windows, MacOs y UNIX. Y a su vez en diferentes tipos de dispositivos.

Para poder seguir este paradigma la compilación de un programa [Java][1] no genera código fuente, si no que genera **bytecodes**. Estos **bytecodes** son interpretados por una máquina virtual o JVM (Java Virtual Machine). Dicha máquina ya está escrita para cada uno de los sistemas operativos en cuestión.

### Historia de Java


La última versión de Java distribuida (a día de hoy, *abril 2017*) es Java 8.


### Características del lenguaje Java
Dentro de las características del lenguaje [Java][1] encontramos:

#### Independiente de Plataforma
Cuando compilamos código fuente Java no se genera código máquina específico, si no que se generan **bytecodes**, los cuales son interpretados por la Java Virtual Machine (JVM), posibilitando que un mismo código fuente pueda ser ejecutado en múltiples plataformas.

#### Fuertemente Tipado??


#### Orientado a Objetos
Cualquier elemento del lenguaje [Java][1] es un objeto. Dentro de los objetos se encapsulan los datos, los cuales son accedidos mediante métodos.

### Sencillo
Java está enfocado para ser un lenguaje fácil de aprender. Simplemente se deberán de entender los conceptos básicos de la programación orientada a objetos (POO).

#### Seguro


#### Arquitectura Neutral
El formato de los ficheros generados por el compilador [Java][1] tienen un formato neutro, por lo cual permite que sean ejecutados por diferentes procesadores.

#### Portable
Java no tiene nada que dependa de la plataforma, lo cual le hace que sea portable a diferentes plataformas.

#### Robusto
El lenguaje [Java][1] intenta controlar las situaciones de error en los procesos de compilación y de ejecución, reduciendo de esta manera el riesgo de fallo.

#### Multi-hilo
Java nos permite la programación concurrente, de tal manera que un único programa puede abrir diferentes hilos de ejecución.

#### Interpretado
Los **bytecodes** son interpretados en tiempo real a código máquina.

#### Alto Rendimiento
[Java][1] ofrece compiladores Just-In-Time que permiten tener un alto rendimiento.

#### Distribuido
El lenguaje [Java][1] está pensando para ser ejecutado en arquitecturas distribuidas, como pueda ser Internet.

#### Dinámico
??



### Tecnologías de desarrollo Java

Dentro de Java existen diferentes tecnologías de desarrollo, cada una enfocada a un fin diferente, ya sea la base del lenguaje [Java][1], [Java][1] para el ámbito empresarial, [Java][1] para el desarrollo de aplicaciones móviles,...

Cada una de las tecnologías de desarrollo del lenguaje [Java][1] contiene:

>>¿Correcto?

1. Máquina virtual Java (JVM)
2. API de desarrollo de la plataforma

Las tecnologías que existen en la **plataforma [Java][1]** son:

* Java SE
* Java EE
* Java ME
* JavaFX
* Java Card
* Java Embedded
* Java TV
* Java DB


¿Otras tecnologías que se ofrecen en el marco [Java][1] son:?

* Java 3D
* Java Advanced Imaging (JAI)
* JavaBeans Activation Framework
* Java Communications
* JavaMail
* Java Media Framework (JMF)
* Java Speech
* Real-Time Specification for Java (RTSJ)


### Java SE

Librerias Base

* Java Lang/Java Util - proporcionan la funcionalidad básica para cualquier aplicación Java.
* Collections, es un framework que representa una forma unificada las estructuras de datos (listas, colas, pilas,...). Además incorpora una serie de métodos para la manipulación de estas estructuras de datos.
* Concurrencia, paquete que proporciona un framework con utilidades para la gestión de hilos. En el framework se incluyen pool de hilos, colas de bloqueo,...
* JAR (Java Archive), permite la gestión de archivos JAR.JAR es un fichero independiente de la plataforma que nos permite empaquetar diferentes ficheros (clases, imágenes,...).
* Logging librería que nos permite generar un reporte de información para usuarios fianles de nuestros programas Java.
* Gestión y Monitorización, librerías para la gestión y monitorización de la plataforma Java. Incluye las extensiones de monitorización JMX.
* Preferences API, permite configurar datos de configuraciones y preferencias de las aplicaciones Java. Estas configuraciones son de dos tipos: del sistema y de los usuarios.
* Ref Objects,
* Reflection, librería que nos proporciona los mecanismos necesarios para hacer introspección de las clases y así descubrir los campos, métodos y constructores que estás contienen.
* Expresiones Regulares, librería que nos permite hacer matching entre cadenas de caracteres y patrones especificados mediante expresiones regulares.
* Versionado, permite el control de versionado de los paquetes Java.
* ZIP, librerías para la lectura y escritura de formatos ZIP y GZIP.
* Instrumentation, API Java que nos permite crear agentes de cara a poder monitorizar las aplicaciones y recopilar información de rendimiento.

Otras librerías base
* Beans,

Librerías de Integración
* IDL,
* JDBC,
* JNDI,

Toolkits de Interface de Usuario
* AWT
* Swing
* Java 2D









[1]: http://www.manualweb.net/tutorial-java/ "Manual Java"
