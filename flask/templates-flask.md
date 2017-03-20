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

```html
<!doctype html>
<html>
<head><title>Template desde Flask</title></head>
<body>
  Hola!!!!
</body></html>
```

### Variables en una Template
Si bien definir una Template sin variables no tiene mucho sentido y sería más un fichero estático que una template.

Para definir variables dentro de una template en [Flask][1] encerraremos estas entre dobles llaves.

<code>{{ variable }}</code>

Cuando invoquemos al template deberemos de pasar el valor para la variable. De esta forma la template se rellenará y mostrará con dicho contenido.

De esta forma, si avanzamos nuestra template tendremos lo siguiente:

```html
<!doctype html>
<html>
<head><title>Template desde Flask</title></head>
<body>
  Hola {{ nombre }}!!!!
</body></html>
```

Así podremos tener una plantilla que salude a una persona u otra dependiendo del valor que se le pase por parámetro.

### Invocando una Template
A la hora de invocar a una template en [Flask][1] tenémos el método <code>.render_template()</code>. A este método pasaremos el nombre de la plantilla y los valores para sus atributos.

<pre lang="python">.render_template('plantilla', vble1=valor1, vble2=valor2,..., vbleN=valorN)</pre>

Para invocar a nuestra plantilla utilizaremos el siguiente código:

<pre lang="python">@app.route('/saludo/<nombre>')
def saludo(nombre):
 return render_template('saludo.html',nombre=nombre)</pre>

### Decisiones en Templates

Dentro de las templates no solo podemos insertar variables, si no que, por ejemplo, podemos realizar tomas de decisión.

Para ello contamos con la estructura <code>if-else</code> la cual nos permite evaluar el conteido de una variable y actuar en consecuencia.

La estructura para la sentencia <code>if-else</code> es

```html
<% if variable %>
  <!-- Código HTML -->
<%e else %>
  <!-- Código HTML -->
<% end if %>  
```

Si lo aplicamos a nuestro ejemplo podemos comprobar si llega contenido en la variable nombre, ya que si no hay contenido, se realizará un saludo estándar.

Así la template quedará de la siguiente manera:

```html
<!doctype html>
<html>
<head><title>Template desde Flask</title></head>
<body>
  <% if nombre %>
    Hola {{ nombre }}!!!!
  <% else %>
    Hola!!!!
  <% end if %>
</body></html>
```

### Template con Listas


### Uso de Request, Sessiomn y g en Templates

### Uso de get_flashed_messages() en Plantillas

### Herencia de Plantillas
Nos permite mantener elementos iguales a lo largo de diferentes plantillas, como podría ser la cabecera, pie de página, lateral,....


> Un ejemplo podría ser el uso de caracteres no escapados en plantillas flask


[1]: http://www.manualweb.net/tutorial-flask/
[2]: http://www.manualweb.net/tutorial-python/
[3]: http://www.manualweb.net/tutorial-html/
[4]: http://www.manualweb.net/tutorial-javascript/
[5]: http://www.manualweb.net/tutorial-css/
