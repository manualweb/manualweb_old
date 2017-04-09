---
ID: 280
post_title: Introducción a XSLT
author: Víctor Cuervo
post_date: 2010-05-29 00:23:26
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/xslt/introduccion-a-xslt/
published: true
nombreforo:
  - XSLT
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/extensible-stylesheet-language-transformations-xslt
---
<!--TOC-->

### Qué es XSLT

[XSLT][1] o [XSL Transformations][1] es la parte más importante del lenguaje [XSL (eXtensible StyleSheet Language)][2]. La función de [XSLT][1] es la de transformar documentos [XML][3] en documentos [XHTML][4] u otros documentos [XML][3]. El W3C es el encargado de la definición de especificación [XSLT][1]. [XSLT][1] se basa en XPath para realizar la búsqueda de información a través del documento [XML][3]. XPath son cadenas que son expresiones regulares, las cuales hacen referencia a alguna estructura dentro del documento [XML][3]. El proceso de transformación se basa en plantillas. Dichas plantillas identifican una estructura a partir de la cual realizar la transformación (con XPath), así como las acciones a realizar con dicha estructura: recorrerla, obtener el dato de la etiqueta, el valor de alguno de sus atributos, contar cuantos elementos tiene la etiqueta anidados,... Además, para poder aplicar las transformaciones, necesitaremos asociar el documento de transformación al documento [XML][3] receptor de la misma. Antes de empezar a aprender más cosas sobre [XSLT][1] sería recomendable que tuvieses algún conocimiento sobre [XML][3]. 
### HTML versus XML+XSLT A diferencia del lenguaje 

[HTML][5], donde cada una de sus etiquetas lleva asociada una representación gráfica, el [XML][3] identifica datos, los cuales no tienen representación gráfica asociada. Cuando definimos una tabla en [HTML][5] (la etiqueta [table][6]), sabemos que las herramientas que interpreten el documento [HTML][5], normalmente los navegadores web, pintarán la tabla. De una forma u otra visualizaremos la tabla en nuestra pantalla. Si bien, si tenemos un documento [XML][3], donde podemos tener definida la etiqueta <libro>, está no tendrá ninguna representación gráfica asociada. Es por ello que si visualizamos nuestro documento [XML][3] con alguna herramienta, esta, mostrará el contenido de la etiqueta, pero sin ninguna representación. Es en este punto donde entra el lenguaje [XSLT][1]. Y es que este lenguaje permite transformar el susodicho documento [XML][3] en otro formato, el resultado de la transformación será el que lleve la representación gráfica. 
### Ejemplos de transformaciones Así, podemos tener múltiples transformaciones del documento 

[XML][3] en otros documentos de distintos lenguajes: [XHTML][4], [SVG][7], [VRML][8],... Por ejemplo, un documento [XML][3] que tuviese una lista de números podría ser transformado en: una tabla o lista de hitos con dicho listado en [HTML][5], en un gráfico de líneas con [SVG][7] o podrían ser las alturas de figuras 3D con [VRML][8]. Veamos cómo serían dichas transformaciones: 
#### XML original

<pre>2
 4
 6
 8</pre>

#### XML transformado en HTML

<pre><table>
  <tbody>
    <tr>
      <th>
        Datos
      </th>
      
    </tr>
    
    
    <tr>
      <td>
        2
      </td>
      
    </tr>
    
    
    <tr>
      <td>
        4
      </td>
      
    </tr>
    
    
    <tr>
      <td>
        6
      </td>
      
    </tr>
    
    
    <tr>
      <td>
        8
      </td>
      
    </tr>
    
  </tbody>
  
</table>
</pre>

#### XML transformado en SVG

#### XML transformado en VRML

<pre>#VRML V2.0 utf8
 Box {
  size 2 4 6
}</pre> En estos ejemplos, vemos que los datos de partida de un documento 

[XML][3] son utilizados como contenido de otros documentos que tienen representaciones gráficas y pasan a ser valores de los mismos. En el documento [HTML][5] son datos de una tabla, en el documento [SVG][7] son las coordenadas de una línea y en el documento [VRML][8] son las dimensiones de un cubo.

 [1]: http://www.manualweb.net/tutorial-xslt/ "XSLT"
 [2]: http://www.manualweb.net/tutorial-xsl/ "XSL"
 [3]: http://www.manualweb.net/tutorial-xml/ "XML"
 [4]: http://www.manualweb.net/tutorial-xhtml/ "xhtml"
 [5]: http://www.manualweb.net/tutorial-html/ "HTML"
 [6]: http://w3api.com/wiki/HTML:TABLE "Table"
 [7]: http://www.manualweb.net/tutorial-svg/ "svg"
 [8]: http://www.manualweb.net/tutorial-vrml/ "VRML"