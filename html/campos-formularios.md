---
ID: pdte
post_title: '17.01 &#8211; Campos de Formularios'
author: Víctor Cuervo
post_date: 2016-04-27 12:00:59
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/campos-formularios/
published: false
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-form/feed/
gitfolder: html
---
Dentro de los campos de formularios que podemos incluir en [HTML][1] encontramos los siguientes:
*   Campos de entrada de datos
    *   Campos de textos
    *   Contraseñas
    *   Checkbox
    *   Radios
    *   Botones de envío
    *   Botones de borrado
    *   Ficheros
    *   Campos Ocultos
    *   Imágenes
    *   Botones
*   Áreas de texto
*   Combos de selección

### <a name="input"></a>Campos de entrada de datos Son los elementos básicos de un formulario ya que son los que nos permiten recuperar información del usuario de diferentes formas. El elemento que representa los campos de entrada de datos es

[input][2]**.** La estructura básica de un campo de entrada es la siguiente: <pre lang="html4strict">&lt;input type=”tipo” id=”identificador” size=”tamaño” name=”nombre” value=”texto por defecto”/></pre> Si vemos los atributos que tiene el elemento input nos encontramos los siguientes:

*   **type**, indica el tipo de campo de entrada de datos que vamos a utilizar. Dependiendo del tipo que indiquemos obtendremos un resultado u otro. Los valores que puede tener el atributo type son: “text”, “password”, “checkbox”, “radio”, “submit”, “reset”, “file”, “hidden”, “image” y “button”.
*   **id,** es el identificador del campo. Es importante ya que será el nombre por el cual podremos identificar, de forma unívoca, al campo.
*   **size**, será el tamaño del campo. Es decir, el número de caracteres que podríamos insertar en el campo de texto.
*   **name,** es el nombre del campo el cual se enviará desde el formulario al servidor.
*   **value,** será el valor por defecto que tendrá el campo de texto y que le aparecerá al usuario al cargar el formulario. Cuando enviemos el formulario al servidor, se coge el la combinación name=value para ser enviada.

#### *Campos de texto* El campo de texto, como bien indica su nombre, es el que nos permite insertar texto en un formulario. El usuario podrá insertar texto visible sobre el campo. En este caso el tipo de elemento input que utilizaremos será “text”. Así, para definir un campo de texto lo haremos de la siguiente forma:

<pre lang="html4strict">&lt;input type=”text” id=”identificador” size=”tamaño” name=”nombre” value=”texto por defecto”/></pre> De esta forma si queremos crear un campo de texto para poder insertar 70 caracteres que contenga un email, lo definiremos de la siguiente forma:

<pre lang="html4strict">&lt;input type=”text” id=”email” name=”email” size=”70” value=”usuario@dominio.com”/></pre>

#### *Contraseñas* Cuando un usuario inserte una contraseña dentro de un formulario necesitaremos, casi seguro, que el valor de la contraseña no aparezca y que por el contrario aparezcan caracteres como asteriscos. Para insertar un campo que acepte contraseñas dentro de un formulario vamos a utilizar un tipo “password” dentro del elemento input.

<pre lang="html4strict">&lt;input type=”password” id=”identificador” size=”tamaño” name=”nombre”/></pre> En este caso, aunque podemos poner un valor por defecto, si bien, no parece tener mucho sentido. Si queremos definir un campo que acepte contraseñas de 20 caracteres lo codificaremos de la siguiente forma:

<pre lang="html4strict">&lt;input type=”password” id=”clave” name=”clave” size=”20”/></pre>

#### *Checkbox* Un checkbox nos permite capturar un dato del usuario mediante un elemento de check. El check puede tener dos valores, seleccionado o no seleccionado. El tipo del elemento input que utilizaremos será “checkbox”. Así lo definiremos de la siguiente forma:

<pre lang="html4strict">&lt;input type=”checkbox” id=”identificador” name=”nombre”/></pre> En el caso del checkbox no tienen sentido el atributo tamaño ni el valor por defecto. Ya que, recordemos que solo podemos tener el check seleccionado o no. Pero lo que sí podemos hacer es generar un checkbox que esta preseleccionado. Para ello utilizamos el

[atributo checked][3]**.** <pre lang="html4strict">&lt;input type=”checkbox” id=”identificador” name=”nombre” checked=”checked”/></pre> Pero ¿dónde está el texto que acompaña al checkbox? Realmente el checkbox no tiene definido que acompañe al checkbox. Si no que hay que añadir el texto directamente al lado del checkbox.

