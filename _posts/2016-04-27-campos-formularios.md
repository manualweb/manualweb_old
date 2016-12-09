---
ID: 864
post_title: '17.01 &#8211; Campos de Formularios'
author: Víctor Cuervo
post_date: 2016-04-27 12:00:59
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/campos-formularios/
published: true
nombreforo:
  - HTML
urlforo:
  - http://dudasprogramacion.com/html
urlmanual:
  - http://www.manualweb.net/tutorial-html/
urltest:
  - http://www.testprogramacion.com/html
urlcurso:
  - >
    http://www.aulaprogramacion.com/curso-html/
urlcharla:
  - >
    https://www.facebook.com/groups/html5.es/
urlvideo:
  - PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos:
  - >
    http://lineadecodigo.com/tag/html-form/feed/
---
Dentro de los campos de formularios que podemos incluir en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> encontramos los siguientes:
<ul>
	<li>Campos de entrada de datos
<ul>
	<li>Campos de textos</li>
	<li>Contraseñas</li>
	<li>Checkbox</li>
	<li>Radios</li>
	<li>Botones de envío</li>
	<li>Botones de borrado</li>
	<li>Ficheros</li>
	<li>Campos Ocultos</li>
	<li>Imágenes</li>
	<li>Botones</li>
</ul>
</li>
	<li>Áreas de texto</li>
	<li>Combos de selección</li>
</ul>

<h3><a name="input"></a>Campos de entrada de datos</h3>
Son los elementos básicos de un formulario ya que son los que nos permiten recuperar información del usuario de diferentes formas.

El elemento que representa los campos de entrada de datos es <a href="http://www.w3api.com/wiki/HTML:INPUT">input</a><b>.</b> La estructura básica de un campo de entrada es la siguiente:

<pre lang="html4strict"><input type=”tipo” id=”identificador” size=”tamaño” name=”nombre” value=”texto por defecto”/></pre>

Si vemos los atributos que tiene el elemento input nos encontramos los siguientes:
<ul>
	<li><b>type</b>, indica el tipo de campo de entrada de datos que vamos a utilizar. Dependiendo del tipo que indiquemos obtendremos un resultado u otro. Los valores que puede tener el atributo type son: “text”, “password”, “checkbox”, “radio”, “submit”, “reset”, “file”, “hidden”, “image” y “button”.</li>
	<li><b>id,</b> es el identificador del campo. Es importante ya que será el nombre por el cual podremos identificar, de forma unívoca, al campo.</li>
	<li><b>size</b>, será el tamaño del campo. Es decir, el número de caracteres que podríamos insertar en el campo de texto.</li>
	<li><b>name,</b> es el nombre del campo el cual se enviará desde el formulario al servidor.</li>
	<li><b>value,</b> será el valor por defecto que tendrá el campo de texto y que le aparecerá al usuario al cargar el formulario.</li>
</ul>

Cuando enviemos el formulario al servidor, se coge el la combinación name=value para ser enviada.

<h4><i>Campos de texto</i></h4>
El campo de texto, como bien indica su nombre, es el que nos permite insertar texto en un formulario. El usuario podrá insertar texto visible sobre el campo.

En este caso el tipo de elemento input que utilizaremos será “text”. Así, para definir un campo de texto lo haremos de la siguiente forma:

<pre lang="html4strict"><input type=”text” id=”identificador” size=”tamaño” name=”nombre” value=”texto por defecto”/></pre>

De esta forma si queremos crear un campo de texto para poder insertar 70 caracteres que contenga un email, lo definiremos de la siguiente forma:

<pre lang="html4strict"><input type=”text” id=”email” name=”email” size=”70” value=”usuario@dominio.com”/></pre>

<h4><i>Contraseñas</i></h4>
Cuando un usuario inserte una contraseña dentro de un formulario necesitaremos, casi seguro, que el valor de la contraseña no aparezca y que por el contrario aparezcan caracteres como asteriscos.

Para insertar un campo que acepte contraseñas dentro de un formulario vamos a utilizar un tipo “password” dentro del elemento input.

