---
ID: 765
post_title: '09.01 &#8211; Texto básico en HTML'
author: Víctor Cuervo
post_date: 2016-04-15 12:00:51
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/texto-basico-html/
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
---
<a name="br"></a>
### Saltos de línea en el texto Está claro que escribir el texto todo seguido, sin darle un orden o una separación, sería un caos. Así que lo primero que vamos a aprender es el crear un salto de línea en el texto. Y es que si escribimos lo siguiente: 

<pre>Esta es una línea

Y esta otra línea.</pre> Veremos que al cargar nuestra página web no se producirá el efecto deseado y que no existe la separación entre las dos líneas. Y es que el salto de línea en un documento web equivale a un espacio en blanco a la hora de visualizarse. Y si ponemos muchos saltos de línea seguidos solo se contabilizará el primero, que será el que equivalga a un espacio en blanco. Para poder añadir un salto de línea deberemos de utilizar el 

[elemento br][1]. El [elemento br][1] es un elemento simple. Es decir, no tiene un elemento de inicio y un elemento de cierre. Así, para representar dos saltos de línea utilizaremos el siguiente código: 
<pre>Esta es una línea <br /><br />
Y esta otra línea.</pre>

<a name="p"></a>
### Organizando el texto en párrafos Ahora que conocemos el 

[elemento br][1] vemos su potencial, si bien, si queremos dar estilo a un documento a base de datos de línea, veremos que es bastante complicado. Es por eso que el lenguaje [HTML][2] nos ofrece otra serie de elementos para organizar el contenido del texto. Así contamos con párrafos, los cuales son representados mediante el [elemento p][3]. En este caso el [elemento p][3] tiene una elemento de inicio y un elemento de cierre. Y el contenido de dentro será lo que representa al párrafo. 
<pre><p>
  Parrafo>/p></pre>
  
  De esta manera si queremos generar dos párrafos crearemos el siguiente código.
  
  <pre><p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed a felis non sem elementum tempor in at urna. Suspendisse auctor libero ut nibh consequat sed sagittis dolor iaculis. Donec condimentum mauris nec eros auctor sed vestibulum tellus consequat. Pellentesque tincidunt hendrerit neque, tincidunt tempus mauris consequat non.
</p>



<p>
  Nullam interdum, enim sed ultrices sagittis, nibh tortor viverra lacus, eu tristique risus sapien et eros. Cras gravida, felis sed sagittis convallis, nulla ante vehicula justo, id imperdiet enim nisi id mauris. Nunc egestas volutpat congue. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vehicula purus eu enim vulputate rhoncus.
</p></pre>
  
  
  
  <a name="hx"></a><h3>
    Elementos de cabecera o titulares
  </h3>
  Si seguimos revisando el poder dar formato al texto nos encontramos con los elementos de cabecera o titulares.
  Estos elementos nos servirán para poner títulos a las diferentes secciones que tenga nuestra web. Son dos elementos, el de inicio y el de cierre y el contenido será el nombre de la cabecera o titular.
  
  El 
  
  <a href="http://www.w3api.com/wiki/HTML:H1">elemento es de tipo hx</a>, donde la x va desde el 1 hasta el 6. Por ejemplo, si queremos poner un elemento de cabecera de tipo 1 escribiríamos lo siguiente:
  
  <pre><h1>
  Cabecera o Titulo
</h1></pre>
  
  Así veríamos todos los elementos de cabecera:
  
  
  
  <pre><h1>
  Cabecera de tipo H1
</h1>


<h2>
  Cabecera de tipo H2
</h2>


<h3>
  Cabecera de tipo H3
</h3>


<h4>
  Cabecera de tipo H4
</h4>


<h5>
  Cabecera de tipo H5
</h5>


<h6>
  Cabecera de tipo H6
</h6></pre>
  
  
  
  <a name="cite"></a><h3>
    Crear una cita
  </h3>
  Otro elemento que nos servirá para organizar nuestro documento 
  
  <a href="http://www.manualweb.net/tutorial-html/">HTML</a> será el <a href="http://www.w3api.com/wiki/HTML:BLOCKQUOTE">elemento blockquote</a> o <a href="http://www.w3api.com/wiki/HTML:Q">q</a>. Este elemento nos permite reseñar una cita.
  
  La diferencia entre el <a href="http://www.w3api.com/wiki/HTML:BLOCKQUOTE">elemento blockquote</a> y <a href="http://www.w3api.com/wiki/HTML:Q">elemento q</a> es qué <a href="http://www.w3api.com/wiki/HTML:BLOCKQUOTE">blockquote</a> será un elemento de párrafo en si mismo, mientras que <a href="http://www.w3api.com/wiki/HTML:Q">q</a> será autocontenida dentro de otro texto, lo que se conoce como un elemento en línea.
  
  De esta forma, una cita con <a href="http://www.w3api.com/wiki/HTML:BLOCKQUOTE">blockquote</a> será:
  
  <pre><blockquote>
  "Muchas veces me moría pensando que no iba verte. Pero moría la muerte cada vez que te veía". Eduardo Galeano
