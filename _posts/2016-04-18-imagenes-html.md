---
ID: 795
post_title: '11 &#8211; Imágenes en HTML'
author: Víctor Cuervo
post_date: 2016-04-18 12:00:05
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/imagenes-html/
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
    http://lineadecodigo.com/tag/html-imagenes/feed/
---
<span style="font-weight: 400">Si solo insertamos texto en nuestras páginas webs, estas quedarán muy sencillas y poco lucidas. Es por ello que en </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> tenemos la capacidad de insertar imágenes.</span> <span style="font-weight: 400">Las imágenes podrán ser elementos representativos de página web o elementos decorativos. Si bien, en el caso de ser elementos decorativos deberíamos de utilizar </span>[<span style="font-weight: 400">CSS</span>][2]<span style="font-weight: 400"> para insertarlos en nuestra página web.</span> <span style="font-weight: 400">El uso de imágenes dentro de una página web tiene que hacerse con cautela, ya que cada imagen que pongamos en nuestra web incrementará el tamaño (peso) de la página. Por lo cual se verá afectado el tiempo de descarga de la página.</span> 
### Insertar una imagen: El elemento img

<span style="font-weight: 400">Para insertar una imagen en HTML tenemos el </span>[<span style="font-weight: 400">elemento img</span>][3]<span style="font-weight: 400">, cuya sintaxis básica es:</span> 
<pre><img src="”nombreimagen.jpg”" alt="" /></pre>

<span style="font-weight: 400">Como podemos comprobar, el </span>[<span style="font-weight: 400">elemento img</span>][3]<span style="font-weight: 400"> es un elemento sencillo, con lo cual no tiene elemento de cierre y termina con la barra invertida.</span> <span style="font-weight: 400">El atributo principal del </span>[<span style="font-weight: 400">elemento img</span>][3]<span style="font-weight: 400"> es </span>[<span style="font-weight: 400">src</span>][4]<span style="font-weight: 400"> nos indica la ruta de la imagen que queremos cargar. Así, si la imagen se encuentra en la misma ruta que nuestra página web pondremos:</span> 
<pre><img src="”foto.jpg”" alt="" /></pre>

<span style="font-weight: 400">En el caso de que la imagen esté en otro directorio, por ejemplo en </span>*<span style="font-weight: 400">“/multimedia/imagenes” </span>*<span style="font-weight: 400">pondremos lo siguiente:</span> 
<pre><img src="”/multimedia/imagenes/foto.jpg”" alt="" /></pre>

<span style="font-weight: 400">Incluso la imagen puede residir en otro servidor. En ese caso la URL que contenga la imagen deberá de indicar el protocolo y el servidor que alberga la imagen. Por ejemplo podremos tener el siguiente código:</span> 
<pre><img src="//lineadecodigo.com/imagenes/logo.jpg”" alt="" /></pre>

### Dimensiones de la imagen: width y height

<span style="font-weight: 400">Si no indicamos más sobre el </span>[<span style="font-weight: 400">elemento img</span>][3]<span style="font-weight: 400">, la imagen que le hayamos pasado en su campo src se cargará con su tamaño original.</span> <span style="font-weight: 400">Si bien disponemos de los atributos </span>[<span style="font-weight: 400">width</span>][5]<span style="font-weight: 400"> para el ancho de la imagen y </span>[<span style="font-weight: 400">height</span>][6]<span style="font-weight: 400"> para el alto de la imagen. De esta forma, si queremos que nuestra imagen se vea en 100x100 pixels, podemos insertar el siguiente código:</span> 
<pre><img src="”foto.jpg”" alt="" width="”100”" height="”100”" /></pre>

<span style="font-weight: 400">El tamaño de la imagen puede ser especificado en pixels o en porcentajes. En caso de omitir la unidad se utilizará el pixel.</span> 
<pre><img src="”foto.jpg”" alt="" width="”100”" height="”100”" />
<img src="”foto.jpg”" alt="" width="”100px”" height="”100px”" />
<img src="”foto.jpg”" alt="" width="”50%”" height="”50%”" /></pre>

<span style="font-weight: 400">Por cuestiones de rendimiento en la carga de las webs siempre es bueno el indicar sus valores </span>[<span style="font-weight: 400">width</span>][5]<span style="font-weight: 400"> y </span>[<span style="font-weight: 400">height</span>][6]<span style="font-weight: 400">.</span> <span style="font-weight: 400">Los valores del alto y el ancho que indiquemos en la </span>[<span style="font-weight: 400">elemento img</span>][3]<span style="font-weight: 400"> no tienen porqué coincidir con el tamaño real de la imagen. Por ejemplo, reduciendo los valores de estos atributos podremos conseguir una previsualización de la misma, lo que se conoce como thumbnail.</span> 
### Texto alternativo de la imagen: el atributo alt y longdesc

