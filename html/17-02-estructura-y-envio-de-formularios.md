---
ID: 1408
post_title: >
  17.02 – Estructura y envío de
  formularios
author: Víctor Cuervo
post_date: 2017-04-12 20:04:33
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/estructura-y-envio-de-formularios/
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
urlvideo:
  - PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos:
  - >
    http://lineadecodigo.com/tag/html-form/feed/
gitfolder:
  - html
---
Una de las cosas importantes que tenemos que saber de los formularios [HTML][1] es cómo funciona la Estructura y envío de formularios.

### <a name="label"></a>Etiquetando el formulario Hemos visto cómo insertar campos para que el usuario introduzca información en el formulario. En algunos casos hemos visto que aunque el campo tiene un dato de valor no lleva una etiqueta asociada. Es verdad que podemos poner texto al lado del elemento de entrada de datos. Por ejemplo en un checkbox:

<pre>Equipo: &lt;input type=”checkbox” id=”betis” name=”equipo” value=”Real Betis”/&gt;Real Betis</pre>

¿Quién nos dice que el texto asociado al checkbox es “Equipo” o “Real Betis”? Para resolver esto el lenguaje

[HTML][1] nos proporciona el [elemento label][2]. La sintaxis del [elemento label][2] es la siguiente:

<pre>&lt;label for=”identificador”&gt;Texto de la Etiqueta&lt;/label&gt;</pre>

El

**atributo for** llevará asociado un identificador que deberá de coincidir con el valor de algún [atributo id][3] de uno de los elementos del formulario. Y será sobre ese elemento sobre el que quede asociado. De esta forma, en el caso que definimos anteriormente sobre el checkbox, la forma correcta de asociar una etiqueta al elemento será la siguiente:

<pre>Equipo: &lt;input type=”checkbox” id=”betis” name=”equipo” value=”Real Betis”/&gt;
&lt;label for=”betis”&gt;Real Betis&lt;/label&gt;</pre>

### <a name="fieldset"></a>Estructura del formulario En

[HTML][1] contamos con dos elementos para dar una ***estructura a los formularios***. Estos elementos: [fieldset][4] y [legend][5] nos ayudan a agrupar los datos relacionados dentro del formulario. Pero vayamos por parte. El primero es [fieldset][4], este es un elemento que agrupa a diferentes elementos del formulario, elementos que están relacionados entre ellos. La sintaxis de [fieldset][4] es la siguiente:

<pre><fieldset>
  ...
    
  
</fieldset></pre>

Entre estos elementos aparecerán los campos del formulario. Por ejemplo si tenemos campos personales básicos podemos agruparlos de la siguiente forma:

<pre><fieldset>
  <label for="nombre">Nombre</label>
        <label for="apellido">Apellido</label>
    
    
  
</fieldset></pre>

El

[elemento legend][5] nos servirá para darle un significado a una agrupación

<pre><fieldset>
  &lt;legend&gt;Introduzca sus datos personales&lt;/legend&gt;
        <label for="nombre">Nombre</label>
        <label for="apellido">Apellido</label>
    
    
  
</fieldset></pre>

### <a name="foco"></a>Hacer foco en el formulario Cuando construyamos un formulario deberemos de preocuparnos por cómo hacer foco en los elementos. Está claro que si utilizamos un navegador web el uso del ratón nos facilitará el ir rellenando cada uno de los campos del formulario. Pero piensa en alguien que no tenga un ratón o bien que utilice un agente de usuario no visual adaptado para discapacitados. En este caso y para temas de accesibilidad tenemos dos formas de hacer foco en el formulario. Una será el uso de la tabulación, y el otro el uso de teclas de acceso.

#### Tabulaciones por el formulario Para las navegaciones por tabulación en el formulario existe el

**atributo tabindex**. Este atributo que lo podemos encontrar en todos los elementos de un formulario nos sirve para establecer un orden mediante números ordinales de los campos del formulario. La estructura del **atributo tabindex** es:

<pre>tabindex=”numero”</pre>

De esta forma podríamos establecer el orden de un formulario de dos datos básicos y un botón mediante el siguiente código:

<pre><label for="nombre">Nombre</label>&lt;input tabindex=”1” type="text" id="nombre"/&gt;
<label for="apellido">Apellido</label>&lt;input tabindex=”2” type="text" id="apellido"/&gt;
&lt;button id=”envio” tabindex=”3”&gt;Enviar Formulario&lt;/button&gt;</pre>

#### Teclas de acceso Otra forma de poder acceder a un elemento del formulario es asignando al elemento una tecla de acceso. De esta manera cuando pulsamos esta tecla (en combinación con alguna definida en el sistema, como la tecla ALT para Windows) iremos directamente a dicho elemento. El atributo que nos permite hacer esto es el

**atributo accesskey**. La estructura del **atributo accesskey** es la siguiente:

<pre>accesskey=tecla</pre>

Así podríamos definir un campo de un formulario al cual fuésemos al pulsar sobre la “tecla N”:

<pre>&lt;label for="nombre" accesskey=”N”&gt;Nombre&lt;/label&gt;
&lt;input tabindex=”1” type="text" id="nombre"/&gt;</pre>

### <a name="diseabled"></a>Deshabilitar controles A la hora de crear un formulario puede darse el caso que haya algunos campos que en determinados momentos nos aparezcan deshabilitados. Es decir, que el usuario no pueda modificar el valor de dichos campos. Para poder deshabilitar los controles de un formulario contamos con el

**atributo disabled**. La estructura del **atributo disabled** es directamente:

