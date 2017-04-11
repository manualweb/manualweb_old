---
ID: 1359
post_title: 05 – Sintaxis del HTML
author: Víctor Cuervo
post_date: 2017-04-11 23:47:57
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/sintaxis-del-html/
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
urlvideo:
  - PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos:
  - >
    http://lineadecodigo.com/tag/html-basicos/feed/
gitfolder:
  - html
---
En la sintaxis del HTML hablamos sobre: [TOC] <span style="font-weight: 400">Dentro del </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> vamos a encontrar diferentes estructuras que deberemos de diferenciar. En primer lugar están </span>**los elementos**<span style="font-weight: 400"> que es la principal estructura del lenguaje y los que conforman las páginas web.</span> <span style="font-weight: 400">A su vez los elementos contendrán </span>**atributos**<span style="font-weight: 400">. Los atributos dan más especificidad al comportamiento de los elementos, permitiendo parametrizarlos.</span>

### **Los elementos HTML**

<span style="font-weight: 400">Los elementos </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> son los que configuran la estructura de la página. También son llamados en algunos sitios como etiquetas, derivado del tema del lenguaje de marcado. Si bien su nombre correcto es el de elementos.</span> <span style="font-weight: 400">Todo elemento se encierra entre los símbolos <strong>menor que <</strong> y <strong>mayor que ></strong>:</span>

<pre><span style="font-weight: 400">&lt;elemento&gt;</span></pre>

<span style="font-weight: 400">Dentro de los elementos </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> encontramos dos tipos:</span> <li style="font-weight: 400">
  <span style="font-weight: 400">Elementos que tienen un inicio y un cierre</span>
</li>
<li style="font-weight: 400">
  <span style="font-weight: 400">Elementos únicos</span>
</li>

<span style="font-weight: 400">Los </span>**elementos que tienen un inicio y un cierre**<span style="font-weight: 400"> permiten tener a otros elementos u otro contenido anidado, es decir, a otros elementos o directamente texto. La estructura de los elementos de inicio y cierre es la siguiente:</span>

<pre><span style="font-weight: 400">&lt;elemento&gt; contenido| subelementos &lt;/elemento&gt;</span></pre>

<span style="font-weight: 400">Como podemos apreciar el elemento de cierre se precede de una barra invertida.</span> <span style="font-weight: 400">Algunos de estos elementos son </span>[<span style="font-weight: 400">p</span>][2]<span style="font-weight: 400">, </span>[<span style="font-weight: 400">div</span>][3]<span style="font-weight: 400">, </span>[<span style="font-weight: 400">ul</span>][4]<span style="font-weight: 400">,...</span> <span style="font-weight: 400">En el caso de los elementos únicos, estos no permiten anidar contenido y aparecen de forma aislada. Su estructura es la siguiente:</span>

<pre><span style="font-weight: 400">&lt;elemento /&gt;</span></pre>

<span style="font-weight: 400">Como podemos apreciar la barra invertida se encuentra al final y dentro del elemento. Algún ejemplo de estos elementos es </span>[<span style="font-weight: 400">img</span>][5]<span style="font-weight: 400">, </span>[<span style="font-weight: 400">br</span>][6]<span style="font-weight: 400">,...</span>

### **Atributos en HTML**

<span style="font-weight: 400">Los elementos pueden ser parametrizados mediante los atributos. Los atributos siguen la estructura nombre/valor y se deberán de poner antes del cierre del elemento.</span> <span style="font-weight: 400">La estructura de definición de los atributos es la siguiente:</span>

<pre><span style="font-weight: 400">&lt;elemento atributo=”valor”&gt;</span></pre>

<span style="font-weight: 400">El valor del atributo estará delimitado mediante comillas simples o comillas dobles.</span>

### **Entidades en HTML**

<span style="font-weight: 400">Otra estructura que nos podemos encontrar dentro de una página </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> son las entidades. Las entidades <strong>empiezan por un ampersand &</strong>, seguidas del <strong>código de la entidad</strong> -que puede ser numérico o alfanumérico- y <strong>finalizan en un punto y coma ;</strong></span> <span style="font-weight: 400">La estructura de una entidad en </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> será la siguiente:</span>

<pre><span style="font-weight: 400">&código;</span></pre>

<span style="font-weight: 400">Las entidades nos sirven para representar símbolos que son parte de la estructura del lenguaje, como es el caso de los símbolos mayor y menor. O símbolos específicos de un determinado juego de caracteres, cómo podrían ser símbolos de monedas o caracteres especiales.</span>

<pre>&lt;      representa &lt;
&gt;      representa &gt;
"    representa ‘
&eur;     representa €</pre>

<span style="font-weight: 400">Ya hablaremos en detalle sobre ellas más adelante.</span>

### **Comentarios en HTML**

<span style="font-weight: 400">Para poder insertar un comentario dentro de las páginas </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> deberemos de utilizar la siguiente estructura:</span>

<pre><!-- comentario --></pre>

El comentario puede tener varias líneas de texto.

<pre><!-- esto es
         un comentario --></pre>

### **Normas de codificación en un documento HTML**

<span style="font-weight: 400">Existen una serie de normas de codificación que hay que conocer y seguir dentro del lenguaje </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> a la hora de crear nuestras páginas web.</span>

#### **No sensible a mayúsculas**

<span style="font-weight: 400">El lenguaje </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> no es sensible a mayúsculas. Es decir, que da igual que escribamos nuestros elementos y atributos en mayúsculas y/o minúsculas.</span> <span style="font-weight: 400">Si bien, por convenio, </span>**se recomienda que tanto los elementos como los atributos sean escritos en minúsculas**<span style="font-weight: 400">.</span>

#### **Espacios en blanco**

<span style="font-weight: 400">Si insertamos un espacio en blanco dentro de nuestra página se generará un espacio en blanco dentro de la visualización. Si bien si juntamos varios espacios en blancos, </span>**estos solo generarán un único espacio en blanco**<span style="font-weight: 400">.</span> <span style="font-weight: 400">Lo mismo ocurre si insertamos una o varias tabulaciones. Estas solo generan un único espacio en blanco. Si queremos crear un conjunto de espacios en blanco seguidos deberemos de utilizar la entidad: </span>

<pre>&nbsp;</pre>

<span style="font-weight: 400">Cada vez que insertemos esta entidad generamos un espacio en blanco.</span>

#### **Saltos de línea**

<span style="font-weight: 400">Los saltos de línea que insertemos dentro de la página web no tienen ningún efecto de cara a la renderización del contenido. Por lo tanto, un salto de línea en el código no genera nada.</span> Si queremos insertar un salto de línea dentro de nuestra página web deberemos de utilizar el elemento

<pre><br /></pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:P
 [3]: http://www.w3api.com/wiki/HTML:DIV
 [4]: http://www.w3api.com/wiki/HTML:UL
 [5]: http://www.w3api.com/wiki/HTML:IMG
 [6]: http://www.w3api.com/wiki/HTML:BR