<pre lang="html4strict"><input type=”password” id=”identificador” size=”tamaño” name=”nombre”/></pre>

En este caso, aunque podemos poner un valor por defecto, si bien, no parece tener mucho sentido. Si queremos definir un campo que acepte contraseñas de 20 caracteres lo codificaremos de la siguiente forma:

<pre lang="html4strict"><input type=”password” id=”clave” name=”clave” size=”20”/></pre>

<h4><i>Checkbox</i></h4>
Un checkbox nos permite capturar un dato del usuario mediante un elemento de check. El check puede tener dos valores, seleccionado o no seleccionado. El tipo del elemento input que utilizaremos será “checkbox”. Así lo definiremos de la siguiente forma:

<pre lang="html4strict"><input type=”checkbox” id=”identificador” name=”nombre”/></pre>

En el caso del checkbox no tienen sentido el atributo tamaño ni el valor por defecto. Ya que, recordemos que solo podemos tener el check seleccionado o no. Pero lo que sí podemos hacer es generar un checkbox que esta preseleccionado. Para ello utilizamos el <a href="http://www.w3api.com/wiki/HTML:INPUT.checked">atributo checked</a><b>.</b>

<pre lang="html4strict"><input type=”checkbox” id=”identificador” name=”nombre” checked=”checked”/></pre>

Pero ¿dónde está el texto que acompaña al checkbox? Realmente el checkbox no tiene definido que acompañe al checkbox. Si no que hay que añadir el texto directamente al lado del checkbox.

<pre lang="html4strict"><input type=”checkbox” id=”identificador” name=”nombre” checked=”checked”/>
Texto del checkbox</pre>

Aunque más adelante vamos a ver una forma más correcta de asociar el texto al checkbox.

Así, si queremos crear un checkbox que nos pregunte si estamos de acuerdo con unas condiciones podríamos codificarlo de la siguiente forma:

<pre lang="html4strict"><input type=”checkbox” id=”condiciones” name=”condiciones”/>
Está de acuerdo con las condiciones explicadas más arriba.</pre>

Los checkbox suelen ir en grupos para seleccionar varias opciones. Por ejemplo podríamos tener el siguiente código con el que podamos seleccionar qué lenguaje de programación queremos aprender.

<pre lang="html4strict"><input type="checkbox" name="lenguaje" value="html">HTML
<input type="checkbox" name="lenguaje" value="javascript">Javascript
<input type="checkbox" name="lenguaje" value="css">CSS
<input type="checkbox" name="lenguaje" value="xml">XML</pre>

<h4><i>Radios</i></h4>
Con los elementos de radio podemos ofrecer un conjunto de opciones al usuario de tal manera que solo pueda elegir una de ellas. El tipo de elemento input que utilizamos es “radio”.

La sintaxis que seguiremos en los elementos input de tipo radio será la siguiente:

<pre lang="html4strict"><input type=”radio” id=”identificador” value=”valor” name=”nombre”/></pre>

En el caso de los elementos radio <b>toma un papel principal el </b><a href="http://www.w3api.com/wiki/HTML:Name"><b>atributo name</b></a>. Ya que para poder agrupar opciones deberemos de tener el mismo valor de <a href="http://www.w3api.com/wiki/HTML:Name">atributo name</a>.

Así, si queremos crear un grupo de radios para que nos elija una edad le podremos crear de la siguiente forma:

<pre lang="html4strict"><input type=”radio” id=”menos18” value=”menos18” name=”edad”/>Menos de 18
<input type=”radio” id=”18a30” value=”18a30” name=”edad”/>18 a 30
<input type=”radio” id=”31a50” value=”31a50” name=”edad”/>31 a 50
<input type=”radio” id=”mas50” value=”mas50” name=”edad”/>Más de 50</pre>

Al igual que sucedía con los campos de entrada de tipo check, podemos cargar campos de tipo radio en nuestro formulario con un elemento preseleccionado. Para ello volvemos a recurrir al <a href="http://www.w3api.com/wiki/HTML:INPUT.checked">atributo checked</a>.