<pre lang="html4strict">&lt;input type=”checkbox” id=”identificador” name=”nombre” checked=”checked”/>
Texto del checkbox</pre> Aunque más adelante vamos a ver una forma más correcta de asociar el texto al checkbox. Así, si queremos crear un checkbox que nos pregunte si estamos de acuerdo con unas condiciones podríamos codificarlo de la siguiente forma:

<pre lang="html4strict">&lt;input type=”checkbox” id=”condiciones” name=”condiciones”/>
Está de acuerdo con las condiciones explicadas más arriba.</pre> Los checkbox suelen ir en grupos para seleccionar varias opciones. Por ejemplo podríamos tener el siguiente código con el que podamos seleccionar qué lenguaje de programación queremos aprender.

<pre lang="html4strict"><input type="checkbox" name="lenguaje" value="html" />HTML
<input type="checkbox" name="lenguaje" value="javascript" />Javascript
<input type="checkbox" name="lenguaje" value="css" />CSS
<input type="checkbox" name="lenguaje" value="xml" />XML</pre>

#### *Radios* Con los elementos de radio podemos ofrecer un conjunto de opciones al usuario de tal manera que solo pueda elegir una de ellas. El tipo de elemento input que utilizamos es “radio”. La sintaxis que seguiremos en los elementos input de tipo radio será la siguiente:

<pre lang="html4strict">&lt;input type=”radio” id=”identificador” value=”valor” name=”nombre”/></pre> En el caso de los elementos radio

**toma un papel principal el **[**atributo name**][4]. Ya que para poder agrupar opciones deberemos de tener el mismo valor de [atributo name][4]. Así, si queremos crear un grupo de radios para que nos elija una edad le podremos crear de la siguiente forma: <pre lang="html4strict">&lt;input type=”radio” id=”menos18” value=”menos18” name=”edad”/>Menos de 18
&lt;input type=”radio” id=”18a30” value=”18a30” name=”edad”/>18 a 30
&lt;input type=”radio” id=”31a50” value=”31a50” name=”edad”/>31 a 50
&lt;input type=”radio” id=”mas50” value=”mas50” name=”edad”/>Más de 50</pre> Al igual que sucedía con los campos de entrada de tipo check, podemos cargar campos de tipo radio en nuestro formulario con un elemento preseleccionado. Para ello volvemos a recurrir al

[atributo checked][3]. <pre lang="html4strict">&lt;input type=”radio” id=”identificador” value=”valor” name=”nombre” checked=”checked”/></pre>

#### *Ficheros* Cuando diseñemos un formulario es posible que necesitemos enviar un fichero de datos al servidor. En este caso el campo de entrada de datos nos tiene que dar la posibilidad de acceder al sistema de fichero del dispositivo para poder seleccionar uno. En este caso vamos a necesitar un campo de entrada de tipo “file”. La sintaxis de los campos de entrada para tipos file sería:

<pre lang="html4strict">&lt;input type=”file” id=”identificador” value=”valor” name=”nombre”/></pre>

#### *Campos Ocultos* Otra de las opciones que nos podemos encontrar dentro de los formularios es con la necesidad de enviar información oculta. Es decir, información que tiene que ir anexa al formulario pero que no necesita ser introducida por el usuario. Para ello tenemos la posibilidad de crear campos de datos ocultos. La sintaxis para los campos de entrada ocultos es:

<pre lang="html4strict">&lt;input type=”hidden” id=”identificador” value=”valor” name=”nombre”/></pre> En estos casos el campo valor siempre va relleno, ya que no hay otra forma de que el usuario le asigne un valor.

#### *Imágenes* Uno de los tipos de

[elementos input][2] es el tipo *“image”*. Mediante el tipo *“image”* podemos crear un botón de envío que sea una imágen. La imagen se cargará mediante el [atributo src][5]. La estructura para [elementos input][2] de este tipo es: <pre lang="html4strict">&lt;input type=”image” src=”url-image” name=”nombre” alt=”texto-alternativo”/></pre> Como sucede cada vez que manipulamos imágenes hay que rellenar el

[atributo alt][6] con un texto alternativo por motivos de accesibilidad. Cuando pulsemos sobre la imagen se enviará el formulario, además se enviarán dos atributos *name.x* y *name.y* con los datos de las coordenadas x,y en las que se pulsó sobre la imagen.
### <a name="textarea"></a>Áreas de texto Un elemento algo más avanzado que el campo de entrada de datos es el área de texto. Mediante un área de texto tenemos la capacidad de que el usuario inserte una gran cantidad de datos y además que esos datos puedan estar en diferentes líneas. Para poder insertar un área de texto en nuestro formulario utilizamos el

