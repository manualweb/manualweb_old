---
ID: 1030
post_title: '0x - Request Flask'
post_date: 2017-01-03 20:28
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/flask/request-flask/
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

El contenido que un cliente web manda al servidor siempre va almacenado en la Request. En [Flask][1] la Request se representa mediante el objeto <code>request</code>

Para poder utilizar el objeto <code>request</code> deberemos de importarlo al principio de nuestro programa [Flask][1]

<pre lang="python">from flask import request</pre>

### Tipo de Request
Una de las primeras cosas para las que podemos utilizar el objeto <code>request</code> es la de saber el tipo de petición que nos hace el cliente: GET, POST, DELETE,... para ello el objeto <code>request</code> nos ofrece el atributo <code>.method</code>

Así podremos preguntar lo siguiente:

<pre lang="python">if request.method == 'POST':</pre>

### Acceso a Parámetros
El objeto <code>request</code> nos servirá para acceder a la información que nos envíe el cliente. La principal información que nos envía son los parámetros, ya sean parámetros tipo GET o parámeteos tipo POST.

#### Acceso a Parámetros GET
Para accerder a un parámetro de tipo GET, que son aquellos que vienen como una lista de claves/valor dentro de la URL de petición.

<samp>?parametro1=valor1&parametro2=valor2&...&parametroN=valorN</samp>

El objeto <code>request</code> nos ofrece la colección <code>.args</code> y el método <code>.get()</code> para poder acceder a parámetros de tipo GET.

El método <code>.get()</code> recibe como parámetro el nombre del parámetro que queremos recuperar, lo que sería la clave.

La estructura sería:

<pre lang="python">response.args.get('clave','')</pre>

Si nos invocan mediante un método GET con la cadena:

<samp>?nombre=Victor</samp>

Podremos acceder a dicho parámetro de la siguiente forma:

<pre lang="python">nombre = request.args.get('nombre','')</pre>

#### Acceso a Parámetros POST





[1]: http://www.manualweb.net/tutorial-flask/
[2]: http://www.manualweb.net/tutorial-python/
[3]: http://www.manualweb.net/tutorial-html/
[4]: http://www.manualweb.net/tutorial-javascript/
[5]: http://www.manualweb.net/tutorial-css/
