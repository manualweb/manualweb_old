---
ID: 1355
post_title: '08 – Metadatos: Las metatags de HTML'
author: Víctor Cuervo
post_date: 2017-04-11 23:58:17
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/metadatos-las-metatags-de-html/
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
Las metatags de [HTML][1] nos permiten dotar de metadatos a la página [HTML][1]. Es decir de información relativa al contenido de la página, pero que no se representa de ninguna forma. **Si bien son muy importantes ya que será una parte de información que leerán los buscadores web y un correcto uso de los metadatos harán que nuestra página sea mejor o peor indexada**.

Por ejemplo podremos encontrar dentro de los metadatos, la descripción de la página, un conjunto palabras que describan la página, el tipo de codificación de la página, información relativa al autor de la página o con qué herramienta ha sido construida, entre otras más.

La estructura general de las meta-tags se define mediante [el elemento meta][2]:

~~~html
<meta name=”metadato” content=”valor” http-equiv=”cabecera-http” schema=”esquema”/>
~~~

Dentro de los metadatos podríamos diferenciarlos de tres tipos:

* **Metadatos generales**, que proporcionan información relativa al documento [HTML][1].
* **Metadatos http**, son aquellos que modifican alguna propiedad de las cabeceras http.

### Metadatos Generales

Nos permiten definir información de metadatos generales del documento: autor, descripción palabras clave,... Es estándar HTML 4.01 no define un perfil de metadatos a utilizar y deja abierto su uso. Si bien hace referencia al [Dublin Core Profile][3] para la descripción de documentos electrónicos. Algunos de los metadatos más utilizados son:

#### Author

Para hacer referencia al autor del documento. La estructura sería:

~~~html
<meta name=”author” content=”Manual Web” />
~~~

#### Description

Define la descripción del contenido del documento a forma de resumen. Su uso sería:

~~~html
<meta name=”description” content=”Manual Web que nos explica el uso del lenguaje HTML” />
~~~

#### Keywords

Conjunto de palabras que describen el documento. Las palabras van separadas por comas. Se escribiría de la siguiente forma:

~~~html
<meta name=”keywords” content=”manual,html,elementos,atributos,ejemplos” />
~~~

#### Revised

Información relativa a cuándo el documento fue revisado por última vez. Se utilizará de la siguiente forma:

~~~html
<meta name=”revised” content=”24/03/2016” />
~~~


### Metadatos Cabeceras HTTP

Las cabeceras http suelen ser establecidas en el servidor, si bien podemos modificarlas en el cliente mediante las meta-tags. El navegador realizará alguna acción al interpretar estas cabeceras. Por ejemplo podemos decirle al navegador cada cuanto tiempo tiene que recargar la página, o durante cuánto tiempo debe de cachear la página.

Estos metadatos se apoyan en el **atributo http-equiv**.

#### Refresh

Especifica cada cuanto tiempo tiene que recargar la página el navegador web. El tiempo es en segundos.

~~~html
<meta http-equiv=”refresh” content=”5” />
~~~

Incluso podemos utilizar este tipo para hacer una redirección a otra página.

~~~html
<meta http-equiv="refresh" content="2; http://lineadecodigo.com" />
~~~


#### Content-type

Nos sirve para identificar el tipo de documento, que será un documento de tipo text/html y la codificación del contenido. Si es ISO 8859-1, UTF-8,... Esto servirá al navegador a interpretar los caracteres que vayan dentro del contenido.

~~~html
<meta http-equiv="content-type" content="text/html; charset=UTF-8" />
~~~

#### Cookie

Nos sirve para guardar una cookie. Los datos guardados son clave/valor

~~~html
<meta http-equiv="cookie" content="clave=valor; expires=Saturday, 25-Mar-16 23:59:59 GMT;"" />
~~~

### Metadatos y el Open Graph Protocol

Como hemos comentado anteriormente la especificación HTML 4.01 no habla de un perfil de metadatos. Es por ello que hay diferentes perfiles que están proliferando diferentes perfiles que nos permiten metadatar el documento con algún fin. Uno de esos perfiles es el [Open Graph Protocol][4], este perfil es utilizado, entre otros, por Facebook para poder interpretar el documento de una forma más sencilla. Algunos de los metadatos que define el [Open Graph Protocol][4] son:

#### og:title

Define el título del documento.

<pre>&lt;meta name=”og:title” content=”Manual Web. Manuales en Español” /&gt;</pre>

#### og:type

Indica el tipo de objeto que representa la página. Si es un artículo, un vídeo, una imagen,...

<pre>&lt;meta name=”og:type” content=”article” /&gt;</pre>

#### og:image

Permite establecer la imagen más representativa del documento

<pre>&lt;meta name=”og:image” content=”http://www.manualweb.net/logo.png” /&gt;</pre>

#### og:url

Nos ayuda a definir la URL asociada al documento. Esto es por si queremos utilizar alguna diferente a la URL que ya tenga.

<pre>&lt;meta name=”og:url” content=”http://www.manualweb.net” /&gt;</pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:META
 [3]: http://www.metatags.org/dublin_core_metadata_element_set
 [4]: http://ogp.me/
