---
ID: pdte
post_title: '13 &#8211; Enlaces en HTML'
author: Víctor Cuervo
post_date: 2017-04-12 01:05
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/enlaces-html/
published: false
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

<span style="font-weight: 400;">Lo más importante de los documentos </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> son los enlaces. Ya que mediante los enlaces en HTML podemos comunicar una página con otra. De esta forma, enlazando documentos </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> podemos acabar tejiendo lo que es Internet.</span> <span style="font-weight: 400;">Para crear un enlace en HTML utilizamos el </span>[<span style="font-weight: 400;">elemento A</span>][2]<span style="font-weight: 400;"> con la siguiente sintaxis:</span> <a>Contenido del enlace</a> <span style="font-weight: 400;">Pero solo con esto el enlace no tendrá mucha utilidad ya que el principal objetivo del enlace es enlazar a un destino. Para poder indicar el destino de un enlace utilizamos el </span>[<span style="font-weight: 400;">atributo href</span>][3]**.**<span style="font-weight: 400;"> En valor del </span>[<span style="font-weight: 400;">atributo href</span>][3]<span style="font-weight: 400;"> puede ser cualquier URI que represente un recurso. Es decir, una página, una parte de una página, una URL genérica, un archivo,...</span> <span style="font-weight: 400;">De esta forma el enlace en HTML lo crearemos con la sintaxis:</span> <pre lang="html4strict"><a href="”URI”">Contenido del enlace</a></pre>

<span style="font-weight: 400;">A modo de ejemplo podríamos tener los siguientes enlaces:</span> <pre lang="html4strict"><a href="”documento.html”">Enlace a un documento</a>
<a href="”documento.html#resumen”">Enlace a una parte de un documento</a>
<a href="”http://www.manualweb.net”">Enlace a una web</a>
<a href="”http://www.manualweb.net/tutorial-html/”">Enlace a un directorio</a>
<a href="”miimagen.png”">Enlace a una imagen</a>
<a href="”mimusica.mp3”">Enlace a un archivo de sonido</a></pre>

### Destino del enlace

<span style="font-weight: 400;">Pero, ¿dónde se abre el enlace? Pues por defecto y si no hemos configurado nada en el navegador web que estemos utilizando el enlace se abre en la misma ventana en la que tengamos el enlace.</span> <span style="font-weight: 400;">Si bien, en el enlace, podemos indicar el destino que queremos darle a dicho enlace. Eso lo podemos hacer mediante el </span>[<span style="font-weight: 400;">atributo target</span>][4]**.**<span style="font-weight: 400;"> Los posibles valores que admite el </span>[<span style="font-weight: 400;">atributo target</span>][4]<span style="font-weight: 400;"> son:</span>
<li style="font-weight: 400;">
  <b>_blank</b><span style="font-weight: 400;">, el agente de usuario intentará abrir el enlace en una nueva ventana. La nueva ventana no tendrá nombre.</span>
</li>
<li style="font-weight: 400;">
  <b>_self</b><span style="font-weight: 400;">, el agente de usuario intentará abrir el enlace en el mismo marco donde está en código actual.</span>
</li>
<li style="font-weight: 400;">
  <b>_parent</b><span style="font-weight: 400;">, el agente de usuario intentará abrir el enlace en el </span><a href="http://w3api.com/wiki/HTML:FRAMESET"><span style="font-weight: 400;">frameset</span></a><span style="font-weight: 400;"> inmediatamente superior al que se encuentra la página. Esto suele suceder cuando tenemos el enlace en un área de frames.</span>
</li>
<li style="font-weight: 400;">
  <b>_top</b><span style="font-weight: 400;">, el agente de usuario intentará abrir el enlace en la ventana padre. En el caso de que exista un </span><a href="http://w3api.com/wiki/HTML:FRAMESET"><span style="font-weight: 400;">frameset</span></a><span style="font-weight: 400;"> lo eliminará y se hará con toda la ventana.</span>
</li>
<li style="font-weight: 400;">
  <b>nombre_marco</b><span style="font-weight: 400;">, se podrá indicar el nombre de un frame. En este caso el agente de usuario intentará abrir el enlace en el </span><a href="http://w3api.com/wiki/HTML:FRAME"><span style="font-weight: 400;">FRAME</span></a><span style="font-weight: 400;"> que coincida con el nombre. En el caso de no existir un </span><a href="http://w3api.com/wiki/HTML:FRAME"><span style="font-weight: 400;">FRAME</span></a><span style="font-weight: 400;"> con ese nombre lo abrirá en una nueva ventana, asignándole dicho nombre.</span>
