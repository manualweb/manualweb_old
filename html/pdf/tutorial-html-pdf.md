# Tutorial HTML

![Tutorial HTML](https://github.com/manualweb/manualweb/raw/master/html/images/html-logo.png)

| | |
|---|---|
|autor:|[Víctor Cuervo](http://www.victorcuervo.com)|
|versión:|v1.0|
|fecha:|2017-04-12|
|url:|http://www.manualweb.net/tutorial-html/|
|github:|https://github.com/manualweb/manualweb/tree/master/html|

## Índice

* Introducción a la World Wide Web
* Introducción al HTML
* Historia del HTML
  * Historia del HTML: Los inicios
  * Historia del HTML: El estándar
* Tipos de documentos HTML
* Sintaxis del HTM
* El documento HTML
* Mi Primera Página HTML
* Metadatos: Las metatags de HTML
* Texto en HTML
  * Texto básico en HTML
  * Texto avanzado en HTML
* Colores en HTML
* Imágenes en HTML
* Mapa de imágenes
* Enlaces en HTML
* Agrupaciones en HTML
* Listas en HTML
* Tablas en HTML
  * Tablas Básicas en HTML
  * Tablas Avanzadas en HTML
* Formularios en HTML
  * Campos de Formularios
  * Estructura y envío de formularios

## Introducción a la World Wide Web

Hoy en día la tecnología de la red, va avanzando a pasos agigantados. ¿Por qué? La razón es que tanto las empresas como a nivel individual la sociedad se está dando cuenta de todas las posibilidades que la 'red de redes' nos ofrece.

Antes de adentrarnos en el [HTML][1] deberemos de tener una serie de conceptos básicos sobre lo que es Internet y el mundo que lo rodea.

### ¿Qué es Internet?

Internet es un conjunto de ordenadores o red de ordenadores interconectados entre mediante algún soporte, ya sea físico o inalámbrico. El lenguaje que utilizan los ordenadores para hablarse entre ellos se llama TCP/IP. Mediante el lenguaje TCP/IP las máquinas se intercambian la información.

### El Inicio: Comunicando máquinas

En 1969 nace un proyecto de índole militar en EEUU llamado ARPANET, este proyecto es el primero que permite conectar máquinas de diferentes universidades entre sí.

Poco a poco el proyecto fue cogiendo un matiz de investigación hasta separarse del propio proyecto militar, conectando más máquinas, y llegando a conceptualizar lo que es Internet Así hasta llegar a los día de hoy, donde las máquinas que están conectadas a la red son de empresas, universidades, personales,... dónde las máquinas ya no son solo ordenadores, sino que pueden ser móviles, elementos de domótica, coches,...

### La World Wide Web y el HTML

Un poco más tarde, sobre 1990, en el CERN, Tim Berners Lee y una serie de colaboradores definió un sistema de almacenamiento y recuperación de información. De tal manera que la información pudiese ser consultada de una forma estándar desde cualquier sitio. Estaba naciendo el lenguaje que define la información, nacía [HTML][1]. Era la gestación de la **World Wide Web**, información enlazada una con otra creando el tejido que es la red.

Actualmente el lenguaje [HTML][1] tiene [como especificación oficial HTML 5.0][2] *(28 de octubre de 2014)* y se está trabajando en [el borrador de HTML 5.1][3] *(última actualización [el 10 de marzo de 2016][4])*.

El lenguaje **HTML (HyperText Markup Language)** o lenguaje de etiquetas de hipertexto es un lenguaje que permite definir la estructura de una página web mediante un conjunto de elementos o etiquetas. La base de los documentos web o documentos [HTML][1] es que unos se van enlazando con otros creando una gran malla o red de documentos que es lo que conocemos como World Wide Web, “la red” o más comúnmente como “la web”.

### Los Navegadores Web y las URL

Solo faltaban los programas que nos permitieran visualizar dicha información. De esta forma en 1993 se creaba el **navegador web** Mosaic.

Herramienta imprescindible para poder visualizar el contenido HTML. Los navegadores web son las herramientas que nos permiten movernos por la red, visualizar y acceder a los contenidos de la misma.

Muy atrás han quedado los tiempos en los que solo existía el navegador web Mosaic y ahora en el mercado podemos encontrar una gran cantidad de navegadores web: [Chrome][5], [Firefox][6], [Opera][7], [Safari][8], [Internet Explorer][9],...

Para identificar cada uno de los contenidos que hay en la red se ha definido el concepto de **URL (o URI)**. Mediante una URL podemos acceder a cualquier contenido de la red utilizando un agente de usuario, más conocido como navegador web o browser.

Una URL se compone, a modo general, de diferentes partes:

* **Protocolo**, es el tipo de comunicación que queremos establecer con la máquina. Por ejemplo, si queremos visualizar un documento utilizaremos http, si queremos recuperar un fichero indicaremos ftp,...
* **Máquina**, será la máquina que tiene el contenido. Las máquinas se identifican mediante un código numérico llamado IP, pero como esos códigos con complejos de aprender las damos nombres. Así podemos conocer una máquina (o máquinas) como [google.com][10], [lineadecodigo.com][11], [manualweb.net][12],...
* **Contenido**, será el contenido al cual queremos acceder. Este puede ser el nombre de un fichero, el nombre de una página web, el nombre de un vídeo,... El contenido suele estar ubicado en un directorio, por lo cual dicho nombre suele venir antepuesto de la ruta de un directorio.

La estructura general de una URL será la siguiente:

<pre>protocolo://máquina/contenido</pre>

Si nos fijamos en los nombres de las máquinas, estos suelen tener dos partes:

* **Nombre de la Máquina**, este suele ser el nombre del servicio al que intentamos acceder. Por ejemplo: google, manualweb, elpais,...
* **Dominio**, es la extensión que nos permite identificar el tipo o ubicación del servicio al que accedemos. Por ejemplo: .com, .net, .gov,... Aunque hay que tener cuidado ya que los dominios, en ciertos casos, no están reglados y pueden referirse a otra cosa distinta.

Algunos dominios que podemos encontrarnos son:

* **.com**, para empresas o compañías. - [http://www.google.com][10]</a>
* **.org**, para organizaciones. - [http://www.greenpeace.org][13]
* **.edu**, para recursos de educación y universidades. - [http://www.mit.edu][14]
* **.mil**, para estamentos militares. - [http://www.navy.mil][15]
* **.gov**, para elementos gubernamentales. - [http://www.whitehouse.gov][16]
* **.es, .fr, .co, .pe, .ar,...** son dominios de países (españa, francia, colombia, perú, argentina,...) - [http://www.red.es][17]

## Introducción al HTML

### ¿Qué es el HTML?

**HTML (HyperText Markup Language)** es un lenguaje que nos permite crear páginas web mediante etiquetas o elementos.

Mediante [HTML][1] podremos incluir dentro de nuestras páginas web *texto, imágenes, enlaces, tablas, vídeos, música,...* cualquier elemento que te puedas imaginar. Todo elemento es representado por una etiqueta.

Las páginas web que creemos **serán visualizadas mediante un navegador web o browser**, los cuales interpretan en contenido del documento y lo presentan de forma visual. De manera forman es conocido como **agente de usuario.** Ya que a parte de los navegadores web pueden existir programas que exploten de otra manera el contenido, por ejemplo los lectores de contenido adaptados a discapacitados.

La característica principal del [HTML][1] son los enlaces. Mediante los enlaces podremos realizar navegaciones entre páginas web, movernos de una a otra. Esta característica es la que hace diferente al lenguaje [HTML][1] de otros formatos como Microsoft Word, PDF,...

### ¿Quién define el HTML?

El organismo encargado de la definición, supervisión y evolución del lenguaje estándar [HTML][1] es el [W3C (World Wide Web Consortium)][18]. Si bien, son las diferentes empresas que construyen software relacionado con el lenguaje [HTML][1] quienes implementan el lenguaje.

Esto puede dar en algunos casos que haya implementaciones de elementos por fuera del lenguaje, o que el mismo elemento se comporte de forma diferente dependiendo del navegador que lo visualice.

La especificación oficial del lenguaje [HTML][1] es [HTML 5.0][2] *(28 de octubre de 2014) *y se está trabajando en [el borrador de HTML 5.1][3] *(última actualización *[*el 10 de marzo de 2016*][19]*).*

### Herramientas para crear código HTML

Las páginas [HTML][1] son nada más que texto plano. Es por ello que, para crearlas, simplemente necesitemos de la ayuda de un editor o procesador de textos.

#### Editores de Texto

Puedes utilizar cualquier editor de texto. El Notepad o WordPad de Microsoft Windows, [UltraEdit][20], [NoteTab][21], el TextEdit de Mac, o un editor avanzado como [Sublime Text][22] o [Atom][23].

#### Herramientas WYSIWYG

Si bien, existe otra alternativa que es el utilizar herramientas WYSIWYG *(Why You See Is What You Get)*. Estas herramientas nos proporcionan un interface gráfico para poder montar la página web, ocultándose el código [HTML][1] que se genera por debajo.

Si bien, estas herramientas, casi siempre, nos dejarán editar el código [HTML][1] generado.

Algunos ejemplos de herramientas *HTML WYSIWYG*:

* [CoffeCup HTML Editor][24]
* [HoTMetal Pro][25]
* [DreamWeaver][26]
* [Microsoft Expression][27]

#### Herramientas On-Line

Ahora está muy de moda el crear la página web desde una herramienta on-line. Es decir, desde una página web.

Este tipo de sitios te permiten dos cosas: por un lado *crear tu página web de forma gráfica* y por otro *almacenarla* (en muchos casos de forma gratuita) para que la pueda visualizar la gente. Algunos de estos sitios son:

* [Google Sites][28]
* [IM Creator][29]
* [WIX][30]
* Sitios de blogs: [WordPress][31], [Blogger][32],...

## La historia del HTML

La historia del [HTML][1] ha sido muy cambiante desde que [Tim Berners-Lee][33] y [Robert Cailliau][34] trabajasen en el **CERN** y tuviesen la necesidad de establecer una forma de **compartir la información.** Daba lugar al nacimiento del hipertexto, enlaces y protocolo http, todo lo que acabo siendo el lenguaje [HTML][1].

Ha pasado por épocas de definición en sus primeras versiones **HTML 2** y **HTML 3.2**. Ha permitido la creación del [W3C][18] para la gestión de estándares. Ha vivido la ***"guerra de los navegadores"*** entre *Internet Explorer* y *Netscape*. Se ha conseguido estandarizar con gran aceptación en **HTML 4.01**. Y ha visto como "unos disidentes" abandonaron el [W3C][18] para generar un evolucionado y moderno **[HTML 5][35].**

Así podríamos resumir **la historia del [HTML][1] en las siguientes épocas**:

*   Inicios del HTML
*   HTML Tags y Mosaic
*   HTML 2.0
*   Creación de la W3C y HTML 3.0
*   HTML 3.2
*   HTML 4.01
*   XML y XHTML 1.0
*   HTML 5
*   HTML.next 

## La Historia del HTML: Los Inicios

### Los inicios del HTML

Los inicios de HTML se deben a [Tim Berners-Lee][33] cuando trabajaba en el **CERN (Centro Europeo de Investigación Nuclear)**. Y es que estando como trabajador del CERN se encontró con la problemática de poder facilitar el acceso a la información con la que trabajaban desde cualquier ordenador del centro o de otras instituciones que trabajaban con ellos.

Buscaban una forma sencilla y estándar de acceder a toda la información. Es en ese momento cuando nace el **protocolo HTTP** (hypertext transfer protocol) y las páginas [HTML][1].

Además ideó que las páginas estarían unidas entre sí, estarían enlazadas. Era el concepto de **hipertexto.**

Para la definición del estándar HTML, [Tim Berners-Lee][33] se basó en el lenguaje de marcado **SGML (Standard General Markup Language)**. Este lenguaje define reglas de etiquetado y estructura generales. A partir de SGML se han definido lenguajes como [HTML][1], Postscript, RTF,...

Tras tener el desarrollo del sistema de Hipertexto interno, [Tim Berners-Lee][33] lo presentó a una convocatoria para desarrollar el sistema Hipertexto en Internet junto con el ingeniero de sistemas [Robert Cailliau][34]. La propuesta que presentaron la llamaron **World Wide Web (W3)**.

### HTML Tags y Mosaic

**La primera versión del [HTML][1] nace hacía 1989 como un subconjunto de SGML** y es especificada mediante un documento que se denomina [HTML Tags][36].

En el documento [HTML Tags][36] ya podemos ver los conceptos básicos del lenguaje HTML ya que en él se define como insertar texto, títulos, enlaces y listas. Y algún elemento que acabó perdiéndose con el paso del tiempo como la identificación de índice del documento.

Podemos observar que intentan aglutinar en un lenguaje conceptos como estructura, formato y semántica, los cuales han ido derivando a la creación de otros lenguajes como [CSS][37] y [XML][38].

Junto con [HTML Tags][36] **aparece el primer navegador para poder visualizar las páginas que se llamó “WorldWideWeb”.**

Posteriormente se crearían otros navegadores web (Samba, Erwise, y Viola) además del que puede ser considerado como el primer navegador web global que fue [Mosaic][39], desarrollado por NCSA.

El grupo de gente que creo [Mosaic][39] (Mark Andreessen entre ellos) abandonó NCSA para crear posteriormente Netscape.

### HTML 2.0

El proyecto World Wide Web se empieza a extender por el mundo, siendo varios proveedores de servicios (entre ellos AOL) los que empiezan a dar acceso a la red.

En paralelo a esta creciente entrada colaboradores aparece, en noviembre de 1995, [HTML 2.0][40]. La versión [HTML 2.0][40] es desarrollada por el **IETF (Internet Engineering Task Force)**.

[HTML 2.0][40] es la primera versión que podríamos considerar como estándar, o al menos definida por un organismo oficial.

En [HTML 2.0][40] con respecto al inicial [HTML Tags][36] podíamos encontrar cosas como imágenes, mapas de imágenes, formularios, barras separadoras... así como una definición inicial del DTD HTML.

### Creación de la W3C y HTML 3.0

Tras diferentes conversaciones entre [Tim Berners-Lee][33] y el MIT, el 1 de octubre de 1994 es creado el consorcio W3. Más conocido como [W3C][18] (World Wide Web Consortium) con la idea de definir estándares para Internet.

Dentro de la [W3C][18] se empieza a trabajar en noviembre 1995 sobre el borrador de [HTML 3.0][41], el cual nunca llegará a ser recomendación y se quedará en borrador.

Es **HTML 3.2** la versión que pasa a ser la recomendación. El borrador de [HTML 3.0][41] es interesante ya que se empieza a hablar de elementos como tablas, textos alrededor de las imágenes, y un [elemento llamado MATH][42] que permite crear fórmulas dentro del documento [HTML][1].

El elemento MATH acabó cayéndose de posteriores revisiones del lenguaje [HTML][1] y conformando un nuevo lenguaje en sí llamado [MathML][43].

Una de las cosas que más buscaba [HTML 3.0][41] es que fuese compatible hacia atrás con todo lo que se había creado hasta entonces. Quizás un trabajo demasiado teórico.

### HTML 3.2

Podríamos decir que [HTML 3.2][44] es la primera versión de [HTML][1] ampliamente extendida y utilizada en la red.

[HTML 3.2][44] dejaba de ser una especificación teórica, buscaba ser más práctica. **[HTML 3.2][44] veía la luz en enero de 1997**.

En [HTML 3.2][44] se pasaban a utilizar elementos que habían nacido fuera de la especificación y que habían sido definidos por los fabricantes como Netscape e Internet Explorer.

Así podemos encontrar en [HTML 3.2][44] la *capacidad de crear código script, capas, formularios, posibilidad de meter Applets de [Java][45], modificar el tamaño metiendo fuentes,..*

Quizás la especificación [HTML 3.2][44] quedó demasiado abierta y empezó una **“guerra entre navegadores”** en la que cada fabricante quería presionar porque se aceptasen sus elementos. Así Internet Explorer presionaba para tener el **elemento MARQUEE **y Netscape para tener el elemento **BLINK**.

## Historia del HTML: El estándar

### HTML 4.01

Después de años de lucha entre los fabricantes la W3C intentaba poner un poco de orden con las versiones de HTML 4 y [HTML 4.01][46] en los años 1998 y 1999 respectivamente.

Por el momento la especificación [HTML 4.01][46] (24 de diciembre de 1999) es la más longeva del estándar.

En [HTML 4.01][46] la W3C empieza con la separación de la estructura del documento con la de la representación visual. Así crea un lenguaje paralelo al [HTML 4.01][46] llamado [CSS][37].

Los elementos nuevos que aparecen en [HTML 4.01][46] son las hojas de estilo ([CSS][37]), los objetos (para poder insertar elementos externos como vídeo y música) y los frameset para dividir la pantalla en partes.

Aunque [HTML 4.01][46] era un lenguaje que definía de forma clara el estándar [HTML][1] y lo consensuaba entre los diferentes navegadores web, todavía dejaba abierta la posibilidad de interpretación de la estructura. Esta interpretación venía derivada de que la base del [HTML][1] seguía siendo el esquema de SGML.

### XML y XHTML 1.0

Debido a la falta de coherencia en la definición de los esquemas derivados del SGML, la W3C decide definir un nuevo subesquema de SGML denominado [XML][38]. Este esquema sería un esquema bien definido y cerrado, lo cual podría proporcionarnos documentos coherentes y sin posibilidad de dobles interpretaciones.

El lenguaje [XML 1.0][47] es creado el 10 de febrero de 1998, principalmente para la compartición de datos entre computadoras. Si bien, la W3C ve al XML como una posible solución a sus problemas de interpretación del [HTML 4.01][46] creando el lenguaje [XHTML 1.0][48] (eXtensible HyperText Markup Language).

[XHTML 1.0][48] viene a ser los mismo que [HTML 4.01][46] pero con una definición de documento basada sobre [XML][38] en vez de sobre SGML.

Así se dictan una serie de normas de las cuales la principal es que el documento [XHTML 1.0][48] tiene que ser un **documento bien formado.** Para ello se establecen normas como que todo elemento que tenga una etiqueta de inicio debe de tener obligatoriamente una etiqueta de fin, que los nombres de los elementos y de los atributos deben de ir en minúsculas, no podrán existir atributos que vayan sin valor,...

La definición de [XHTML 1.0][48] pasa a ser bastante estricta para el lenguaje [HTML][1].

### HTML5

Una vez publicado [XHTML 1.0][48] los esfuerzos de la W3C se dirigen a la creación de XHTML 2.0 como evolución del lenguaje.

Nuevamente la [W3C][18] se mete en un trabajo teórico, lo que hace que algunos “disidentes” (oportunistas para otros), como Ian Hickson,  monten un grupo paralelo conocido como [WHATWG][49] (Web Hypertext Application Technology Working Group) que empieza a trabajar en [HTML5][50] el 4 junio de 2004.

[HTML5][50] empieza su definición apoyándose en dos puntos. Por un lado la compatibilidad hacía atrás de todo lo que hay creado y por otro la capacidad de absorber todas las funcionalidades que los nuevos fabricantes de la web habían ido construyendo, véase Google, Apple u Opera.

Además [WHATWG][49] siempre ha acusado a la [W3C][18] de tener unos procesos de estandarización muy largos y no alineados a las necesidades del mercado.

Entre las nuevas funcionalidades se encuentran la simplicidad para reproducir audio y vídeo, el disponer de un lienzo de dibujo denominado Canvas,.... Además alrededor de [HTML5][50] nacen una gran cantidad de especificaciones para la mejora de las Webapps como son Websockets, Geolocalización, Webstorage,..

La [W3C][18], en 2007, decide aparcar el trabajo realizado con XHTML 2.0 y empezar a trabajar con [HTML5][50]. Si bien el grupo [WHATWG][49] sigue con su trabajo y estudio sobre diferentes API, los cuales irán cayendo en el estándar.

[La especificación de HTML5][51] es publicada oficialmente el 28 de octubre de 2014. Actualmente el [HTML Working Group][52] está trabajando en [el borrador de HTML 5.1][53] *(cuya última actualización es del [10 de marzo de 2016][19]).*

### El futuro del HTML: HTML.next

Tanto la [W3C][18] como el [WHATWG][49] están trabajando sobre la evolución del [HTML5][50]. Cada uno a su ritmo.

Es por ello que es posible que muchas de las cosas en las que está trabajando [WHATWG][49] no acaben dentro del estándar [HTML5][50]. Así [un subconjunto del trabajo sobre HTML5 pasará a ser recomendación del W3C y la otra parte pasará para las siguientes versiones][54]. Esto es lo que se ha dado a conocer como [HTML.next][55]

En [HTML.next][55] están [propuestos elementos][56] como RECO, para el reconocimiento de voz, áreas de texto WYSIWYG, DATAGRID para representar datos tabulares, DATA para insertar elementos sólo reconocibles para máquinas,...

## Tipo de documentos HTML

Lo primero que tiene que hacer un documento [HTML][1] es definir su **DOCTYPE o tipo de documento HTLM que es**. Para ello la [W3C][18] ha definido una serie de tipos de documentos.

La declaración del DOCTYPE tiene que ser la primera línea de nuestro documento [HTML][1].

En el caso de que no indiquemos el DOCTYPE del documento el navegador interpretará el documento como quirks o modo de compatibilidad. Buscando que el contenido de la página pueda ser visualizado.

Algunos de los tipos de DOCTYPE que define la [W3C][18] son:

* HTML 4.01 transitorio
* HTML 4.01 frameset
* HTML Estricto
* HTML5

### HTML 4.01 Estricto

Implica que el documento que generemos tiene que ser compatible con la definición del estándar HTML 4.01. Es por ello que todos los elementos que utilicemos en el documento tienes que estar dentro de la definición.

Este modo es interpretado correctamente por todos los navegadores y es compatible con el [estándar CSS][37]. Además que conseguiremos tener documentos accesibles.

Aunque no contempla las reglas del estándar XHTML sobre anidación, escritura,... es un punto sencillo para hacer una migración hacia XHTML.

La cabecera que utilizaremos en este caso será:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Strict//EN" "http://www.w3.org/TR/html4/strict.dtd">
```

Hay que tener cuidado con el modo estricto ya que algunos navegadores antiguos pueden no interpretar este tipo de documentos.

### HTML 4.01 Transitorio

El nombre de transitorio le viene porque no llega a ser un documento 100% estricto, pero está en camino o en transición a conseguirlo.

De igual manera que en el modo estricto los elementos deben de ser de la especificación HTML 4.01, si bien se permiten elementos que estén obsoletos o deprecados.

La cabecera que utilizaremos en estos casos será:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

### HTML 4.01 Frameset

En el caso de que nuestra página esté compuesta por frames deberemos de utilizar un tipo de DOCTYPE frameset.

La cabecera que utilicemos en estos casos será:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
"http://www.w3.org/TR/html4/frameset.dtd">
```

### HTML5

En [HTML5][35] han dado un giro a la cabecera ya que han visto que era demasiado compleja para los desarrolladores. Así que lo han reducido a la máxima expresión.

La cabecera que utilizaremos en los documentos [HTML5][35] será:

```
<!DOCTYPE html>
```

Una de las cosas que vemos en este DOCTYPE es que ya no existe una dependencia del DTD del lenguaje.

### **Validando documentos**

Una vez que hayamos construido un documento lo mejor que podemos es validarlo. Para ello la W3C nos proporciona un validador en [http://validator.w3.org/][57]

Mediante esta sencilla herramienta podremos validar un documento a partir de una URL de Internet, subiendo un fichero o escribiendo directamente en una caja de texto.

Así podremos ver si el documento que hemos generado es compatible con el DOCTYPE que hayamos definido.


 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3.org/TR/2014/REC-html5-20141028/
 [3]: https://www.w3.org/TR/2016/WD-html51-20160310/
 [4]: https://www.w3.org/blog/news/archives/5313
 [5]: http://www.ayudaenlaweb.com/navegadores/que-es-google-chrome/
 [6]: http://www.ayudaenlaweb.com/navegadores/que-es-firefox/
 [7]: http://www.ayudaenlaweb.com/navegadores/que-es-opera/
 [8]: http://www.ayudaenlaweb.com/navegadores/que-es-safari/
 [9]: http://www.ayudaenlaweb.com/navegadores/que-es-internet-explorer/
 [10]: http://www.google.com
 [11]: http://lineadecodigo.com
 [12]: http://www.manualweb.net
 [13]: http://www.greenpeace.org
 [14]: http://www.mit.edu
 [15]: http://www.navy.mil
 [16]: http://www.whitehouse.gov
 [17]: http://www.red.es
 [18]: http://www.w3.org
 [19]: https://www.w3.org/blog/news/archives/5313
 [20]: http://www.idmcomp.com/
 [21]: http://www.notetab.com/
 [22]: http://www.sublimetext.com/
 [23]: https://atom.io/
 [24]: http://www.coffeecup.com/html-editor/
 [25]: http://www.hotmetalpro.com/
 [26]: http://www.adobe.com/es/products/dreamweaver/
 [27]: http://www.microsoft.com/expression
 [28]: https://sites.google.com/
 [29]: http://imcreator.com/
 [30]: http://es.wix.com/
 [31]: http://www.wordpress.org/
 [32]: http://www.blogger.com/
 [33]: http://www.w3.org/People/Berners-Lee/
 [34]: http://public.web.cern.ch/public/en/people/Cailliau-en.html
 [35]: http://www.manualweb.net/tutorial-html5/
 [36]: http://www.w3.org/History/19921103-hypertext/hypertext/WWW/MarkUp/Tags.html
 [37]: http://www.manualweb.net/tutorial-css/
 [38]: http://www.manualweb.net/tutorial-xml/
 [39]: http://www.ncsa.illinois.edu/Projects/mosaic.html
 [40]: http://www.ietf.org/rfc/rfc1866.txt  
 [41]: http://www.w3.org/MarkUp/html3/CoverPage
 [42]: http://www.w3.org/MarkUp/html3/maths.html
 [43]: http://www.w3.org/Math/
 [44]: http://www.w3.org/TR/REC-html32
 [45]: http://www.manualweb.net/tutorial-java/
 [46]: http://www.w3.org/TR/REC-html40/
 [47]: http://www.w3.org/TR/1998/REC-xml-19980210
 [48]: http://www.w3.org/TR/xhtml1/
 [49]: http://www.whatwg.org/
 [50]: http://www.w3.org/TR/html5/
 [51]: http://www.w3.org/TR/2014/REC-html5-20141028/
 [52]: http://www.w3.org/html/wg/
 [53]: https://www.w3.org/TR/2016/WD-html51-20160310/
 [54]: http://www.w3.org/QA/2012/07/html5_and_htmlnext.html
 [55]: http://www.w3.org/wiki/HTML/next
 [56]: http://www.w3.org/html/wg/next/markup/
 [57]: http://validator.w3.org/
