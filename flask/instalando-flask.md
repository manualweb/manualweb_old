---
ID: 1020
post_title: '02 - Instalar el Framework Flask'
post_date: 2016-12-11 13:32
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/instalar-framework-flask/
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

## Instalar el Framework Flask

### Requisitos para utilizar el Framework Flask
[Flask][1] depende de librerías externas como **Werkzeug** y **Jinja2**. **Werkzeug** es un toolkit para aplicaciones WSGI, que es un interface entre aplicaciones Python y servidores web. **Jinja2** es un engine para el renderizado de plantillas (o templates) web.

Para poder utilizar [Flask][1] debes de tener, al menos, Python 2.6 instalado. [Flask][1] también funciona con Python 3.


### Realizando la instalación
Para instalar [Flask][1] vamos a utilizar <code>pip</code>. Así que simplemente deberemos de escribir en nuestra línea de comandos lo siguiente:

<kbd>$ pip install Flask</kbd>

Puede ser que para la instalación necesites ser administrador. En ese caso ejecuta:

<kbd>$ sudo pip install Flask</kbd>

### Flask con virtualenv
Una buena práctica dentro del mundo Python es ejecutar el código dentro de un entorno virtual o <code>virtualenv</code>. Dentro del entorno virtual podremos trabajar con diferentes versiones de Python y de las librerías que estemos utilizando.

Para instalar <code>virtualenv</code> deberás de ejecutar lo siguiente

<kbd>$ pip install virtualenv</kbd>

Una vez instalado <code>virtualenv</code> deberás de crear un directorio para tu proyecto.

<kbd>$ mkdir miproyecto
$ cd miproyecto</kbd>

Ahora creamos el entorno virtual del proyecto:

<kbd>$ virtualenv mientornovirtual</kbd>

> Se suele utilizar <code>venv</code> como nombre de los entornos virtuales

Ahora tenemos que saber hacer dos cosas. Por un lado activar el entorno virtual:

<kbd>$ . mientornovirtual/bin/activate</kbd>

Y desactivarlo una vez acabemos de utilizarlo

<kbd>$ deactivate</kbd>  


[1]: http://www.manualweb.net/tutorial-flask/