[elemento textarea][7]. La sintaxis del [elemento textarea][7] será la siguiente: <pre lang="html4strict">&lt;textarea rows=”numerofilas” cols=”numerocolumnas” name=”nombre”>&lt;/textarea></pre> A diferencia del

[elemento input][2], el textarea tiene una etiqueta de inicio y una de fin. Los atributos que nos encontramos en un [textarea][7] son:
*   **[**rows**][8]**, ****indica el número de filas que tiene el área de texto.

*   [**cols**][9]**,** indica el número de columnas que tiene el área de texto.

*   [**name**][4]**,** al igual que sucede con otros elementos del formulario, name contiene el nombre del campo, el cual será enviado al servidor para ser procesado. De esta forma, si queremos crear un área de texto de 20 filas por 100 columnas en el que un usuario pueda insertar un comentario tendríamos el siguiente código:

<pre lang="html4strict">&lt;textarea rows=”20” cols=”100” name=”comentario”>&lt;/textarea></pre> Si queremos que el área de texto vaya con un valor por defecto, tendremos que añadir dicho contenido entre las etiquetas de textarea.

<pre lang="html4strict">&lt;textarea rows=”20” cols=”100” name=”comentario”>Contenido de comentario...&lt;/textarea></pre>

### <a name="select"></a>Combos de opciones Otro elemento que podemos insertar dentro de un formulario es un combo de opciones. Es decir, un elemento en el que el usuario pueda elegir un elemento o varios de una lista. El elemento que nos permite insertar un combo de opciones es

[select][10]. La sintaxis básica de un [elemento select][10] es: <pre lang="html4strict">&lt;select name=”nombre” size=”valoresvisibles” multiple=”multiple”>&lt;/select></pre> De los valores que nos encontramos en el

[elemento select][10] destacamos:
*   **name,** que al igual que en anteriores casos sirve para dar un nombre al campo que se enviará al servidor.
*   **size,** indica el número de opciones que aparecen visibles por defecto. En el caso de que haya más opciones que las elegidas por defecto lo que nos aparecerá será un scroll para poder localizar todas.
*   **multiple**, este atributo nos servirá para poder elegir varias de las opciones. Es decir, para tener una elección múltiple. Como hemos visto el elemento select sólo demarca el combo de las opciones. Para definir cada una de las opciones tenemos el

[elemento option][11]. La sintaxis básica del [elemento option][11] es la siguiente: <pre lang="html4strict">&lt;option label=”etiqueta” value=”valor”>&lt;/option></pre> Dónde el

**atributo label** indica el texto que aparecerá para poder ser seleccionado en el combo y **value** el valor realmente de ese item. En el caso de que no pongamos el atributo label o el atributo value, el valor que cogerán dichos atributos será el texto que encontremos entre los [elementos de option][11]**.** Por lo tanto, si juntamos la sintaxis del [elemento select][10] y el [elemento option][11] tenemos la siguiente codificación: <pre lang="html4strict">&lt;select name=”nombre” size=”valoresvisibles” multiple=”multiple”>
  &lt;option label=”etiqueta” value=”valor”>&lt;/option>
&lt;/select></pre> Si queremos crear un combo de opciones donde podamos elegir un equipo de fútbol tendríamos el siguiente código:

<pre lang="html4strict"><select>
  &lt;option>Atlético de Madrid&lt;/option>
  &lt;option>Real Betis&lt;/option>
  &lt;option>FC. Barcelona&lt;/option>
  &lt;option>Real Madrid&lt;/option>
  &lt;option>Zaragoza&lt;/option>
</select></pre> Si queremos que una de las opciones del combo vaya marcada recurriremos al

[atributo selected][12]. Así, en nuestro ejemplo si marcamos como predefinido el equipo del Betis tendríamos el siguiente código: <pre lang="html4strict"><select>
  &lt;option>Atletico de Madrid&lt;/option>
  &lt;option selected=”selected”>Betis&lt;/option>
  &lt;option>FC. Barcelona&lt;/option>
  &lt;option>Real Madrid&lt;/option>
  &lt;option>Zaragoza&lt;/option>
</select></pre> Otra de las cosas que podemos realizar dentro de un combo es agrupar opciones. Si la lista de opciones es muy grande podemos utilizar el