<pre>disabled</pre>

De esta manera si queremos deshabilitar nuestro anterior campo de texto que nos permitía insertar un nombre escribimos lo siguiente:

<pre>&lt;label for="nombre" accesskey=”N”&gt;Nombre&lt;/label&gt;
</pre>

No podremos hacer foco sobre los elementos de un formulario que estén deshabilitados. De igual manera al hacer tabulación tampoco se podrá tabular sobre ellos. Además no se enviarán como parte de la petición del formulario. En el caso de que queramos buscar el mismo efecto de que el elemento esté deshabilitado, pero que se pueda tabular, hacer foco y enviar, tenemos el atributo de solo lectura o readonly. La estructura del

**atributo readonly** es básica:

<pre>readonly</pre>

Si lo aplicamos nuevamente a nuestro campo de texto tendremos:

<pre>&lt;label for="nombre" accesskey=”N”&gt;Nombre&lt;/label&gt;
</pre>

El atributo readonly solo se puede aplicar a

[elementos input][6] y [textarea][7].

### <a name="submit"></a>Envío del formulario Una vez que ya hemos construido nuestro formulario solo nos quedará una cosa, esta será enviar el formulario. Para enviar el formulario deberemos de controlar dos cosas. Por un lado a dónde lo vamos a enviar, es decir, cual es la URL del programa destino (o página destino) que va a procesar los datos del formulario y que nos va a dar una respuesta. Por otro lado está el tipo de envío de los parámetros. En el caso del tipo de envío tenemos la posibilidad de hacerlo mediante un formato GET (con los datos visibles) o POST (con los datos no visibles). Ambos elementos los configuraremos dentro del

[elemento form][8].

#### Destino del formulario Para establecer el destino del formulario tenemos el

[atributo action][9]. El [atributo action][9] tiene la URL de destino del formulario. La estructura del [atributo action][9] es:

<pre></pre>

Las URL de destino suelen ser programas o código de servidor, ya sea

[Java][10], [PHP][11], Node, [ASP][11],... Los cuales recuperan la información del formulario, la manipulan y nos devuelven una nueva página [HTML][1].

#### Tipo de envío: GET y POST Para establecer el tipo de envío del formulario tenemos el

[atributo method][12]. El [atributo method][12] puede tener dos valores: GET y POST. El atributo method lo encontramos dentro del [elemento form][8]:

<pre></pre>

A la hora de enviar los

** formularios de forma GET** lo que vamos a conseguir es que a la URL destino del formulario se le añaden los parámetros con los datos del formulario en la estructura: <samp>action?nombre1=valor1&nombre2=valor2&...&nombreN=valorN</samp> Si tenemos el siguiente formulario:

<pre></pre>

Lo que se enviará en la URL será algo parecido a:

<samp>envio.php?name=Victor&apellido=Cuervo</samp> Es importante que nos fijemos que utiliza el valor que hay dentro de los [atributos name][13] para realizar el envío. Si indicamos que el método de envío del formulario es POST lo que hará el navegador es enviar los datos junto al cuerpo del formulario y no se verán en la URL. Así, en el siguiente formulario:

<pre></pre>

Solo veremos, al enviarlo:

<samp>enviar.php</samp>

#### Formato del contenido del formulario Cuando enviamos el formulario deberemos de saber qué sucede con el contenido. Es decir, si lo envía de alguna forma en especial o con algún tipo de tratamiento. Lo primero que tenemos que saber es que el campo que permite establecer el formato del contenido del formulario es

**enctype**, que es un atributo del [elemento form][8]:

<pre></pre>

Los formularios, por defecto, se envían mediante el formato

**application/x-www-form-urlencoded. **Este formato lo que hace es sustituir los espacios por + y convierte los caracteres especiales en secuencias de escape. Por otro lado las combinaciones de nombre valor las separa por un = y las parejas con símbolos &. Como ya vimos en las peticiones del tipo GET.

<pre></pre>

Si bien, en el caso de que queramos enviar formularios con un gran volumen de información o con imágenes, deberemos de utilizar el tipo

**multipart/form-data**.

<pre></pre>

Los formularios que utilizan el tipo

**multipart/form-data** contienen una serie de partes conocidas como form-data en las que va cada uno de los campos enviados en el formulario. De esta forma si tenemos el siguiente formulario:

<pre></pre>

La petición multipart podría ser de la siguiente forma:

<pre>-----------------------------931237358445456570660578548
Content-Disposition: form-data; name="nombre"

Victor
-----------------------------931237358445456570660578548
Content-Disposition: form-data; name="apellido"

Cuervo
-----------------------------931237358445456570660578548
Content-Disposition: form-data; name="fichero"; filename="fotografia.png"
Content-Type: image/png</pre>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:LABEL
 [3]: http://www.w3api.com/wiki/HTML:Id
 [4]: http://www.w3api.com/wiki/HTML:FIELDSET
 [5]: http://www.w3api.com/wiki/HTML:LEGEND
 [6]: http://www.w3api.com/wiki/HTML:INPUT
 [7]: http://www.w3api.com/wiki/HTML:TEXTAREA
 [8]: http://www.w3api.com/wiki/HTML:FORM
 [9]: http://www.w3api.com/wiki/HTML:Action
 [10]: http://www.manualweb.net/tutorial-java/
 [11]: http://www.manualweb.net/tutorial-php/
 [12]: http://www.w3api.com/wiki/HTML:Method
 [13]: http://www.w3api.com/wiki/HTML:Name