<span style="font-weight: 400">Sobre una imagen podemos indicar un texto alternativo o descriptivo de la misma. Para ello tenemos el </span>[<span style="font-weight: 400">atributo alt</span>][7]<span style="font-weight: 400">.</span> 
<pre><img src="”foto.jpg”" alt="”texto" /></pre>

<span style="font-weight: 400">Pero, ¿por qué quiero poner un texto, cuando realmente es una imagen gráfica?</span> <span style="font-weight: 400">Piensa que esto es útil en varios casos. Por ejemplo, si por algún problema técnico no se puede cargar la imagen, el navegador mostrará en su espacio el texto alternativo, lo cual dará al usuario una idea de lo que iba en ese sitio.</span> <span style="font-weight: 400">Otra cosa útil es para cuando nuestra página sea utilizada por personas discapacitadas con problemas de visibilidad. En este caso estas personas disponen de herramientas que le van leyendo la página y cuando llegan a una imagen leen el contenido que encuentran en el </span>[<span style="font-weight: 400">atributo alt</span>][7]<span style="font-weight: 400">.</span> <span style="font-weight: 400">Es por ello que el texto alternativo que insertemos en la imagen debe de ser bastante descriptivo de la misma. En algunos casos se llega hasta indicar el tamaño de la imagen.</span> 
<pre><img src="”foto.jpg”" alt="”Fotografía" /></pre>

### Tipos de formatos de imágenes

<span style="font-weight: 400">Hemos aprendido mucho de cómo podemos insertar nuestras imágenes en el documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">. Pero a la hora de insertar imágenes, qué tipo de imágenes puedo insertar en el documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">.</span> <span style="font-weight: 400">En este punto tenemos un pequeño problema y es que los estándares de </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> no definen los tipos de formato de imagen que se pueden ver en un navegador web.</span> <span style="font-weight: 400">Los formatos de imágenes más comúnmente aceptados son:</span> 
<li style="font-weight: 400">
  <b>JPEG,</b><span style="font-weight: 400"> son imágenes digitales comprimidas con pérdida de información. Pero que nos permiten tener imágenes digitales que ocupen poco espacio.</span>
</li>
<li style="font-weight: 400">
  <b>GIF,</b><span style="font-weight: 400"> es un formato para imágenes de mapas de bits las cuales soportan 8 bits por pixel. El formato GIF soporta imágenes animadas.</span>
</li>
<li style="font-weight: 400">
  <b>PNG,</b><span style="font-weight: 400"> es un formato de imagen en mapa de bits que emplea compresión de datos sin pérdida de información. No requieren de licencia de patente. Es un formato creado para utilizar imágenes en Internet con un tamaño adecuado.</span>
</li>

<span style="font-weight: 400">Otros formatos que también son aceptados:</span> 
<li style="font-weight: 400">
  <b>APNG,</b><span style="font-weight: 400"> son imágenes PNG animadas. Intenta evolucionar los gráficos animados en GIF.</span>
</li>
<li style="font-weight: 400">
  <b>SVG</b><span style="font-weight: 400">, gráficos vectoriales escalables. Son gráficos especificados mediante texto, lo cual hace que sean interpretables por los dispositivos y puedan escalar a través de diferentes resoluciones.</span>
</li>
<li style="font-weight: 400">
  <b>BMP</b><span style="font-weight: 400">, son imágenes de mapas de bits. Se pueden encontrar con extensión .bmp y .dib</span>
</li>
<li style="font-weight: 400">
  <b>BMP ICO y PNG ICO</b><span style="font-weight: 400">, formato para representar iconos en el sistema operativo Windows. Los iconos suelen contener diferentes tamaños y densidad de pixels. De esta forma pueden ser escalados.</span>
</li>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.manualweb.net/tutorial-css/
 [3]: http://w3api.com/wiki/HTML:IMG
 [4]: http://www.w3api.com/wiki/HTML:Src
 [5]: http://www.w3api.com/wiki/HTML:Width
 [6]: http://www.w3api.com/wiki/HTML:Height
 [7]: http://www.w3api.com/wiki/HTML:Alt