<pre lang="html4strict"><input type=”radio” id=”identificador” value=”valor” name=”nombre” checked=”checked”/></pre>

<h4><i>Ficheros</i></h4>
Cuando diseñemos un formulario es posible que necesitemos enviar un fichero de datos al servidor. En este caso el campo de entrada de datos nos tiene que dar la posibilidad de acceder al sistema de fichero del dispositivo para poder seleccionar uno.

En este caso vamos a necesitar un campo de entrada de tipo “file”. La sintaxis de los campos de entrada para tipos file sería:

<pre lang="html4strict"><input type=”file” id=”identificador” value=”valor” name=”nombre”/></pre>

<h4><i>Campos Ocultos</i></h4>
Otra de las opciones que nos podemos encontrar dentro de los formularios es con la necesidad de enviar información oculta. Es decir, información que tiene que ir anexa al formulario pero que no necesita ser introducida por el usuario. Para ello tenemos la posibilidad de crear campos de datos ocultos.

La sintaxis para los campos de entrada ocultos es:

<pre lang="html4strict"><input type=”hidden” id=”identificador” value=”valor” name=”nombre”/></pre>

En estos casos el campo valor siempre va relleno, ya que no hay otra forma de que el usuario le asigne un valor.

<h4><i>Imágenes</i></h4>
Uno de los tipos de <a href="http://www.w3api.com/wiki/HTML:INPUT">elementos input</a> es el tipo <i>“image”</i>. Mediante el tipo <i>“image”</i> podemos crear un botón de envío que sea una imágen. La imagen se cargará mediante el <a href="http://www.w3api.com/wiki/HTML:Src">atributo src</a>. La estructura para <a href="http://www.w3api.com/wiki/HTML:INPUT">elementos input</a> de este tipo es:

<pre lang="html4strict"><input type=”image” src=”url-image” name=”nombre” alt=”texto-alternativo”/></pre>

Como sucede cada vez que manipulamos imágenes hay que rellenar el <a href="http://www.w3api.com/wiki/HTML:Alt">atributo alt</a> con un texto alternativo por motivos de accesibilidad.

Cuando pulsemos sobre la imagen se enviará el formulario, además se enviarán dos atributos <i>name.x</i> y <i>name.y</i> con los datos de las coordenadas x,y en las que se pulsó sobre la imagen.

<h3><a name="textarea"></a>Áreas de texto</h3>
Un elemento algo más avanzado que el campo de entrada de datos es el área de texto. Mediante un área de texto tenemos la capacidad de que el usuario inserte una gran cantidad de datos y además que esos datos puedan estar en diferentes líneas.

Para poder insertar un área de texto en nuestro formulario utilizamos el <a href="http://www.w3api.com/wiki/HTML:TEXTAREA">elemento textarea</a>. La sintaxis del <a href="http://www.w3api.com/wiki/HTML:TEXTAREA">elemento textarea</a> será la siguiente:

<pre lang="html4strict"><textarea rows=”numerofilas” cols=”numerocolumnas” name=”nombre”></textarea></pre>

A diferencia del <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a>, el textarea tiene una etiqueta de inicio y una de fin.

Los atributos que nos encontramos en un <a href="http://www.w3api.com/wiki/HTML:TEXTAREA">textarea</a> son:
<ul>
	<li><b><a href="http://www.w3api.com/wiki/HTML:TEXTAREA.rows"><b>rows</b></a><b>, </b></b>indica el número de filas que tiene el área de texto.</li>
</ul>
<ul>
	<li><a href="http://www.w3api.com/wiki/HTML:TEXTAREA.cols"><b>cols</b></a><b>,</b> indica el número de columnas que tiene el área de texto.</li>
</ul>
<ul>
	<li><a href="http://www.w3api.com/wiki/HTML:Name"><b>name</b></a><b>,</b> al igual que sucede con otros elementos del formulario, name contiene el nombre del campo, el cual será enviado al servidor para ser procesado.</li>
