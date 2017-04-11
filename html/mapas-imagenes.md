---
ID: pdte
post_title: '12 &#8211; Mapas de Imágenes'
author: Víctor Cuervo
post_date: 2017-04-12 01:04
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/mapas-imagenes/
published: false
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-imagenes/feed/
gitfolder: html
---
<span style="font-weight: 400;">Los mapas de imágenes nos permiten crear un conjunto de enlaces dentro de una imagen o bien enlazar una parte en concreto de una imagen. Para ello </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> nos ofrece el </span>[<span style="font-weight: 400;">elemento map</span>][2]<span style="font-weight: 400;">.</span> <span style="font-weight: 400;">La estructura del </span>[<span style="font-weight: 400;">elemento map</span>][2]<span style="font-weight: 400;"> es la siguiente:</span> <pre lang="html4strict"><map name="”nombreMapa”">
  <area />
   
  <area />
  ...

</map>
</pre>

<span style="font-weight: 400;">Lo que vemos es que el elemento map anida un conjunto de elementos area. Los </span>[<span style="font-weight: 400;">elementos area</span>][3]<span style="font-weight: 400;"> serán los que establezcan las zonas enlazables dentro de la imagen.</span> <span style="font-weight: 400;">Es importante saber que el mapa en sí no tiene una imagen asociada, si no que tendremos que asociar un </span>[<span style="font-weight: 400;">elemento img</span>][4]<span style="font-weight: 400;"> al mapa para conseguir tener los áreas enlazables.</span>
### Nombre del Mapa

<span style="font-weight: 400;">Una de las cosas más importantes en los mapas de imágenes es darle un nombre. Ya que este nombre será el que enlacemos sobre la imagen para poder usar el mapa de imágenes.</span> <span style="font-weight: 400;">El nombre del mapa de imágenes se da mediante el </span>[<span style="font-weight: 400;">atributo name</span>][5]<span style="font-weight: 400;">.</span> <map name="”nombreMapa”">
</map>

### Tipos de Áreas

<span style="font-weight: 400;">Dentro de los tipos de áreas que podemos crear dentro de una imagen tenemos diferentes formas:</span>
<li style="font-weight: 400;">
  <b>Círculo,</b><span style="font-weight: 400;"> define una región mediante un círculo.</span>
</li>
<li style="font-weight: 400;">
  <b>Rectángulo,</b><span style="font-weight: 400;"> define la región mediante un rectángulo.</span>
</li>
<li style="font-weight: 400;">
  <b>Polígono, </b><span style="font-weight: 400;">define una región mediante un conjunto de puntos que representan un polígono</span>
</li>
<li style="font-weight: 400;">
  <b>Por defecto,</b><span style="font-weight: 400;"> sería el resto de zonas no referenciada por ninguna zona.</span>
</li>

<span style="font-weight: 400;">El </span>[<span style="font-weight: 400;">elemento area</span>][3]<span style="font-weight: 400;"> tiene la siguiente estructura:</span> <pre lang="html4strict"></pre>

<span style="font-weight: 400;">Dónde </span>[<span style="font-weight: 400;">shape</span>][6]<span style="font-weight: 400;"> es la forma a utilizar, </span>[<span style="font-weight: 400;">coords</span>][7]<span style="font-weight: 400;"> el conjunto de coordenadas que define la forma. Dependiendo de la forma utilizada serán unas coordenadas u otras. El </span>[<span style="font-weight: 400;">atributo href</span>][8]<span style="font-weight: 400;"> contendrá el enlace y </span>[<span style="font-weight: 400;">alt</span>][9]<span style="font-weight: 400;"> el texto alternativo a ese enlace.</span>
#### Circle

<span style="font-weight: 400;">Esta forma define un área circular dentro del mapa. En este caso las coordenadas son x,y como centro del círculo y radio.</span> <pre lang="html4strict"><map>
  <area coords="”x,y,radio”/" shape="”circle”" />

</map>
</pre>

#### Rect

<span style="font-weight: 400;">Representa una forma rectangular en el mapa de imágenes. Las coordenadas son x1,y1 de la esquina superior izquierda seguido de x2,y2 de la esquina inferior derecha.</span> <pre lang="html4strict"><map>
  <area coords="”x1,y1,x2,y2”/" shape="”rect”" />

</map>
</pre>

#### Poly

<span style="font-weight: 400;">Representa una forma de un polígono definido por un conjunto de puntos. Las coordenadas son x1,y1, x2, y2, x3, y3,..., xN, yN. Dónde la primer coordenada y la última deben de coincidir para poder cerrar el polígono.</span> <pre lang="html4strict"><map>
  <area coords="”x1,y1,x2,y2,x3,y3,...,xN,yN”/" shape="”poly”" />

</map>
</pre>

#### **Default**

<span style="font-weight: 400;">Representa el resto de zonas del mapa que no hayan sido referenciadas por ninguna forma. En este caso no hay coordenadas.</span>
### Asociar Mapa a Imagen

<span style="font-weight: 400;">Lo siguiente que tenemos que hacer es definir la imagen mediante el </span>[<span style="font-weight: 400;">elemento img</span>][4]<span style="font-weight: 400;">.</span> <pre lang="html4strict"><img src="”imagen.jpg”" alt="" /></pre>

<span style="font-weight: 400;">Y asociarla el mapa de imágenes. Para ello utilizamos el </span>[<span style="font-weight: 400;">atributo usemap</span>][10]<span style="font-weight: 400;"> al cual asignaremos el valor indicado en el </span>[<span style="font-weight: 400;">atributo name</span>][5]<span style="font-weight: 400;"> del mapa.</span> <pre lang="html4strict"><img src="”imagen.jpg”" alt="" usemap="”#mapa”" /></pre>

### Ejemplo de Mapa de Imágenes

<span style="font-weight: 400;">Para ver el uso de los mapas de imágenes analizaremos el siguiente caso. Vamos a partir de la siguiente imagen y vamos a definir tres mapas. El primero será un área circular sobre el segundo logo, el segundo será un área rectangular sobre el tercer logo y el tercero será un polígono sobre el último logo. En caso de que pinche en otro sitio se irá al enlace del HTML5 que será un área por defecto.</span> <img class="aligncenter size-full wp-image-800" src="http://www.manualweb.net/wp-content/uploads/2016/04/image06.png" alt="image06" width="750" height="250" /> <span style="font-weight: 400;">Así tendremos el siguiente mapa:</span> <pre lang="html4strict"><map name="mapalogos">
  <area coords="405,73,520,166" shape="rect" href="#" />

  <area coords="748,248,750,250" shape="rect" href="#" />

  <area coords="571,119,626,59,687,118,628,177" shape="poly" href="#" />

  <area shape="default" href="#" />

</map>
</pre>

<span style="font-weight: 400;">Y el siguiente uso del mapa desde la imagen</span> <pre lang="html4strict"><img src="logos.png" alt="Mapa de Logos" usemap="#mapalogos" /></pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:MAP
 [3]: http://www.w3api.com/wiki/HTML:AREA
 [4]: http://www.w3api.com/wiki/HTML:IMG
 [5]: http://www.w3api.com/wiki/HTML:Name
 [6]: http://www.w3api.com/wiki/HTML:Shape
 [7]: http://www.w3api.com/wiki/HTML:Coords
 [8]: http://www.w3api.com/wiki/HTML:Href
 [9]: http://www.w3api.com/wiki/HTML:Alt
 [10]: http://www.w3api.com/wiki/HTML:Usemap
