---
ID: 1357
post_title: 07 – Mi Primera Página HTML
author: Víctor Cuervo
post_date: 2017-04-11 23:55:50
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/mi-primera-pagina-html/
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
Con lo que ya llevamos aprendido en el [Manual de HTML][1] es un buen momento para crear nuestra primera página [HTML][1] o mejor dicho, nuestra primera página web.

### Herramientas básicas

Lo primero que vamos a necesitar es un editor de texto instalado en tu ordenador. Ya hemos visto que nos pueden valer el [UltraEdit][2], [NoteTab][3], el TextEdit de Mac, o un avanzado editor como [Sublime Text][4] o [Atom][5]. Dentro del editor de texto crea un documento de texto el cual llamaremos

<kbd>miprimeraweb.html</kbd>

Es importante saber que los documentos [HTML][1] tienen la **extensión .html o .htm**. Es más común la primera de ellas.

### Crear la página HTML

Una vez tengamos nuestro documento de texto vamos a crear la estructura del documento [HTML][1], con sus elementos [html][6], [head][7] y [body][8].

~~~html
<! doctype html>
<html>
<head>
  <title>Mi Primera Página</title>
  <meta charset=”utf-8”/>
</head>
<body>
  <h1>Mi Primera Página</h1>
  Mi primera página en HTML.
</body>
</html>
~~~


Vemos que dentro del [elemento body][8] hemos insertado un [elemento h1][9] con un texto y directamente texto que indica *“Esta es mi primera página web”*.

No te preocupes por los [elementos meta][10] y [h1][9] que aparecen nuevos, ya que los veremos en detalle más adelante.

### Visualizar la página HTML

Una vez guardada la página [HTML][1] vamos a visualizarla. Para poder visualizarla necesitamos un navegador web. Lo más normal es que tu ordenador ya venga con alguno instalado por defecto, si no puedes instalarte alguno como [Google Chrome][11], [Mozilla Firefox][12] u [Opera][13].


Una vez arrancado el navegador web simplemente tiene que abrir la página creada anteriormente, es decir, el archivo **miprimeraweb.html**

Verás que el navegador carga algo parecido a lo siguiente:

![Mi primera página web](https://github.com/manualweb/manualweb/raw/master/html/images/mi-primera-pagina-web.png "Mi primera página web")

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.idmcomp.com/
 [3]: http://www.notetab.com/
 [4]: http://www.sublimetext.com/
 [5]: https://atom.io/
 [6]: http://www.w3api.com/wiki/HTML:HTML
 [7]: http://www.w3api.com/wiki/HTML:HEAD
 [8]: http://www.w3api.com/wiki/HTML:BODY
 [9]: http://www.w3api.com/wiki/HTML:H1
 [10]: http://www.w3api.com/wiki/HTML:META
 [11]: https://www.google.com/chrome/browser/desktop/index.html
 [12]: https://www.mozilla.org/es-ES/firefox/new/
 [13]: http://www.opera.com/