[elemento optgroup][13]. La sintaxis del [elemento optgroup][13] es la siguiente: <pre lang="html4strict">&lt;optgroup label=”etiqueta”>&lt;/optgroup></pre> Dentro del

[elemento optgroup][13] encontraremos todos los [elementos option][11] que queramos agrupar. Si por ejemplo, queremos ofrecer un combo de ciudades y las queremos agrupar por continentes, tendríamos el siguiente código: <pre lang="html4strict">&lt;select name=”ciudad”>
  &lt;optgroup label="Europa">
    &lt;option>Madrid&lt;/option>
    &lt;option>Londres&lt;/option>
    &lt;option>Paris&lt;/option>
  &lt;/optgroup>
  &lt;optgroup label="Suramerica">
    &lt;option>Santiago&lt;/option>
    &lt;option>Sao Paulo&lt;/option>
    &lt;option>Lima&lt;/option>
    &lt;option>Bogota&lt;/option>
  &lt;/optgroup>
  &lt;optgroup label="Africa">
    &lt;option>Casablanca&lt;/option>
    &lt;option>Ciudad del Cabo&lt;/option>
  &lt;/optgroup>
&lt;/select></pre>

### <a name="button"></a>Botones Una vez que hemos insertado campos de texto en nuestro formulario es hora de insertar botones.

***Mediante los botones podremos realizar operaciones de envío del formulario***, de manipulación de datos, borrado,... Existen dos formas de insertar botones dentro de un formulario: el [elemento input][2] y el [elemento button][14]. La primera es recurre nuevamente al [elemento input][2] que hemos visto anteriormente para los campos de texto. La sintaxis para un botón mediante un [elemento input][2] será: <pre lang="html4strict">&lt;input type=”button” value=”TextoBotón”/></pre> Si bien, este botón no hace nada por sí solo y tendríamos que darle un comportamiento vía Javascript para que el botón tuviera funcionalidad.

#### *Botones de envío* En el caso del

[elemento input][2] podemos poner botones de otras dos formas y en estos casos ya con funcionalidad. Estos son los tipos ***“submit”*** y ***“reset”.*** Para crear un botón que nos envíe los datos del formulario al servidor tenemos el tipo submit. Su sintaxis es la siguiente: <pre lang="html4strict">&lt;input type=”submit” value=”TextoBotón”/></pre> Una vez que pulsemos sobre el botón se enviarán los datos que el usuario haya insertado en el formulario.

#### *Botones de borrado* El otro tipo de botón con funcionalidad es el que nos permite el borrado de los datos del formulario. Para ello tenemos el tipo “reset”. La sintaxis de este botón será:

<pre lang="html4strict">&lt;input type=”reset” value=”TextoBotón”/></pre> Cuando el usuario pulse sobre el botón de borrado. Todos los valores que el usuario haya insertado en el formulario se eliminarán.

#### *El elemento button* Como hemos visto hasta ahora los botones que hemos insertado han sido mediante el

[elemento input][2], si bien contamos con otro elemento para poner botones en el formulario que es el [elemento button][14]. Cuya funcionalidad es la misma que la del [elemento input][2]. La sintaxis del [elemento button][14] es: <pre lang="html4strict">&lt;button name=”nombre” type=”TipoBoton” value=”ValorBoton”>&lt;/button></pre> Dependiendo del tipo que asignamos al

[atributo type][15] obtendremos un comportamiento u otro:
*   **submit**, crea un botón para el envío de formulario.
*   **reset**, crea un botón para el borrado de datos del formulario.
*   **button**, crea un botón normal.

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:INPUT
 [3]: http://www.w3api.com/wiki/HTML:INPUT.checked
 [4]: http://www.w3api.com/wiki/HTML:Name
 [5]: http://www.w3api.com/wiki/HTML:Src
 [6]: http://www.w3api.com/wiki/HTML:Alt
 [7]: http://www.w3api.com/wiki/HTML:TEXTAREA
 [8]: http://www.w3api.com/wiki/HTML:TEXTAREA.rows
 [9]: http://www.w3api.com/wiki/HTML:TEXTAREA.cols
 [10]: http://www.w3api.com/wiki/HTML:SELECT
 [11]: http://www.w3api.com/wiki/HTML:OPTION
 [12]: http://www.w3api.com/wiki/HTML:Selected
 [13]: http://www.w3api.com/wiki/HTML:OPTGROUP
 [14]: http://www.w3api.com/wiki/HTML:BUTTON
 [15]: http://www.w3api.com/wiki/HTML:Type
