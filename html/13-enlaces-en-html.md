---
ID: 1378
post_title: 13 – Enlaces en HTML
author: Víctor Cuervo
post_date: 2017-04-12 18:32:50
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/enlaces-en-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-enlaces/feed/
gitfolder: html
---
### ¿Qué son los enlaces en HTML?

Lo más importante de los documentos [HTML][1] son los enlaces. Ya que mediante los enlaces en HTML podemos comunicar una página con otra. De esta forma, enlazando documentos [HTML][1] podemos acabar tejiendo lo que es Internet.

Para crear un enlace en HTML utilizamos el [elemento A][2] con la siguiente sintaxis:

~~~html
<a>Contenido del enlace</a>
~~~

Pero solo con esto el enlace no tendrá mucha utilidad ya que el principal objetivo del enlace es enlazar a un destino. Para poder indicar el destino de un enlace utilizamos el [atributo href][3]. En valor del [atributo href][3] puede ser cualquier URI que represente un recurso. Es decir, una página, una parte de una página, una URL genérica, un archivo,... De esta forma el enlace en HTML lo crearemos con la sintaxis:

~~~html
<a href=”URI”>Contenido del enlace</a>
~~~

A modo de ejemplo podríamos tener los siguientes enlaces:

~~~html
<a href=”documento.html”>Enlace a un documento</a>
<a href=”documento.html#resumen”>Enlace a una parte de un documento</a>
<a href=”http://www.manualweb.net”>Enlace a una web</a>
<a href=”http://www.manualweb.net/tutorial-html/”>Enlace a un directorio</a>
<a href=”miimagen.png”>Enlace a una imagen</a>
<a href=”mimusica.mp3”>Enlace a un archivo de sonido</a>
~~~

### Destino del enlace

Pero, ¿dónde se abre el enlace? Pues por defecto y si no hemos configurado nada en el navegador web que estemos utilizando el enlace se abre en la misma ventana en la que tengamos el enlace.

Si bien, en el enlace, podemos indicar el destino que queremos darle a dicho enlace. Eso lo podemos hacer mediante el [atributo target][4]. Los posibles valores que admite el [atributo target][4] son:

* **_blank**, el agente de usuario intentará abrir el enlace en una nueva ventana. La nueva ventana no tendrá nombre.
* **_self**, el agente de usuario intentará abrir el enlace en el mismo marco donde está en código actual.
* **_parent**, el agente de usuario intentará abrir el enlace en el [frameset][11] inmediatamente superior al que se encuentra la página. Esto suele suceder cuando tenemos el enlace en un área de frames.
* **_top**, el agente de usuario intentará abrir el enlace en la ventana padre. En el caso de que exista un [frameset][11] lo eliminará y se hará con toda la ventana.
* **nombre_marco**, se podrá indicar el nombre de un frame. En este caso el agente de usuario intentará abrir el enlace en el [frame][12] que coincida con el nombre. En el caso de no existir un [frame][12] con ese nombre lo abrirá en una nueva ventana, asignándole dicho nombre.

Así podremos tener el siguiente código:

~~~html
<a href=”enlace.html” target=”_blank”>Abrir enlace en una nueva ventana</a>
<a href=”enlace.html” target=”_top”>Abrir enlace en la ventana superior</a>
~~~

### Título de los enlaces

El enlace en HTML, tal y como lo hemos visto hasta ahora, sirve para enlazar contra un recurso de la web: servidor, directorio, dominio,... Y lo que en mayor o menor medida describe lo que enlazamos es el contenido que encontramos entre las [etiquetas A][2].

Si bien el [elemento A][2] nos ofrece un [atributo llamado title][5]. En el [atributo title][5] podemos describir de una forma textual el destino del enlace. Esto servirá no solo al usuario para que pueda obtener más información de dónde va, si no a las máquinas a la hora de asignar un nombre a la URI sobre la que estamos enlazando.

Un ejemplo sería:

~~~html
<a href=”http://www.manual.net” title=”Web de Manuales y Tutoriales de Programación”>Ir a Manual Web</a>
~~~

### Enlaces en HTML a una parte del documento

Hasta el momento lo que hemos visto es como montar enlaces en HTML a documentos. Ya sea porque enlazamos directamente al documento o bien porque enlazamos a un servidor o directorio que nos dará un documento.

