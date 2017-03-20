---
ID: 1024
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

Ahora que ya hemos aprendido a instalar el Framework [Flask][1] y como crear un primer programa, vamos a entrar en detalle a ver qué capacidades nos da el Framework [Flask][1] para crear rutas.

### Rutas Flask
¿Qué son realmente las rutas [Flask][1]? Las rutas [Flask][1] son los diferentes path en los que atenderá la aplicación, desde el path raíz <samp>'/'</samp> a cualquier concatenacion de path que se nos pueda ocurrir: <samp>'/saludo/'</samp>, <samp>'/saludo/es/'</samp>,...

Para definir una ruta en [Flask][1] deberemos de utilizar un decordador que utilice el método <code>.route()</code>, el método <code>.route()</code> recibirá como parámetro el path sobre el que queremos construir la ruta.

<pre lang='python'>
@app.route('/')
def principal():
  return 'Página Principal'
</pre>

El decorador con el método <code>.route()</code> se lo asignamos a un método. Este método será el encargado de procesar las peticiones que lleguen a dicha ruta. El retorno del método podrá ser un contenido, ya sea un texto plano, un texto en formato [HTML][3], JSON,...

En el ejemplo del código hemos puesto que devuelva texto plano. Pero podríamos haber escrito lo siguiene:

<pre lang='python'>
@app.route('/')
def principal():
  return '<html><body><h1>Hola!!!</h1></body></html>'
</pre>

Con lo que respecta a la ruta, podemos poner tantas subcarpetas como queramos, ya sea una anidación:

<pre lang='python'>
@app.route('/saludo')
def saludo():
  return 'Hola'
</pre>

O dos:

<pre lang='python'>
@app.route('/saludo/en')
def saludo_en():
  return 'Hello'
</pre>

O las que necesitemos.

### Rutas Flask con Variables
Cuando estemos definiendo rutas podemos poner que nos lleguen valores variables, las cuales podemos utilizar dentro del código para evaluarlas. Las variables se definen encerradas entre los símbolos menor < y mayor > con la siguiente estructura:

<pre lang='python'>
@app.route('/saludo/<nombre>')
def saludo(nombre):
  return 'Hola ' + nombre
</pre>


### URLs de las Rutas Flask


### Metodos HTTP



[1]: http://www.manualweb.net/tutorial-flask/
[2]: http://www.manualweb.net/tutorial-python/
[3]: http://www.manualweb.net/tutorial-html/
