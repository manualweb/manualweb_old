---
ID: 756
post_title: '08 &#8211; Metadatos: Las metatags de HTML'
author: Víctor Cuervo
post_date: 2016-04-11 12:00:47
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/metadatos-las-metatags-html/
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
<span style="font-weight: 400;">Las metatags de </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;"> nos permiten dotar de metadatos a la página </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;">. Es decir de información relativa al contenido de la página, pero que no se representa de ninguna forma. </span><b>Si bien son muy importantes ya que será una parte de información que leerán los buscadores web y un correcto uso de los metadatos harán que nuestra página sea mejor o peor indexada</b><span style="font-weight: 400;">.</span>

<span style="font-weight: 400;">Por ejemplo podremos encontrar dentro de los metadatos, la descripción de la página, un conjunto palabras que describan la página, el tipo de codificación de la página, información relativa al autor de la página o con qué herramienta ha sido construida, entre otras más.</span>

<span style="font-weight: 400;">La estructura general de las meta-tags se define mediante </span><a href="http://www.w3api.com/wiki/HTML:META"><span style="font-weight: 400;">el elemento meta</span></a><span style="font-weight: 400;">:</span>

<pre lang="html4strict"><meta name=”metadato” content=”valor” http-equiv=”cabecera-http” schema=”esquema”/></pre>

<span style="font-weight: 400;">Dentro de los metadatos podríamos diferenciarlos de tres tipos:</span>
<ul>
	<li style="font-weight: 400;"><b>Metadatos generales</b><span style="font-weight: 400;">, que proporcionan información relativa al documento </span><a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400;">HTML</span></a><span style="font-weight: 400;">.</span></li>
	<li style="font-weight: 400;"><b>Metadatos http</b><span style="font-weight: 400;">, son aquellos que modifican alguna propiedad de las cabeceras http.</span></li>
</ul>
<h3>Metadatos Generales</h3>
<span style="font-weight: 400;">Nos permiten definir información de metadatos generales del documento: autor, descripción palabras clave,... Es estándar HTML 4.01 no define un perfil de metadatos a utilizar y deja abierto su uso. Si bien hace referencia al </span><a href="http://www.metatags.org/dublin_core_metadata_element_set"><span style="font-weight: 400;">Dublin Core Profile</span></a><span style="font-weight: 400;"> para la descripción de documentos electrónicos.</span>

<span style="font-weight: 400;">Algunos de los metadatos más utilizados son:</span>
<h4>Author</h4>
<span style="font-weight: 400;">Para hacer referencia al autor del documento. La estructura sería:</span>

<pre lang="html4strict"><meta name=”author” content=”Manual Web” /></pre>
<h4>Description</h4>
<span style="font-weight: 400;">Define la descripción del contenido del documento a forma de resumen. Su uso sería:</span>

<pre lang="html4strict"><meta name=”description” content=”Manual Web que nos explica el uso del lenguaje HTML” /></pre>

<h4>Keywords</h4>
<span style="font-weight: 400;">Conjunto de palabras que describen el documento. Las palabras van separadas por comas. Se escribiría de la siguiente forma:</span>

<pre lang="html4strict"><meta name=”keywords” content=”manual,html,elementos,atributos,ejemplos” /></pre>

<h4>Revised</h4>
<span style="font-weight: 400;">Información relativa a cuándo el documento fue revisado por última vez. Se utilizará de la siguiente forma:</span>

<pre lang="html4strict"><meta name=”revised” content=”24/03/2016” /></pre>

<h3>Metadatos Cabeceras HTTP</h3>
<span style="font-weight: 400;">Las cabeceras http suelen ser establecidas en el servidor, si bien podemos modificarlas en el cliente mediante las meta-tags. El navegador realizará alguna acción al interpretar estas cabeceras. Por ejemplo podemos decirle al navegador cada cuanto tiempo tiene que recargar la página, o durante cuánto tiempo debe de cachear la página.</span>

<span style="font-weight: 400;">Estos metadatos se apoyan en el </span><b>atributo http-equiv</b><span style="font-weight: 400;">.</span>
<h4>Refresh</h4>
<span style="font-weight: 400;">Especifica cada cuanto tiempo tiene que recargar la página el navegador web. El tiempo es en segundos.</span>

<pre lang="html4strict"><meta http-equiv=”refresh” content=”5” /></pre>

<span style="font-weight: 400;">Incluso podemos utilizar este tipo para hacer una redirección a otra página.</span>

<pre lang="html4strict"><meta http-equiv=”refresh” content=”2; http://lineadecodigo.com” /></pre>

<h4>Content-type</h4>
<span style="font-weight: 400;">Nos sirve para identificar el tipo de documento, que será un documento de tipo text/html y la codificación del contenido. Si es ISO 8859-1, UTF-8,... Esto servirá al navegador a interpretar los caracteres que vayan dentro del contenido.</span>

<pre lang="html4strict"><meta http-equiv=”content-type” content=”text/html; charset=UTF-8"” /></pre>

<h4>Cookie</h4>
<span style="font-weight: 400;">Nos sirve para guardar una cookie. Los datos guardados son clave/valor</span>

<pre lang="html4strict"><meta http-equiv=”cookie” content=”clave=valor; expires=Saturday, 25-Mar-16 23:59:59 GMT;” /></pre>

<h3>Metadatos y el Open Graph Protocol</h3>
<span style="font-weight: 400;">Como hemos comentado anteriormente la especificación HTML 4.01 no habla de un perfil de metadatos. Es por ello que hay diferentes perfiles que están proliferando diferentes perfiles que nos permiten metadatar el documento con algún fin.</span>

<span style="font-weight: 400;">Uno de esos perfiles es el </span><a href="http://ogp.me/"><span style="font-weight: 400;">Open Graph Protocol</span></a><span style="font-weight: 400;">, este perfil es utilizado, entre otros, por Facebook para poder interpretar el documento de una forma más sencilla.</span>

<span style="font-weight: 400;">Algunos de los metadatos que define el </span><a href="http://ogp.me/"><span style="font-weight: 400;">Open Graph Protocol</span></a><span style="font-weight: 400;"> son:</span>
<h4>og:title</h4>
<span style="font-weight: 400;">Define el título del documento.</span>

<pre lang="html4strict"><meta name=”og:title” content=”Manual Web. Manuales en Español” /></pre>
<h4>og:type</h4>
<span style="font-weight: 400;">Indica el tipo de objeto que representa la página. Si es un artículo, un vídeo, una imagen,...</span>

<pre lang="html4strict"><meta name=”og:type” content=”article” /></pre>
<h4>og:image</h4>
<span style="font-weight: 400;">Permite establecer la imagen más representativa del documento</span>

<pre lang="html4strict"><meta name=”og:image” content=”http://www.manualweb.net/logo.png” /></pre>

<h4>og:url</h4>
<span style="font-weight: 400;">Nos ayuda a definir la URL asociada al documento. Esto es por si queremos utilizar alguna diferente a la URL que ya tenga.</span>

<pre lang="html4strict"><meta name=”og:url” content=”http://www.manualweb.net” /></pre>