Pero otra capacidad que tenemos en [HTML][1] es la de enlazar a una parte concreta del documento. Imagina que en un documento tenemos un título y varios capítulos. Y lo que queremos hacer desde otro documento [HTML][1] o bien desde el mismo documento es enlazar directamente al inicio de un capítulo.

#### Marcando una parte del documento

Para poder enlazar a una parte concreta de un documento lo primero que tenemos que hacer es marcar esa parte del documento. Para ello contamos con el [atributo name][6]. Si creamos un enlace con el [atributo name][6], este enlace se definirá como posición y no como enlace de navegación.

La sintaxis será:

~~~html
<a name="partedocumento">Contenido</a>
~~~

En este caso el contenido puede ser vacío ya que no se ofrecerá nada para navegar. Es por ello que podemos ponerlo antes de nuestro capítulo.

~~~html
<p>Parrafo</p>
<a name=”cap2”></a><h2>Nuevo Capítulo</2>
~~~

Es muy importante el contenido que le demos al [atributo name][6], ya que dicho contenido vamos a utilizarlo para acceder desde un enlace.

#### Enlazando a una parte del documento

Una vez que hemos creado el marcaje del enlace en HTML en un documento es hora de acceder a esa parte del documento. Para ello solo tenemos que poner el nombre que le hayamos dado al [atributo name][6] precedido de una almohadilla.

La sintaxis será:

~~~html
<a href="#name">Enlace a parte del documento</a>
~~~

Es decir, en el caso de que la parte marcada en el documento la hayamos marcado con “cap2” el enlace que tenemos que conformar será:

~~~html
<a href="#cap2">Enlace al capítulo 2</a>
~~~

La parte del documento al que accedemos no tiene porqué estar en el mismo documento del enlace, puede estar en otro documento o servidor. De esta forma podemos tener enlaces a partes de otros documentos de la siguiente forma:

~~~html
<a href="documento2.html#cap2">Enlace al capítulo 2 del documento2</a>
<a href="http://servidor.com/#cap2">Enlace al capítulo 2 del servidor</a>
~~~

El **utilizar la almohadilla** como valor del [href][3] nos puede servir para acceder a la parte superior del documento. Es por ello que esto es utilizado como enlace en las partes inferiores de los documentos [HTML][1] para subir a la parte de arriba.

~~~html
<a href="#">Ir Arriba</a>
~~~

### Enlaces en HTML con imágenes

En lo que va de capítulo sólo hemos visto enlaces en HTML cuyo contenido era texto. Si bien como contenido de los enlaces podemos poner imágenes.

~~~html
<a href="http://www.victorcuervo.com"><img src=”victor.jpg” alt=”Foto de Victor”/></a>
~~~

De esta forma toda la imagen será un elemento enlazable que nos llevará, en el caso de pinchar sobre ella, al destino indicado en el [atributo href][3].

Esta técnica se suele utilizar para presentar una imágen de baja resolución y tamaño, que al pulsarla nos cargue una imagen con mayor resolución y tamaño. Un código que podría ser de la siguiente forma:

~~~html
<a href="foto.png"><img src="thumbnail_foto.png" alt="Mi foto"/></a>
~~~

### Enlaces en HTML para descargar fichero

Otro de los usos que se les da a los enlaces en HTML es el de habilitar la descarga de ficheros. En este caso el destino indicado por el [atributo href][3] debe de ser el fichero que queremos descargar. En estos casos es bueno que el fichero a descargar este comprimido.

El código quedaría de la siguiente forma:

~~~html
<a href="fichero.zip">Descargar el fichero</a>
~~~

Es importante que sepas que el navegador siempre va a intentar abrir el fichero enlazado en el [atributo href][3] para poder mostrarlo visualmente. En el caso de que no encuentre ningún programa para abrirlo nos mostrará un menú emergente en el que nos dará la posibilidad de guardar el fichero.

### Protocolos en la URL del enlace

Hasta ahora hemos visto que todos los enlaces en HTML se apoyan en el protocolo http, pero el enlace especificado en el [atributo href][3] no tiene porqué ser http, si no que podría ser otro protocolo como ftp, mailto,...

~~~html
<a href="ftp://servidorftp.com">Servidor FTP</a>
~~~

