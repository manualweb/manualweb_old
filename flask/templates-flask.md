---
ID: 1028
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

Cuando estamos creando rutas con [Flaks][1] no es necesario que generemos todo el código [HTML][3] de una forma dinámica dentro de los métodos de las rutas.

Una de las alternativas que tenemos para generar código es el renderizar un template de [Flaks][1].

Las templates son páginas [HTML][3] las cuales contienen variables que pueden ser sustituidas a la hora de invocarlas. Estas variables pueden ser elementos sueltos o bien pueden ser listas de elementos, los cuales iteraremos y mostraremos en el template.

### Definiendo una Template
Lo primero que tenemos que saber acerca de las templates es que se almancenan en el directorio

<samp>/templates</samp>

Las templates no dejan de ser ficheros .html. Así podríamos tener una primera template que sea saludo.html

<samp>/templates/saludo.html</samp>

Así podríamos tener una primera template que fuese la siguiente:

<pre lang="html4strict"><!doctype html>
<html>
<head><title>Template desde Flask</title></head>
<body>
  Hola!!!!
</body></html>
</pre>

### Variables en una Template

### Invocando una Template


### Template con Listas