</li>

<span style="font-weight: 400;">Así podremos tener el siguiente código:</span> <pre lang="html4strict"><a href="”enlace.html”" target="”_blank”">Abrir enlace en una nueva ventana</a>
<a href="”enlace.html”" target="”_top”">Abrir enlace en la ventana superior</a></pre>

### Título de los enlaces

<span style="font-weight: 400;">El enlace en HTML, tal y como lo hemos visto hasta ahora, sirve para enlazar contra un recurso de la web: servidor, directorio, dominio,... Y lo que en mayor o menor medida describe lo que enlazamos es el contenido que encontramos entre las etiquetas A.</span> <span style="font-weight: 400;">Si bien el elemento A nos ofrece un </span>[<span style="font-weight: 400;">atributo llamado title</span>][5]<span style="font-weight: 400;">. En el </span>[<span style="font-weight: 400;">atributo title</span>][5]<span style="font-weight: 400;"> podemos describir de una forma textual el destino del enlace. Esto servirá no solo al usuario para que pueda obtener más información de dónde va, si no a las máquinas a la hora de asignar un nombre a la URI sobre la que estamos enlazando.</span> <span style="font-weight: 400;">Un ejemplo sería:</span> <pre lang="html4strict"><a title="”Web" href="”http://www.manual.net”">Ir a Manual Web</a></pre>

### Enlaces en HTML a una parte del documento

<span style="font-weight: 400;">Hasta el momento lo que hemos visto es como montar enlaces en HTML a documentos. Ya sea porque enlazamos directamente al documento o bien porque enlazamos a un servidor o directorio que nos dará un documento.</span> <span style="font-weight: 400;">Pero otra capacidad que tenemos en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> es la de enlazar a una parte concreta del documento. Imagina que en un documento tenemos un título y varios capítulos. Y lo que queremos hacer desde otro documento </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> o bien desde el mismo documento es enlazar directamente al inicio de un capítulo.</span>
#### Marcando una parte del documento

<span style="font-weight: 400;">Para poder enlazar a una parte concreta de un documento lo primero que tenemos que hacer es marcar esa parte del documento. Para ello contamos con el </span>[<span style="font-weight: 400;">atributo name</span>][6]<span style="font-weight: 400;">. Si creamos un enlace con el </span>[<span style="font-weight: 400;">atributo name</span>][6]<span style="font-weight: 400;">, este enlace se definirá como posición y no como enlace de navegación.</span> <span style="font-weight: 400;">La sintaxis será:</span> <pre lang="html4strict"><a name="”partedocumento”"></a>Contenido</pre>

<span style="font-weight: 400;">En este caso el contenido puede ser vacío ya que no se ofrecerá nada para navegar. Es por ello que podemos ponerlo antes de nuestro capítulo.</span> Parrafo <a name="”cap2”"></a>
## Nuevo Capítulo

<span style="font-weight: 400;">Es muy importante el contenido que le demos al </span>[<span style="font-weight: 400;">atributo name</span>][6]<span style="font-weight: 400;">, ya que dicho contenido vamos a utilizarlo para acceder desde un enlace.</span>
#### Enlazando a una parte del documento

<span style="font-weight: 400;">Una vez que hemos creado el marcaje del enlace en HTML en un documento es hora de acceder a esa parte del documento. Para ello solo tenemos que poner el nombre que le hayamos dado al </span>[<span style="font-weight: 400;">atributo name</span>][6]<span style="font-weight: 400;"> precedido de una almohadilla.</span> <span style="font-weight: 400;">La sintaxis será:</span> <pre lang="html4strict"><a href="”#name”">Enlace a parte del documento</a></pre>

<span style="font-weight: 400;">Es decir, en el caso de que la parte marcada en el documento la hayamos marcado con “cap2” el enlace que tenemos que conformar será:</span> <pre lang="html4strict"><a href="”#cap2”">Enlace al capítulo 2</a></pre>

<span style="font-weight: 400;">La parte del documento al que accedemos no tiene porqué estar en el mismo documento del enlace, puede estar en otro documento o servidor. De esta forma podemos tener enlaces a partes de otros documentos de la siguiente forma:</span> <pre lang="html4strict"><a href="”documento2.html#cap2”">Enlace al capítulo 2 del documento2</a>
<a href="”http://servidor.com/#cap2”">Enlace al capítulo 2 del servidor</a></pre>