Lo bueno de utilizar el protocolo mailto dentro de los enlaces en HTML es que el navegador web nos va a abrir directamente el programa de correo electrónico que tengamos predeterminado en el ordenador.

La estructura del protocolo mailto en un enlace a sería la siguiente:

~~~html
<a href="mailto:usuario@dominio.com">Email para usuario@dominio.com</a>
~~~

Lo bueno es que además podemos ponerle parámetros al modelo de mailto y se autorellenarán campos como el tema del email, campos CC, BCC,...

~~~html
<a href="mailto:usuario@dominio.com?subject='Tema del Mensaje'">Email para usuario@dominio.com</a>
~~~

### Relaciones entre documentos: el elemento link

Hasta ahora hemos visto enlaces explícitos entre diferentes recursos. Si bien el lenguaje [HTML][1] nos da la posibilidad de establecer relaciones entre documentos sin tener que explicitar directamente un enlace. Para ello [HTML][1] nos ofrece el [elemento link][7].

La estructura del [elemento link][7] es:

~~~html
<link href="destino" rel="relacion" rev="relacion-inversa"/>
~~~

Es importante saber que el elemento link solo aparece dentro de la [cabecera o head][8] del documento.

El [atributo rel][9] establece la relación que hay con el documento destino, mientras que el atributo rev define la relación del documento destino con el documento actual. Es decir, la relación inversa.

Por otro lado el [atributo href][3] es el que contiene la URI del documento destino.

Uno de los usos del [elemento link][7] es para establecer las relaciones de documentos que formen una publicación completa. De esta forma manejando los valores del atributo rel podemos establecer dónde está el índice, cuál es artículo anterior y cual es el próximo artículo.

~~~html
<link rel=”index” href=”indice.html”>
<link rel=”prev” href=”c2.html”>
<link rel=”next” href=”c4.html”>
~~~

Aunque los enlaces de tipo [link][7] no son renderizados por el navegador pueden ser interpretados para añadir la información al navegador.

### Tipos de relaciones entre documentos

Según el lenguaje [HTML][1] se definen los siguientes tipos de relaciones entre documentos. Estos valore pueden ser utilizados por los atributos [rel][9] y rev.

*  **alternate,** indica una versión alternativa del documento.
*  **stylesheet,** hace referencia a una hoja de estilo externa para el documento.
*  **start**, primer documento de un conjunto de documento.
*  **next**, siguiente documento al actual.
*  **prev**, documento anterior al actual.
*  **contents**, documento que contiene la tabla de contenidos.
*  **index**, documento que contiene el índice.
*  **glossary**, documento que contiene el glosario.
*  **copyright**, información del copyright del documento actual.
*  **chapter,** documento que actúa como capítulo en una colección de documentos.
*  **section,** documento que actúa como sección en un conjunto de documentos.
*  **subsection,** documento que actúa como subsección en un conjunto de documentos.
*  **appendix**, documento que actúa como apéndice de una colección de documentos.
*  **help,** documento de ayuda.
*  **bookmark,** para marcar un punto concreto del documento.

### Enlaces en HTLM para hojas de estilo

En [elemento link][7] nos servirá para cargar las hojas de estilo del documento [HTML][1]. Ya veremos más adelante qué son, pero digamos que nos sirven para darle estilo gráfico a la página.

Las hojas de estilos se almacenan en ficheros .css. Así que podemos utilizar el [elemento link][7] para enlazarlas indicando que **su tipo es “text/css”**, mediante el [atributo type][10].

~~~html
<link href=”style.css” rel=”style” type=”text/css”/>
~~~

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:A
 [3]: http://www.w3api.com/wiki/HTML:Href
 [4]: http://www.w3api.com/wiki/HTML:Target
 [5]: http://www.w3api.com/wiki/HTML:Title
 [6]: http://www.w3api.com/wiki/HTML:Name
 [7]: http://www.w3api.com/wiki/HTML:LINK
 [8]: http://www.w3api.com/wiki/HTML:HEAD
 [9]: http://www.w3api.com/wiki/HTML:LINK.rel
 [10]: http://www.w3api.com/wiki/HTML:Type
[11]: http://w3api.com/wiki/HTML:FRAMESET
[12]: http://w3api.com/wiki/HTML:FRAME
