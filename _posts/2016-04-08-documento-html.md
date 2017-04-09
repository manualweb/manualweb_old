---
ID: 746
post_title: '06 &#8211; El documento HTML'
author: Víctor Cuervo
post_date: 2016-04-08 12:00:48
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/documento-html/
published: true
nombreforo:
  - HTML
urlforo:
  - http://dudasprogramacion.com/html
urlmanual:
  - http://www.manualweb.net/tutorial-html/
urltest:
  - http://www.testprogramacion.com/html
urlcurso:
  - >
    http://www.aulaprogramacion.com/curso-html/
urlcharla:
  - >
    https://www.facebook.com/groups/html5.es/
urlvideo:
  - PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos:
  - >
    http://lineadecodigo.com/tag/html-basicos/feed/
---
En **el documento HTML** hablamos de: [TOC] <span style="font-weight: 400">El documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> tiene dos partes bien diferenciadas. La primera será </span>**la cabecera**<span style="font-weight: 400"> del documento en la que irá información relativa a la semántica del documento, metadatos, o a los recursos que necesita para su correcta visualización.</span> <span style="font-weight: 400">Por otro lado tenemos el cuerpo. </span>**El cuerpo**<span style="font-weight: 400"> contendrá la estructura del documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">. Dentro del cuerpo iremos situando los diferentes elementos del lenguaje </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> para la correcta visualización de la página.</span> <span style="font-weight: 400">Pero el documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> se caracteriza por empezar y terminar por el </span>[**elemento html**][2]<span style="font-weight: 400">. Es decir, al principio y al final del documento encontraremos el elemento de inicio y cierre respectivamente.</span> 
<pre><!-- Documento HTML -->
</pre>

<span style="font-weight: 400">Importante es saber que antes del primer </span>[<span style="font-weight: 400">elemento html</span>][2]<span style="font-weight: 400"> vamos a encontrar la definición del tipo de documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> sobre el que trabajemos. Como vimos en el capítulo tipos de documentos </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> podemos tener diferentes tipos o doctypes.</span> <span style="font-weight: 400">De esta forma la estructura básica del documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> será la siguiente:</span> 
<pre><!-- Documento HTML -->
</pre>

### **La cabecera del documento**

<span style="font-weight: 400">Lo primero que encontraremos dentro del documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> será la cabecera. La cabecera se delimita mediante </span>[**el elemento head**][3]<span style="font-weight: 400">.</span> 
<pre><!-- Elementos de cabecera -->
</pre>

<span style="font-weight: 400">Dentro de la cabecera vamos a encontrar elementos que nos definen la semántica del documento, estos serán las metatags o metadatos. Además podremos encontrar scripts, hojas de estilo y el más importante, el título de la página.</span> <span style="font-weight: 400">Es importante remarcar que el contenido que se encuentre dentro de la cabecera no tiene una representación visual directa.</span> 
#### **Título del documento**

<span style="font-weight: 400">El título del documento se definirá utilizando </span>[**el elemento title**][4]<span style="font-weight: 400">. Cómo contenido del elemento encontraremos el texto que represente dicho título.</span> <span style="font-weight: 400">La estructura sería la siguiente:</span> 
<pre><title>
  Título del documento
</title></pre>

<span style="font-weight: 400">El título del documento se suele cargar, por convenio como contenido de las pestañas de los navegadores web.</span> 
### **El cuerpo del documento**

<span style="font-weight: 400">El cuerpo del documento será el que contenga los elementos de la estructura. Es decir, aquellos elementos que van a dotar de contenido al documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">.</span> <span style="font-weight: 400">El cuerpo del documento se delimita mediante </span>[**el elemento body**][5]<span style="font-weight: 400">.</span> 
<pre><!-- Cuerpo del documento -->
</pre>

<span style="font-weight: 400">Dentro del cuerpo del documento irán todos los elementos que vamos a ir explicando dentro de este manual.</span> <span style="font-weight: 400">Con la estructura del documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> que hemos visto podemos ver como estructura base de cualquier documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> la siguiente:</span> 
<pre><title>
  Título de la Página
</title>
  
  
    

<!-- Cuerpo del documento HTML -->
  
</pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:HTML
 [3]: http://www.w3api.com/wiki/HTML:HEAD
 [4]: http://www.w3api.com/wiki/HTML:TITLE
 [5]: http://www.w3api.com/wiki/HTML:BODY