</ul>
De esta forma, si queremos crear un área de texto de 20 filas por 100 columnas en el que un usuario pueda insertar un comentario tendríamos el siguiente código:

<pre lang="html4strict"><textarea rows=”20” cols=”100” name=”comentario”></textarea></pre>

Si queremos que el área de texto vaya con un valor por defecto, tendremos que añadir dicho contenido entre las etiquetas de textarea.

<pre lang="html4strict"><textarea rows=”20” cols=”100” name=”comentario”>Contenido de comentario...</textarea></pre>

<h3><a name="select"></a>Combos de opciones</h3>
Otro elemento que podemos insertar dentro de un formulario es un combo de opciones. Es decir, un elemento en el que el usuario pueda elegir un elemento o varios de una lista.

El elemento que nos permite insertar un combo de opciones es <a href="http://www.w3api.com/wiki/HTML:SELECT">select</a>. La sintaxis básica de un <a href="http://www.w3api.com/wiki/HTML:SELECT">elemento select</a> es:

<pre lang="html4strict"><select name=”nombre” size=”valoresvisibles” multiple=”multiple”></select></pre>

De los valores que nos encontramos en el <a href="http://www.w3api.com/wiki/HTML:SELECT">elemento select</a> destacamos:
<ul>
	<li><b>name,</b> que al igual que en anteriores casos sirve para dar un nombre al campo que se enviará al servidor.</li>
	<li><b>size,</b> indica el número de opciones que aparecen visibles por defecto. En el caso de que haya más opciones que las elegidas por defecto lo que nos aparecerá será un scroll para poder localizar todas.</li>
	<li><b>multiple</b>, este atributo nos servirá para poder elegir varias de las opciones. Es decir, para tener una elección múltiple.</li>
</ul>
Como hemos visto el elemento select sólo demarca el combo de las opciones. Para definir cada una de las opciones tenemos el <a href="http://www.w3api.com/wiki/HTML:OPTION">elemento option</a>.

La sintaxis básica del <a href="http://www.w3api.com/wiki/HTML:OPTION">elemento option</a> es la siguiente:

<pre lang="html4strict"><option label=”etiqueta” value=”valor”></option></pre>

Dónde el <b>atributo label</b> indica el texto que aparecerá para poder ser seleccionado en el combo y <b>value</b> el valor realmente de ese item. En el caso de que no pongamos el atributo label o el atributo value, el valor que cogerán dichos atributos será el texto que encontremos entre los <a href="http://www.w3api.com/wiki/HTML:OPTION">elementos de option</a><b>.</b>

Por lo tanto, si juntamos la sintaxis del <a href="http://www.w3api.com/wiki/HTML:SELECT">elemento select</a> y el <a href="http://www.w3api.com/wiki/HTML:OPTION">elemento option</a> tenemos la siguiente codificación:

<pre lang="html4strict"><select name=”nombre” size=”valoresvisibles” multiple=”multiple”>
  <option label=”etiqueta” value=”valor”></option>
</select></pre>

Si queremos crear un combo de opciones donde podamos elegir un equipo de fútbol tendríamos el siguiente código:

<pre lang="html4strict"><select>
  <option>Atlético de Madrid</option>
  <option>Real Betis</option>
  <option>FC. Barcelona</option>
  <option>Real Madrid</option>
  <option>Zaragoza</option>
</select></pre>

Si queremos que una de las opciones del combo vaya marcada recurriremos al <a href="http://www.w3api.com/wiki/HTML:Selected">atributo selected</a>. Así, en nuestro ejemplo si marcamos como predefinido el equipo del Betis tendríamos el siguiente código:

<pre lang="html4strict"><select>
  <option>Atletico de Madrid</option>
  <option selected=”selected”>Betis</option>
  <option>FC. Barcelona</option>
  <option>Real Madrid</option>
  <option>Zaragoza</option>
</select></pre>

Otra de las cosas que podemos realizar dentro de un combo es agrupar opciones. Si la lista de opciones es muy grande podemos utilizar el <a href="http://www.w3api.com/wiki/HTML:OPTGROUP">elemento optgroup</a>.

