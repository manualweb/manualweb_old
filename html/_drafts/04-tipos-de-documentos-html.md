---
ID: 1361
post_title: '04 &#8211; Tipos de documentos HTML'
author: Víctor Cuervo
post_date: 2017-04-11 01:29:19
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1361
published: false
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
    http://lineadecodigo.com/tag/html-basicos/feed/
gitfolder:
  - html
---
<span style="font-weight: 400">Lo primero que tiene que hacer un documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> es definir su <strong>DOCTYPE o tipo de documento HTLM que es</strong>. Para ello la <a href="http://www.w3.org">W3C</a> ha definido una serie de tipos de documentos.</span> <span style="font-weight: 400">La declaración del DOCTYPE tiene que ser la primera línea de nuestro documento </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">.</span> <span style="font-weight: 400">En el caso de que no indiquemos el DOCTYPE del documento el navegador interpretará el documento como quirks o modo de compatibilidad. Buscando que el contenido de la página pueda ser visualizado.</span> <span style="font-weight: 400">Algunos de los tipos de DOCTYPE que define la <a href="http://www.w3.org">W3C</a> con:</span> <li style="font-weight: 400">
  <span style="font-weight: 400">HTML 4.01 transitorio</span>
</li>
<li style="font-weight: 400">
  <span style="font-weight: 400">HTML 4.01 frameset</span>
</li>
<li style="font-weight: 400">
  <span style="font-weight: 400">HTML Estricto</span>
</li>
<li style="font-weight: 400">
  <span style="font-weight: 400">HTML5</span>
</li>

### **HTML 4.01 Estricto**

<span style="font-weight: 400">Implica que el documento que generemos tiene que ser compatible con la definición del estándar <a href="http://www.manualweb.net/tutorial-html/"><span style="font-weight: 400">HTML</span></a> 4.01. Es por ello que todos los elementos que utilicemos en el documento tienes que estar dentro de la definición.</span> <span style="font-weight: 400">Este modo es interpretado correctamente por todos los navegadores y es compatible con el <a href="http://www.manualweb.net/tutorial-css/">estándar CSS</a>. Además que conseguiremos tener documentos accesibles.</span> <span style="font-weight: 400">Aunque no contempla las reglas del estándar XHTML sobre anidación, escritura,... es un punto sencillo para hacer una migración hacia XHTML.</span> <span style="font-weight: 400">La cabecera que utilizaremos en este caso será:</span>

<pre></pre>

<span style="font-weight: 400">Hay que tener cuidado con el modo estricto ya que algunos navegadores antiguos pueden no interpretar este tipo de documentos.</span>

### **HTML 4.01 Transitorio**

<span style="font-weight: 400">El nombre de transitorio le viene porque no llega a ser un documento 100% estricto, pero está en camino o en transición a conseguirlo.</span> <span style="font-weight: 400">De igual manera que en el modo estricto los elementos deben de ser de la especificación HTML 4.01, si bien se permiten elementos que estén obsoletos o deprecados.</span> <span style="font-weight: 400">La cabecera que utilizaremos en estos casos será:</span>

<pre></pre>

### **HTML 4.01 Frameset**

<span style="font-weight: 400">En el caso de que nuestra página esté compuesta por frames deberemos de utilizar un tipo de DOCTYPE frameset.</span> <span style="font-weight: 400">La cabecera que utilicemos en estos casos será:</span>

<

pre lang="html4strict">

### **HTML5** 

<span style="font-weight: 400">En </span>[<span style="font-weight: 400">HTML5</span>][2]<span style="font-weight: 400"> han dado un giro a la cabecera ya que han visto que era demasiado compleja para los desarrolladores. Así que lo han reducido a la máxima expresión.</span>

<span style="font-weight: 400">La cabecera que utilizaremos en los documentos </span>[<span style="font-weight: 400">HTML5</span>][2]<span style="font-weight: 400"> será:</span>

<pre></pre>

<span style="font-weight: 400">Una de las cosas que vemos en este DOCTYPE es que ya no existe una dependencia del DTD del lenguaje.</span>

### **Validando documentos** 

<span style="font-weight: 400">Una vez que hayamos construido un documento lo mejor que podemos es validarlo. Para ello la W3C nos proporciona un validador en </span>[<span style="font-weight: 400">http://validator.w3.org/</span>][3]

<span style="font-weight: 400">Mediante esta sencilla herramienta podremos validar un documento a partir de una URL de Internet, subiendo un fichero o escribiendo directamente en una caja de texto.</span>

<span style="font-weight: 400">Así podremos ver si el documento que hemos generado es compatible con el DOCTYPE que hayamos definido.</span>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.manualweb.net/tutorial-html5/
 [3]: http://validator.w3.org/