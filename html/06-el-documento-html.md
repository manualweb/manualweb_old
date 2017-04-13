---
ID: 1343
post_title: 06 – El documento HTML
author: Víctor Cuervo
post_date: 2017-04-11 23:49:47
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/el-documento-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-basicos/feed/
gitfolder: html
---
En **el documento HTML** hablamos de:

[TOC]

El documento [HTML][1] tiene dos partes bien diferenciadas. La primera será **la cabecera** del documento en la que irá información relativa a la semántica del documento, metadatos, o a los recursos que necesita para su correcta visualización.

Por otro lado tenemos el cuerpo. **El cuerpo** contendrá la estructura del documento [HTML][1]. Dentro del cuerpo iremos situando los diferentes elementos del lenguaje [HTML][1] para la correcta visualización de la página.

Pero el documento [HTML][1] se caracteriza por empezar y terminar por el [**elemento html**][2]. Es decir, al principio y al final del documento encontraremos el elemento de inicio y cierre respectivamente.

```
<html>
  <!-- Documento HTML -->
</html>
```

Importante es saber que antes del primer [elemento html][2] vamos a encontrar la definición del tipo de documento [HTML][1] sobre el que trabajemos. Como vimos en el capítulo tipos de documentos [HTML][1] podemos tener diferentes tipos o doctypes.

De esta forma la estructura básica del documento [HTML][1] será la siguiente:

```
<! doctype html>
<html>
  <!-- Documento HTML -->
</html>
```

### La cabecera del documento

Lo primero que encontraremos dentro del documento [HTML][1] será la cabecera. La cabecera se delimita mediante [**el elemento head**][3].

<pre></pre>

Dentro de la cabecera vamos a encontrar elementos que nos definen la semántica del documento, estos serán las metatags o metadatos. Además podremos encontrar scripts, hojas de estilo y el más importante, el título de la página. Es importante remarcar que el contenido que se encuentre dentro de la cabecera no tiene una representación visual directa.

#### **Título del documento**

El título del documento se definirá utilizando [**el elemento title**][4]. Cómo contenido del elemento encontraremos el texto que represente dicho título. La estructura sería la siguiente:

<pre><title>
  Título del documento


</title></pre>

El título del documento se suele cargar, por convenio como contenido de las pestañas de los navegadores web.

### **El cuerpo del documento**

El cuerpo del documento será el que contenga los elementos de la estructura. Es decir, aquellos elementos que van a dotar de contenido al documento [HTML][1]. El cuerpo del documento se delimita mediante [**el elemento body**][5].

<pre><!-- Cuerpo del documento -->
</pre>

Dentro del cuerpo del documento irán todos los elementos que vamos a ir explicando dentro de este manual. Con la estructura del documento [HTML][1] que hemos visto podemos ver como estructura base de cualquier documento [HTML][1] la siguiente:

<pre>&lt;! doctype html&gt;



    <!-- Cuerpo del documento HTML -->

</pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:HTML
 [3]: http://www.w3api.com/wiki/HTML:HEAD
 [4]: http://www.w3api.com/wiki/HTML:TITLE
 [5]: http://www.w3api.com/wiki/HTML:BODY
