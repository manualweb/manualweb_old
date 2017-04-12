---
ID: 1345
post_title: '03.02 – Historia del HTML: El estándar'
author: Víctor Cuervo
post_date: 2017-04-11 01:45:53
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/historia-del-html-el-estandar/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
gitfolder: html
---
En **Historia del HTML: El estándar** hablamos de:

[TOC]

<a name="html4"></a>
### HTML 4.01

Después de años de lucha entre los fabricantes la W3C intentaba poner un poco de orden con las versiones de HTML 4 y [HTML 4.01][1] en los años 1998 y 1999 respectivamente.

Por el momento la especificación [HTML 4.01][1] (24 de diciembre de 1999) es la más longeva del estándar.

En [HTML 4.01][1] la W3C empieza con la separación de la estructura del documento con la de la representación visual. Así crea un lenguaje paralelo al [HTML 4.01][1] llamado [CSS][2].

Los elementos nuevos que aparecen en [HTML 4.01][1] son las hojas de estilo ([CSS][2]), los objetos (para poder insertar elementos externos como vídeo y música) y los frameset para dividir la pantalla en partes.

Aunque [HTML 4.01][1] era un lenguaje que definía de forma clara el estándar [HTML][3] y lo consensuaba entre los diferentes navegadores web, todavía dejaba abierta la posibilidad de interpretación de la estructura. Esta interpretación venía derivada de que la base del [HTML][3] seguía siendo el esquema de SGML.


<a name="xml"></a>
### XML y XHTML 1.0

Debido a la falta de coherencia en la definición de los esquemas derivados del SGML, la W3C decide definir un nuevo subesquema de SGML denominado [XML][4]. Este esquema sería un esquema bien definido y cerrado, lo cual podría proporcionarnos documentos coherentes y sin posibilidad de dobles interpretaciones.

El lenguaje [XML 1.0][5] es creado el 10 de febrero de 1998, principalmente para la compartición de datos entre computadoras. Si bien, la W3C ve al XML como una posible solución a sus problemas de interpretación del [HTML 4.01][1] creando el lenguaje [XHTML 1.0][6] (eXtensible HyperText Markup Language).

[XHTML 1.0][6] viene a ser los mismo que [HTML 4.01][1] pero con una definición de documento basada sobre [XML][4] en vez de sobre SGML.

Así se dictan una serie de normas de las cuales la principal es que el documento [XHTML 1.0][6] tiene que ser un **documento bien formado.** Para ello se establecen normas como que todo elemento que tenga una etiqueta de inicio debe de tener obligatoriamente una etiqueta de fin, que los nombres de los elementos y de los atributos deben de ir en minúsculas, no podrán existir atributos que vayan sin valor,...

La definición de [XHTML 1.0][6] pasa a ser bastante estricta para el lenguaje [HTML][3].

<a name="html5"></a>
### HTML5

Una vez publicado [XHTML 1.0][6] los esfuerzos de la W3C se dirigen a la creación de XHTML 2.0 como evolución del lenguaje.

Nuevamente la [W3C][7] se mete en un trabajo teórico, lo que hace que algunos “disidentes” (oportunistas para otros), como Ian Hickson,  monten un grupo paralelo conocido como [WHATWG][8] (Web Hypertext Application Technology Working Group) que empieza a trabajar en [HTML5][9] el 4 junio de 2004.

[HTML5][9] empieza su definición apoyándose en dos puntos. Por un lado la compatibilidad hacía atrás de todo lo que hay creado y por otro la capacidad de absorber todas las funcionalidades que los nuevos fabricantes de la web habían ido construyendo, véase Google, Apple u Opera.

Además [WHATWG][8] siempre ha acusado a la [W3C][7] de tener unos procesos de estandarización muy largos y no alineados a las necesidades del mercado.

Entre las nuevas funcionalidades se encuentran la simplicidad para reproducir audio y vídeo, el disponer de un lienzo de dibujo denominado Canvas,.... Además alrededor de [HTML5][9] nacen una gran cantidad de especificaciones para la mejora de las Webapps como son Websockets, Geolocalización, Webstorage,..

La [W3C][7], en 2007, decide aparcar el trabajo realizado con XHTML 2.0 y empezar a trabajar con [HTML5][9]. Si bien el grupo [WHATWG][8] sigue con su trabajo y estudio sobre diferentes API, los cuales irán cayendo en el estándar.

[La especificación de HTML5][10] es publicada oficialmente el 28 de octubre de 2014. Actualmente el [HTML Working Group][11] está trabajando en [el borrador de HTML 5.1][12] *(cuya última actualización es del [10 de marzo de 2016][13]).*

 <a name="next"></a>
### El futuro del HTML: HTML.next

Tanto la [W3C][7] como el [WHATWG][8] están trabajando sobre la evolución del [HTML5][9]. Cada uno a su ritmo.

Es por ello que es posible que muchas de las cosas en las que está trabajando [WHATWG][8] no acaben dentro del estándar [HTML5][9]. Así [un subconjunto del trabajo sobre HTML5 pasará a ser recomendación del W3C y la otra parte pasará para las siguientes versiones][14]. Esto es lo que se ha dado a conocer como [HTML.next][15]

En [HTML.next][15] están [propuestos elementos][16] como RECO, para el reconocimiento de voz, áreas de texto WYSIWYG, DATAGRID para representar datos tabulares, DATA para insertar elementos sólo reconocibles para máquinas,...

 [1]: http://www.w3.org/TR/REC-html40/
 [2]: http://www.manualweb.net/tutorial-css/
 [3]: http://www.manualweb.net/tutorial-html/
 [4]: http://www.manualweb.net/tutorial-xml/
 [5]: http://www.w3.org/TR/1998/REC-xml-19980210
 [6]: http://www.w3.org/TR/xhtml1/
 [7]: http://www.w3.org
 [8]: http://www.whatwg.org/
 [9]: http://www.w3.org/TR/html5/
 [10]: http://www.w3.org/TR/2014/REC-html5-20141028/
 [11]: http://www.w3.org/html/wg/
 [12]: https://www.w3.org/TR/2016/WD-html51-20160310/
 [13]: https://www.w3.org/blog/news/archives/5313
 [14]: http://www.w3.org/QA/2012/07/html5_and_htmlnext.html
 [15]: http://www.w3.org/wiki/HTML/next
 [16]: http://www.w3.org/html/wg/next/markup/