</blockquote></pre>
  
  Y una cita con 
  
  <a href="http://www.w3api.com/wiki/HTML:Q">q</a> puede ser:
  
  <pre>El primer ministro afirmó que <q>”era el mejor momento económico para el páis”</q> el pasado día 8.</pre>
  
  Los elementos 
  
  <a href="http://www.w3api.com/wiki/HTML:BLOCKQUOTE">blockquote</a> y <a href="http://www.w3api.com/wiki/HTML:Q">q</a> nos permiten indicar el origen de la cita mediante el <b>atributo cite</b>.
  
  <pre>El primer ministro afirmó que <q cite="//elpais.com/”">”era el mejor momento económico para el país”</q> el pasado día 8.</pre>
  
  Y el idioma en el que está escrita la cita, mediante el 
  
  <a href="http://www.w3api.com/wiki/HTML:Lang">atributo lang</a>:
  
  <pre>El primer ministro afirmó que <q>”era el mejor momento económico para el páis”</q> el pasado día 8.</pre>
  
  
  
  <a name="subsup"></a><h3>
    Algo para las fórmulas: Subíndices y Superíndices
  </h3>
  Aunque existen lenguajes de marcado especiales para la representación de fórmulas matemáticas, como puede ser MathML, en 
  
  <a href="http://www.manualweb.net/tutorial-html/">HTML</a> encontramos un par de elementos que nos permitirán crear subíndices y superíndices. Estos son los elementos <a href="http://www.w3api.com/wiki/HTML:SUB">sub</a> y <a href="http://www.w3api.com/wiki/HTML:SUP">sup</a> respectivamente.
  
  La representación del contenido irá entre el elemento de inicio y el elemento de cierre.
  
  <pre><sup>superíndice</sup>
<sub>subíndice</sub></pre>
  
  Podemos escribir algunas notas matemáticas como:
  
  
  
  <pre>Como indica el teorema de Pitágoras:
hipotenusa<sup>2</sup> = cateto1<sup>2</sup>+cateto2<sup>2</sup></pre>
  
  O químicas como:
  
  
  
  <pre>El símbolo del agua es H<sub>2</sub>O.</pre>
  
  
  
  <a name="em"></a><h3>
    Enfatizando un texto
  </h3>
  Una de las opciones que encontramos dentro del 
  
  <a href="http://www.manualweb.net/tutorial-html/">HTML</a> es la de enfatizar un texto. Para ello el lenguaje <a href="http://www.manualweb.net/tutorial-html/">HTML</a> nos ofrece el <a href="http://www.w3api.com/wiki/HTML:EM">elemento em</a>.
  
  El texto que vaya dentro de los elementos de inicio y de cierre del <a href="http://www.w3api.com/wiki/HTML:EM">elemento em</a> será el texto que aparece enfatizado en nuestro navegador.
  
  Así podemos escribir el siguiente texto:
  
  <pre>Más vale <em>pájaro en mano</em> que ciento volando.</pre>
  
  
  
  <a name="strong"></a><h3>
    Resaltando un texto, más énfasis
  </h3>
  Si el énfasis que nos proporciona el 
  
  <a href="http://www.w3api.com/wiki/HTML:EM">elemento em</a> no es suficiente para nuestro cometido, si queremos resaltar todavía más el texto, podemos utilizar el <a href="http://www.w3api.com/wiki/HTML:STRONG">elemento strong</a>.
  
  El <a href="http://www.w3api.com/wiki/HTML:STRONG">elemento strong</a> tiene un comportamiento similar al <a href="http://www.w3api.com/wiki/HTML:EM">elemento em</a>.
  
  Así, si queremos resaltar más un texto, podemos escribir.
  
  <pre>A enemigo que huye, <strong>puente de plata</strong>.</pre>
  
  Aunque 
  
  <b>la mayoría de los navegadores representan el resaltado del texto </b><a href="http://www.w3api.com/wiki/HTML:STRONG"><b>strong</b></a><b> en negrita</b> no debemos de confundir esto con el fin del <a href="http://www.w3api.com/wiki/HTML:STRONG">elemento strong</a>, el cual es meramente estructural.

 [1]: http://www.w3api.com/wiki/HTML:BR
 [2]: http://www.manualweb.net/tutorial-html/
 [3]: http://www.w3api.com/wiki/HTML:P