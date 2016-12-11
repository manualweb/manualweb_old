---
ID: 1018
post_title: Tutorial Flask
post_date: 2016-12-11 13:32
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/tutorial-flask/
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
### Introducción al Framework Flask

Flask es un Microframework de Python que está basado en Werkzeug, Jinja 2 y buenas intenciones. Mediante [Flask][1] podemos construir aplicaciones web y servicios Restful con Python de una forma extraordinariamente sencilla. Con pocas líneas podemos llegar a tener un servicio Restful funcionando.

La mayor virtud de [Flask][1] es poder crear rutas web de una forma muy sencilla. Una pequeña aplicación web que nos devolviese un hola mundo sería tan sencilla como escribir:

```python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "¡Hola Mundo!"

if __name__ == "__main__":
    app.run()
```

Y crear un servicio que devolviese un JSON con [Flask][1] lo podríamos hacer con el siguiente código:

```python
...
```

### Características de Flask


[1]: http://www.manualweb.net/tutorial-flask/