La sintaxis del <a href="http://www.w3api.com/wiki/HTML:OPTGROUP">elemento optgroup</a> es la siguiente:

<pre lang="html4strict"><optgroup label=”etiqueta”></optgroup></pre>

Dentro del <a href="http://www.w3api.com/wiki/HTML:OPTGROUP">elemento optgroup</a> encontraremos todos los <a href="http://www.w3api.com/wiki/HTML:OPTION">elementos option</a> que queramos agrupar.

Si por ejemplo, queremos ofrecer un combo de ciudades y las queremos agrupar por continentes, tendríamos el siguiente código:

<pre lang="html4strict"><select name=”ciudad”>
  <optgroup label="Europa">
    <option>Madrid</option>
    <option>Londres</option>
    <option>Paris</option>
  </optgroup>
  <optgroup label="Suramerica">
    <option>Santiago</option>
    <option>Sao Paulo</option>
    <option>Lima</option>
    <option>Bogota</option>
  </optgroup>
  <optgroup label="Africa">
    <option>Casablanca</option>
    <option>Ciudad del Cabo</option>
  </optgroup>
</select></pre>

<h3><a name="button"></a>Botones</h3>
Una vez que hemos insertado campos de texto en nuestro formulario es hora de insertar botones. <b><i>Mediante los botones podremos realizar operaciones de envío del formulario</i></b>, de manipulación de datos, borrado,...

Existen dos formas de insertar botones dentro de un formulario: el <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a> y el <a href="http://www.w3api.com/wiki/HTML:BUTTON">elemento button</a>. La primera es recurre nuevamente al <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a> que hemos visto anteriormente para los campos de texto.

La sintaxis para un botón mediante un <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a> será:

<pre lang="html4strict"><input type=”button” value=”TextoBotón”/></pre>

Si bien, este botón no hace nada por sí solo y tendríamos que darle un comportamiento vía Javascript para que el botón tuviera funcionalidad.
<h4><i>Botones de envío</i></h4>
En el caso del <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a> podemos poner botones de otras dos formas y en estos casos ya con funcionalidad. Estos son los tipos <b><i>“submit”</i></b> y <b><i>“reset”.</i></b>

Para crear un botón que nos envíe los datos del formulario al servidor tenemos el tipo submit. Su sintaxis es la siguiente:

<pre lang="html4strict"><input type=”submit” value=”TextoBotón”/></pre>

Una vez que pulsemos sobre el botón se enviarán los datos que el usuario haya insertado en el formulario.

<h4><i>Botones de borrado</i></h4>
El otro tipo de botón con funcionalidad es el que nos permite el borrado de los datos del formulario. Para ello tenemos el tipo “reset”. La sintaxis de este botón será:

<pre lang="html4strict"><input type=”reset” value=”TextoBotón”/></pre>

Cuando el usuario pulse sobre el botón de borrado. Todos los valores que el usuario haya insertado en el formulario se eliminarán.

<h4><i>El elemento button</i></h4>
Como hemos visto hasta ahora los botones que hemos insertado han sido mediante el <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a>, si bien contamos con otro elemento para poner botones en el formulario que es el <a href="http://www.w3api.com/wiki/HTML:BUTTON">elemento button</a>. Cuya funcionalidad es la misma que la del <a href="http://www.w3api.com/wiki/HTML:INPUT">elemento input</a>.

La sintaxis del <a href="http://www.w3api.com/wiki/HTML:BUTTON">elemento button</a> es:

<pre lang="html4strict"><button name=”nombre” type=”TipoBoton” value=”ValorBoton”></button></pre>

Dependiendo del tipo que asignamos al <a href="http://www.w3api.com/wiki/HTML:Type">atributo type</a> obtendremos un comportamiento u otro:
<ul>
	<li><b>submit</b>, crea un botón para el envío de formulario.</li>
	<li><b>reset</b>, crea un botón para el borrado de datos del formulario.</li>
	<li><b>button</b>, crea un botón normal.</li>
</ul>