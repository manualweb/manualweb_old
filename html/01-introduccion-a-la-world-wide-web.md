---
ID: 1351
post_title: 01 – Introducción a la World Wide Web
author: Víctor Cuervo
post_date: 2017-04-11 01:33:19
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/introduccion-a-la-world-wide-web/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
gitfolder: html
---
En la introducción a la World Wide Web hablamos de:
[TOC]

Hoy en día la tecnología de la red, va avanzando a pasos agigantados. ¿Por qué? La razón es que tanto las empresas como a nivel individual la sociedad se está dando cuenta de todas las posibilidades que la 'red de redes' nos ofrece.

Antes de adentrarnos en el [HTML][1] deberemos de tener una serie de conceptos básicos sobre lo que es Internet y el mundo que lo rodea.

### ¿Qué es Internet?

Internet es un conjunto de ordenadores o red de ordenadores interconectados entre mediante algún soporte, ya sea físico o inalámbrico. El lenguaje que utilizan los ordenadores para hablarse entre ellos se llama TCP/IP. Mediante el lenguaje TCP/IP las máquinas se intercambian la información.

### El Inicio: Comunicando máquinas

En 1969 nace un proyecto de índole militar en EEUU llamado ARPANET, este proyecto es el primero que permite conectar máquinas de diferentes universidades entre sí.

Poco a poco el proyecto fue cogiendo un matiz de investigación hasta separarse del propio proyecto militar, conectando más máquinas, y llegando a conceptualizar lo que es Internet Así hasta llegar a los día de hoy, donde las máquinas que están conectadas a la red son de empresas, universidades, personales,... dónde las máquinas ya no son solo ordenadores, sino que pueden ser móviles, elementos de domótica, coches,...

### La World Wide Web y el HTML

Un poco más tarde, sobre 1990, en el CERN, Tim Berners Lee y una serie de colaboradores definió un sistema de almacenamiento y recuperación de información. De tal manera que la información pudiese ser consultada de una forma estándar desde cualquier sitio. Estaba naciendo el lenguaje que define la información, nacía [HTML][1]. Era la gestación de la **World Wide Web**, información enlazada una con otra creando el tejido que es la red.

Actualmente el lenguaje [HTML][1] tiene [como especificación oficial HTML 5.0][2] *(28 de octubre de 2014)* y se está trabajando en [el borrador de HTML 5.1][3] *(última actualización [el 10 de marzo de 2016][4])*.

El lenguaje **HTML (HyperText Markup Language)** o lenguaje de etiquetas de hipertexto es un lenguaje que permite definir la estructura de una página web mediante un conjunto de elementos o etiquetas. La base de los documentos web o documentos [HTML][1] es que unos se van enlazando con otros creando una gran malla o red de documentos que es lo que conocemos como World Wide Web, “la red” o más comúnmente como “la web”.

### Los Navegadores Web y las URL

Solo faltaban los programas que nos permitieran visualizar dicha información. De esta forma en 1993 se creaba el **navegador web** Mosaic.

Herramienta imprescindible para poder visualizar el contenido HTML. Los navegadores web son las herramientas que nos permiten movernos por la red, visualizar y acceder a los contenidos de la misma.

Muy atrás han quedado los tiempos en los que solo existía el navegador web Mosaic y ahora en el mercado podemos encontrar una gran cantidad de navegadores web: [Chrome][5], [Firefox][6], [Opera][7], [Safari][8], [Internet Explorer][9],...

Para identificar cada uno de los contenidos que hay en la red se ha definido el concepto de **URL (o URI)**. Mediante una URL podemos acceder a cualquier contenido de la red utilizando un agente de usuario, más conocido como navegador web o browser.

Una URL se compone, a modo general, de diferentes partes:


* **Protocolo**, es el tipo de comunicación que queremos establecer con la máquina. Por ejemplo, si queremos visualizar un documento utilizaremos http, si queremos recuperar un fichero indicaremos ftp,...
* **Máquina**, será la máquina que tiene el contenido. Las máquinas se identifican mediante un código numérico llamado IP, pero como esos códigos con complejos de aprender las damos nombres. Así podemos conocer una máquina (o máquinas) como [google.com][10], [lineadecodigo.com][11], [manualweb.net][12],...
</li>
<li>
  <b>Contenido</b>, será el contenido al cual queremos acceder. Este puede ser el nombre de un fichero, el nombre de una página web, el nombre de un vídeo,... El contenido suele estar ubicado en un directorio, por lo cual dicho nombre suele venir antepuesto de la ruta de un directorio.
</li>

La estructura general de una URL será la siguiente:

<pre>protocolo://máquina/contenido</pre>

Si nos fijamos en los nombres de las máquinas, estos suelen tener dos partes: <li>
  <b>Nombre de la Máquina</b>, este suele ser el nombre del servicio al que intentamos acceder. Por ejemplo: google, manualweb, elpais,...
</li>
<li>
  <b>Dominio</b>, es la extensión que nos permite identificar el tipo o ubicación del servicio al que accedemos. Por ejemplo: .com, .net, .gov,... Aunque hay que tener cuidado ya que los dominios, en ciertos casos, no están reglados y pueden referirse a otra cosa distinta.
</li>

Algunos dominios que podemos encontrarnos son: <li>
  <b>.com,</b> para empresas o compañías. - <a href="http://www.google.com">http://www.google.com</a>
</li>
<li>
  <b>.org</b>, para organizaciones. - <a href="http://www.greenpeace.org">http://www.greenpeace.org</a>
</li>
<li>
  <b>.edu</b>, para recursos de educación y universidades. - <a href="http://www.mit.edu">http://www.mit.edu</a>
</li>
<li>
  <b>.mil</b>, para estamentos militares. - <a href="http://www.navy.mil">http://www.navy.mil</a>
</li>
<li>
  <b>.gov,</b> para elementos gubernamentales. - <a href="http://www.whitehouse.gov">http://www.whitehouse.gov</a>
</li>
<li>
  <b>.es, .fr, .co, .pe, .ar,... </b>son dominios de países (españa, francia, colombia, perú, argentina,...) - <a href="http://www.red.es">http://www.red.es</a>
</li>
<li>
  ….
</li>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3.org/TR/2014/REC-html5-20141028/
 [3]: https://www.w3.org/TR/2016/WD-html51-20160310/
 [4]: https://www.w3.org/blog/news/archives/5313
 [5]: http://www.ayudaenlaweb.com/navegadores/que-es-google-chrome/
 [6]: http://www.ayudaenlaweb.com/navegadores/que-es-firefox/
 [7]: http://www.ayudaenlaweb.com/navegadores/que-es-opera/
 [8]: http://www.ayudaenlaweb.com/navegadores/que-es-safari/
 [9]: http://www.ayudaenlaweb.com/navegadores/que-es-internet-explorer/
 [10]: http://www.google.com
 [11]: http://lineadecodigo.com
 [12]: http://www.manualweb.net