<span style="font-weight: 400;">El </span>**utilizar la almohadilla**<span style="font-weight: 400;"> como valor del </span>[<span style="font-weight: 400;">href</span>][3]<span style="font-weight: 400;"> nos puede servir para acceder a la parte superior del documento. Es por ello que esto es utilizado como enlace en las partes inferiores de los documentos </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> para subir a la parte de arriba.</span> <pre lang="html4strict"><a href="”#”">Ir Arriba</a></pre>

### Enlaces en HTML con imágenes

<span style="font-weight: 400;">En lo que va de capítulo sólo hemos visto enlaces en HTML cuyo contenido era texto. Si bien como contenido de los enlaces podemos poner imágenes.</span> <pre lang="html4strict"><a href="”http://www.victorcuervo.com”"><img src="”victor.jpg”" alt="”Foto" /></a></pre>

<span style="font-weight: 400;">De esta forma toda la imagen será un elemento enlazable que nos llevará, en el caso de pinchar sobre ella, al destino indicado en el </span>[<span style="font-weight: 400;">atributo href</span>][3]<span style="font-weight: 400;">.</span> <span style="font-weight: 400;">Esta técnica se suele utilizar para presentar una imágen de baja resolución y tamaño, que al pulsarla nos cargue una imagen con mayor resolución y tamaño. Un código que podría ser de la siguiente forma:</span> <pre lang="html4strict"><a href="”foto.png”"><img src="”thumbnail_foto.png”" alt="”Mi" /></a></pre>

### Enlaces en HTML para descargar fichero

<span style="font-weight: 400;">Otro de los usos que se les da a los enlaces en HTML es el de habilitar la descarga de ficheros. En este caso el destino indicado por el </span>[<span style="font-weight: 400;">atributo href</span>][3]<span style="font-weight: 400;"> debe de ser el fichero que queremos descargar. En estos casos es bueno que el fichero a descargar este comprimido.</span> <span style="font-weight: 400;">El código quedaría de la siguiente forma:</span> <pre lang="html4strict"><a href="”fichero.zip”">Descargar el fichero</a></pre>

<span style="font-weight: 400;">Es importante que sepas que el navegador siempre va a intentar abrir el fichero enlazado en el </span>[<span style="font-weight: 400;">atributo href</span>][3]<span style="font-weight: 400;"> para poder mostrarlo visualmente. En el caso de que no encuentre ningún programa para abrirlo nos mostrará un menú emergente en el que nos dará la posibilidad de guardar el fichero.</span>
### Protocolos en la URL del enlace

<span style="font-weight: 400;">Hasta ahora hemos visto que todos los enlaces en HTML se apoyan en el protocolo http, pero el enlace especificado en el </span>[<span style="font-weight: 400;">atributo href</span>][3]<span style="font-weight: 400;"> no tiene porqué ser http, si no que podría ser otro protocolo como ftp, mailto,...</span> <pre lang="html4strict"><a href="”ftp://servidorftp.com”">Servidor FTP</a></pre>

<span style="font-weight: 400;">Lo bueno de utilizar el protocolo mailto dentro de los enlaces en HTML es que el navegador web nos va a abrir directamente el programa de correo electrónico que tengamos predeterminado en el ordenador.</span> <span style="font-weight: 400;">La estructura del protocolo mailto en un enlace a sería la siguiente:</span> <pre lang="html4strict"><a href="”mailto:usuario@dominio.com”">Email para usuario@dominio.com</a></pre>

<span style="font-weight: 400;">Lo bueno es que además podemos ponerle parámetros al modelo de mailto y se autorellenarán campos como el tema del email, campos CC, BCC,...</span> <pre lang="html4strict"><a href="”mailto:usuario@dominio.com?subject=’Tema">Email para usuario@dominio.com</a></pre>

### Relaciones entre documentos: el elemento link

<span style="font-weight: 400;">Hasta ahora hemos visto enlaces explícitos entre diferentes recursos. Si bien el lenguaje </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> nos da la posibilidad de establecer relaciones entre documentos sin tener que explicitar directamente un enlace. Para ello </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> nos ofrece el </span>[<span style="font-weight: 400;">elemento link</span>][7]<span style="font-weight: 400;">.</span> <span style="font-weight: 400;">La estructura del </span>[<span style="font-weight: 400;">elemento link</span>][7]<span style="font-weight: 400;"> es:</span> <pre lang="html4strict"></pre>

