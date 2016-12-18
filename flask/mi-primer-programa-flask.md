---
ID: 1022
post_title: '03 - Mi primer programa Flask'
post_date: 2016-12-12 00:02
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/flask/mi-primer-programa-flask/
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
## Mi primer programa Flask
Ahora que ya conocemos los aspectos básicos sobre qué es [Flask][1] vamos a realizar el primer programa [Flask][1].

Lo primero que necesitamos es un editor de texto, aquel con el que te encuentres más a gusto, ya sea un completo **Pycharm** o un editor configurable como **Atom**.

### Importar Flask
Al ser un programa [Python][2] la extensión de nuestro fichero será .py. Lo primero que haremos en el programa será importar el Framework [Flask][1], en concreto vamos a importar el objeto <code>Flask</code> que es el objeteo principal del Framework.

<pre lang="python">
from flask import Flask
</pre>

<p class="example">Hola</pre>

Ahora vamos a crear una aplicación [Flask][1], para ello instanciamos el objeto <code>Flask</code>

```python
app = Flask(__name__)
```

Ya tenemos la aplicación que será la que tendremos que ejecutar al final del programa.

### Definir las Rutas
El concepto principal que maneja Flask es el de las rutas. Por entendernos la ruta será un path del servidor. Lo que vamos a hacer es asociar un Path a una funcionalidad, esto lo conseguimos con las rutas.

Para definir una ruta utilizamos el método <code>.route()</code>, el cual recibirá entre paréntesis el path sobre el que queremos asociar la fucionalidad.

Así, si quereos gestionar el path o ruta raíz escribiremos lo siguiente:

```python
@app.route('/')
```

Si lo que queremos es controlar el path o ruta <samp>/mensaje/saludo</samp> cambiaremos el parámetro del método:

```python
@app.route('/mensaje/saludo')
```
Ahora asociamos a esa ruta un método, este será el que se encargue de controlar las peticiones o <code>Request</code> que lleguen a la ruta y de devolver el contenido mediante una <code>Response</code>.

```python
@app.route('/')
def saludo():
    return 'Mi primer programa Flask!'
```

En este caso hemos asociado el método <code>.saludo()</code> a la ruta y lo que hacemos es devolver una simple cadena <samp>'Mi primer programa Flask!'</samp>

### Ejecutar la aplicación Flask


[1]: http://www.manualweb.net/tutorial-flask/
[2]: http://www.manualweb.net/tutorial-python/
