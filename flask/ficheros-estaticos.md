---
ID: 1026
post_title: '04 - Rutas Flask'
post_date: 2016-12-19 00:58
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/flask/rutas-flask/
published: false
nombreforo: Flask
urlforo: http://www.dudasprogramacion.com/python/
urlejemplos: http://lineadecodigo.com/tag/python-flask/feed/
urlvideo:
urlmanual: http://www.manualweb.net/tutorial-flask/
urlcharla:
urltest: http://www.testprogramacion.com/flask/
urlcurso: http://www.aulaprogramacion.com/flask/
---

[Flaskj][1] a parte de gestionar las rutas de la aplicación, nos ofrece un servicio para gestionar ficheros estáticos. Ya que no todo lo que tengamos en la aplicación web serán rspuestas dinámicas de rutas.

En la parte de ficheros estáticos de [Flask][1] encontramos las imágenes, ficheros [HTML][3], código [Javascript][4], hojas de estilo [CSS][5],...

Por convención encontramos el contenido estático de [Flask][1] el la carpeta

<samp>/static</samp>

Si querémos acceder al contenido estático desde código en [Flask][1], es decir, a la URL que representan, podemos utilizar el método <code>.url_for()</code>

Así podremos acceder al contenido de un fichero con el siguiente código:

<pre lang="python">
url_for("static", filename="main.css")
</pre>



[1]: http://www.manualweb.net/tutorial-flask/
[2]: http://www.manualweb.net/tutorial-python/
[3]: http://www.manualweb.net/tutorial-html/
[4]: http://www.manualweb.net/tutorial-javascript/
[5]: http://www.manualweb.net/tutorial-css/