<span style="font-weight: 400;">Es importante saber que el elemento link solo aparece dentro de la </span>[<span style="font-weight: 400;">cabecera o head</span>][8]<span style="font-weight: 400;"> del documento.</span> <span style="font-weight: 400;">El </span>[<span style="font-weight: 400;">atributo rel</span>][9]<span style="font-weight: 400;"> establece la relación que hay con el documento destino, mientras que el atributo rev define la relación del documento destino con el documento actual. Es decir, la relación inversa.</span> <span style="font-weight: 400;">Por otro lado el </span>[<span style="font-weight: 400;">atributo href</span>][3]<span style="font-weight: 400;"> es el que contiene la URI del documento destino.</span> <span style="font-weight: 400;">Uno de los usos del </span>[<span style="font-weight: 400;">elemento link</span>][7]<span style="font-weight: 400;"> es para establecer las relaciones de documentos que formen una publicación completa. De esta forma manejando los valores del atributo rel podemos establecer dónde está el índice, cuál es artículo anterior y cual es el próximo artículo.</span> <pre lang="html4strict"></pre>

<span style="font-weight: 400;">Aunque los enlaces de tipo </span>[<span style="font-weight: 400;">link</span>][7]<span style="font-weight: 400;"> no son renderizados por el navegador pueden ser interpretados para añadir la información al navegador.</span>
### Tipos de relaciones entre documentos

<span style="font-weight: 400;">Según el lenguaje </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> se definen los siguientes tipos de relaciones entre documentos. Estos valore pueden ser utilizados por los atributos </span>[<span style="font-weight: 400;">rel</span>][9]<span style="font-weight: 400;"> y rev.</span>
<li style="font-weight: 400;">
  <b>alternate,</b><span style="font-weight: 400;"> indica una versión alternativa del documento.</span>
</li>
<li style="font-weight: 400;">
  <b>stylesheet,</b><span style="font-weight: 400;"> hace referencia a una hoja de estilo externa para el documento.</span>
</li>
<li style="font-weight: 400;">
  <b>start</b><span style="font-weight: 400;">, primer documento de un conjunto de documento.</span>
</li>
<li style="font-weight: 400;">
  <b>next</b><span style="font-weight: 400;">, siguiente documento al actual.</span>
</li>
<li style="font-weight: 400;">
  <b>prev</b><span style="font-weight: 400;">, documento anterior al actual.</span>
</li>
<li style="font-weight: 400;">
  <b>contents</b><span style="font-weight: 400;">, documento que contiene la tabla de contenidos.</span>
</li>
<li style="font-weight: 400;">
  <b>index</b><span style="font-weight: 400;">, documento que contiene el índice.</span>
</li>
<li style="font-weight: 400;">
  <b>glossary</b><span style="font-weight: 400;">, documento que contiene el glosario.</span>
</li>
<li style="font-weight: 400;">
  <b>copyright</b><span style="font-weight: 400;">, información del copyright del documento actual.</span>
</li>
<li style="font-weight: 400;">
  <b>chapter,</b><span style="font-weight: 400;"> documento que actúa como capítulo en una colección de documentos.</span>
</li>
<li style="font-weight: 400;">
  <b>section,</b><span style="font-weight: 400;"> documento que actúa como sección en un conjunto de documentos.</span>
</li>
<li style="font-weight: 400;">
  <b>subsection,</b><span style="font-weight: 400;"> documento que actúa como subsección en un conjunto de documentos.</span>
</li>
<li style="font-weight: 400;">
  <b>appendix</b><span style="font-weight: 400;">, documento que actúa como apéndice de una colección de documentos.</span>
</li>
<li style="font-weight: 400;">
  <b>help,</b><span style="font-weight: 400;"> documento de ayuda.</span>
</li>
<li style="font-weight: 400;">
  <b>bookmark, </b><span style="font-weight: 400;">para marcar un punto concreto del documento. </span>
</li>

### Enlaces en HTLM para hojas de estilo

<span style="font-weight: 400;">En </span>[<span style="font-weight: 400;">elemento link</span>][7]<span style="font-weight: 400;"> nos servirá para cargar las hojas de estilo del documento </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;">. Ya veremos más adelante qué son, pero digamos que nos sirven para darle estilo gráfico a la página.</span> <span style="font-weight: 400;">Las hojas de estilos se almacenan en ficheros .css. Así que podemos utilizar el </span>[<span style="font-weight: 400;">elemento link</span>][7]<span style="font-weight: 400;"> para enlazarlas indicando que </span>**su tipo es “text/css”**<span style="font-weight: 400;">, mediante el </span>[<span style="font-weight: 400;">atributo type</span>][10]<span style="font-weight: 400;">.</span> <pre lang="html4strict"></pre>

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
