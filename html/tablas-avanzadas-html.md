---
ID: pdte
post_title: '16.02 &#8211; Tablas Avanzadas en HTML'
author: Víctor Cuervo
post_date: 2017-04-12 19:48
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/tablas-avanzadas-html/
published: false
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-tabla/feed/
gitfolder: html
---
Dentro de las tablas avanzadas en HTML veremos: [TOC]
### Grupos de Filas Ya hemos visto que las tablas se van definiendo por filas mediante el

[elemento tr][1]. Pues dentro de [HTML][2] podemos agrupar estas filas por funcionalidad. Para ello podemos agrupar las filas en tres partes:
*   **Cabecera**, representada por el [elemento thead][3].
*   **Cuerpo**, representada por el [elemento tbody][4].
*   **Pie**, representada por el [elemento tfoot][5]. Cada uno de estos elementos tendrá una o n filas, dependiendo de las que queramos agrupar. La estructura es la misma para los tres casos:

<pre lang="html4strict"><thead>
  <tr>
    <!-- fila(s) -->
  </tr>

</thead></pre>

<pre lang="html4strict"><tbody>
  <tr>
    <!-- fila(s) -->
  </tr>

</tbody></pre>

<pre lang="html4strict"><tfoot>
  <tr>
    <!-- fila(s) -->
  </tr>

</tfoot></pre> Es importante saber que no es necesario que aparezcan en ese orden dentro de la tabla, este podría ser alterados. Si bien el navegador si que las representará en dicho orden. De esta forma podríamos tener la siguiente tabla con agrupaciones:

<pre lang="html4strict"><table>
  <thead>
    <tr>
      &lt;td scope=”row”>Mes&lt;/td>
            <td>
        Enero
      </td>


      <td>
        Febrero
      </td>

    </tr>

  </thead>


  <tfoot>
    <tr>
      <td>
        Total
      </td>


      <td>
        15
      </td>


      <td>
        25
      </td>

    </tr>

  </tfoot>


  <tbody>
    <tr>
      <td>
        Agua
      </td>


      <td>
        10
      </td>


      <td>
        15
      </td>

    </tr>


    <tr>
      <td>
        Gas
      </td>


      <td>
        5
      </td>


      <td>
        10
      </td>

    </tr>

  </tbody>

</table></pre> Que representaría lo siguiente:

<table width="100%" border="1">
  <thead>
    <tr style="background-color:#000;color:#fff;">
      <td scope=”row”>Mes</td> <td>
        Enero
      </td>

      <td>
        Febrero
      </td>
    </tr>
  </thead>

  <tfoot style="background-color:#ccc;">
    <tr>
      <td>
        Total
      </td>

      <td>
        15
      </td>

      <td>
        25
      </td>
    </tr>
  </tfoot>

  <tbody>
    <tr>
      <td>
        Agua
      </td>

      <td>
        10
      </td>

      <td>
        15
      </td>
    </tr>

    <tr>
      <td>
        Gas
      </td>

      <td>
        5
      </td>

      <td>
        10
      </td>
    </tr>
  </tbody>
</table>

### Grupos de columnas Ya hemos visto que las tablas se definen por filas. Pero una de las cosas que nos ofrece

[HTML][2] es la posibilidad de definir, sobre dichas filas, grupos de columnas que tengan una relación semántica entre ellas. Por ejemplo en la siguiente tabla vemos que hay una relación semántica de las columnas relativa a los meses. <table width="100%" border="1">
  <colgroup span="2" width="25%" style="background-color:#e6b8af;"></colgroup> <colgroup span="2" width="25%" style="background-color:#dd7e6b;"></colgroup> <tr>
    <td colspan="2">
      Enero
    </td>

    <td colspan="2">
      Febrero
    </td>
  </tr>

  <tr>
    <td>
      Ingresos
    </td>

    <td>
      Gastos
    </td>

    <td>
      Ingresos
    </td>

    <td>
      Gastos
    </td>
  </tr>

  <tr>
    <td>
      1.000€
    </td>

    <td>
      700€
    </td>

    <td>
      1.100€
    </td>

    <td>
      580€
    </td>
  </tr>

  <tr>
    <td>
      1.800€
    </td>

    <td>
      920€
    </td>

    <td>
      1.750€
    </td>

    <td>
      920€
    </td>
  </tr>
</table> Para poder definir estas relaciones semánticas entre las columnas

[HTML][2] nos ofrece el [elemento colgroup][6]. El [elemento colgroup][6] se define al principio de la tabla y tiene la siguiente estructura. <pre lang="html4strict">&lt;colgroup span=”numero-columnas” width=”ancho”>&lt;/colgroup></pre> Dónde el atributo span indica el número de columnas que representa la agrupación. Empezando de izquierda a derecha. Además contamos con el

[atributo width][7] el cual nos permite especificar un ancho para la columna. En la tabla que hemos visto el código [HTML][2] quedaría de la siguiente forma: <pre lang="html4strict"><table>
  <colgroup span=”2” width=”100”></colgroup>
    <colgroup span=”2” width=”100”></colgroup>
    <tr>
    <td colspan=”2”>Enero</td>
       <td colspan=”2”>Febrero</td>

  </tr>


  <tr>
    <td>
      Ingresos
    </td>


    <td>
      Gastos
    </td>


    <td>
      Ingresos
    </td>


    <td>
      Gastos
    </td>

  </tr>


  <tr>
    <td>
      1.000€
    </td>


    <td>
      700€/td>
          <td>
        1.100€
      </td>


      <td>
        580€
      </td>
        </tr>


      <tr>
        <td>
          1.800€
        </td>


        <td>
          920€
        </td>


        <td>
          1.750€
        </td>


        <td>
          920€
        </td>

      </tr>
      </table></pre>

      Si no queremos utilizar el atributo span o

      <b>si bien queremos manipular los estilos gráficos de las columnas, tenemos otro elemento, este es el </b><a href="http://www.w3api.com/wiki/HTML:COL"><b>elemento col</b></a><b>.</b>

      El <a href="http://www.w3api.com/wiki/HTML:COL">elemento col</a> aparecerá dentro del <a href="http://www.w3api.com/wiki/HTML:COLGROUP">elemento colgroup</a> tantas veces como columnas queramos agrupar.

      La estructura de <a href="http://www.w3api.com/wiki/HTML:COL">elemento col</a> es:

      <pre lang="html4strict">&lt;col span=”numero-columnas” width=”ancho-columna” /></pre>

      Es decir que también permite agrupar columnas mediante su atributo width y darles un ancho mediante el

      <a href="http://www.w3api.com/wiki/HTML:Width">atributo width</a>.

      El anterior ejemplo utilizando el <a href="http://www.w3api.com/wiki/HTML:COL">elemento col</a> quedaría de la siguiente forma:

      <pre lang="html4strict"><table>
  <colgroup>
      <col width=”100”>
      <col width=”100”>
    </colgroup>
    <colgroup>
      <col width=”100”>
      <col width=”100”>
    </colgroup>
    <tr>
    <td colspan=”2”>Enero</td>
        <td colspan=”2”>Febrero</td>

  </tr>


  <tr>
    <td>
      Ingresos
    </td>


    <td>
      Gastos
    </td>


    <td>
      Ingresos
    </td>


    <td>
      Gastos
    </td>

  </tr>


  <tr>
    <td>
      1.000€
    </td>


    <td>
      700€/td>
          <td>
        1.100€
      </td>


      <td>
        580€
      </td>
        </tr>


      <tr>
        <td>
          1.800€
        </td>


        <td>
          920€
        </td>


        <td>
          1.750€
        </td>


        <td>
          920€
        </td>

      </tr>
      </table></pre>



      <h3>
        Tablas para agentes de usuario no visuales
      </h3>
      Las tablas no siempre serán representadas por un navegador web o agente de usuario visual. Hay otro tipo de agentes de usuario que son no visuales y que suelen estar adaptados para discapacitados.



      <h4>
        Asociar celdas a cabeceras
      </h4>
      En este sentido tenemos que saber cómo dar formato a las tablas para que estos agentes de usuario no visuales puedan interpretar la información de forma correcta.

      El elemento sobre el que nos podemos apoyar es el atributo header. El atributo header relaciona una celda con una celda de la cabecera, para poder establecer esta relación semántica.

      Partamos de la siguiente tabla...



      <table width="100%" border="1">
        <tr>
          <td>
            Nombre
          </td>


          <td>
            Edad
          </td>


          <td>
            Localidad
          </td>

        </tr>


        <tr>
          <td>
            Víctor
          </td>


          <td>
            38
          </td>


          <td>
            Madrid
          </td>

        </tr>


        <tr>
          <td>
            Esther
          </td>


          <td>
            25
          </td>


          <td>
            Salamanca
          </td>

        </tr>

      </table>

      Para ello lo primero que hay que hacer es darle un

      <a href="http://www.w3api.com/wiki/HTML:Id">atributo id</a> a las celdas de cabecera.

      <pre lang="html4strict"><tr>
  &lt;th id=”nombre”>Nombre&lt;/th>
    &lt;th id=”edad”>Edad&lt;/th>
    &lt;th id=”localidad”>Localidad&lt;/th>

</tr></pre>

      Ahora, para cada celda deberemos de asociar el identificador,

      <a href="http://www.w3api.com/wiki/HTML:Id">atributo id</a>, de la cabecera que les aplique en el atributo headers.

      <pre lang="html4strict"><tr>
  &lt;th headers=”nombre”>Víctor&lt;/th>
    &lt;th headers=”edad”>38&lt;/th>
    &lt;th headers=”localidad”>Madrid&lt;/th>

</tr>


<tr>
  &lt;th headers=”nombre”>Esther&lt;/th>
    &lt;th headers=”edad”>25&lt;/th>
    &lt;th headers=”localidad”>Salamanca&lt;/th>

</tr></pre>

      Así, el agente de usuario no visual, cuando vaya leyendo la fila hará lo siguiente:



      <pre>“Nombre, Víctor. Edad, 38. Localidad, Madrid.
Nombre, Esther. Edad, 25. Localidad, Salamanca.”</pre>



      <h4>
        Categorizar Celdas
      </h4>
      Otra de las cosas que podemos hacer para los agentes de usuario no visuales es categorizar las celdas. En

      <a href="http://www.manualweb.net/tutorial-html/">HTML</a> tenemos un atributo que es axis, de esta manera podemos establecer ejes de agrupación.

      El <b>atributo axis</b> aplica a las <a href="http://www.w3api.com/wiki/HTML:TD">celdas td</a> y celdas de <a href="http://www.w3api.com/wiki/HTML:TH">cabecera th</a>. Y permite darle una categoría textual.

      La estructura sería:

      <pre lang="html4strict">&lt;td axis=”categoria”>...&lt;/td></pre>



      <table width="100%" border="1">
        <tr style="background-color:#ccc;">
          <td>

          </td>


          <td>
            Comida
          </td>


          <td>
            Hotel
          </td>


          <td>
            Transporte
          </td>

        </tr>


        <tr style="background-color:#b1b1b1;">
          <td>
            Madrid
          </td>


          <td>

          </td>


          <td>

          </td>


          <td>

          </td>

        </tr>


        <tr>
          <td style="background-color:#ccc;">
            1 de marzo
          </td>


          <td>
            15
          </td>


          <td>
            120
          </td>


          <td>
            -
          </td>

        </tr>


        <tr>
          <td style="background-color:#ccc;">
            2 de marzo
          </td>


          <td>
            18
          </td>


          <td>
            120
          </td>


          <td>
            34
          </td>

        </tr>


        <tr>
          <td style="background-color:#ccc;">
            3 de marzo
          </td>


          <td>
            25
          </td>


          <td>
            120
          </td>


          <td>
            -
          </td>

        </tr>


        <tr style="background-color:#b1b1b1;">
          <td>
            Ávila
          </td>


          <td>

          </td>


          <td>

          </td>


          <td>

          </td>

        </tr>


        <tr>
          <td style="background-color:#ccc;">
            4 de marzo
          </td>


          <td>
            10
          </td>


          <td>
            75
          </td>


          <td>
            12
          </td>

        </tr>


        <tr>
          <td style="background-color:#ccc;">
            5 de marzo
          </td>


          <td>
            12
          </td>


          <td>
            75
          </td>


          <td>
            14
          </td>

        </tr>

      </table>

      En esta tabla podemos establecer que haya 3 tipos de categorías. Los gastos (comida, hotel y transporte), las ciudades (Madrid y Ávila) y las fechas.

      Así que deberemos de marcar esas celdas con la categoría correspondiente, mediante el atributo axis. El código en

      <a href="http://www.manualweb.net/tutorial-html/">HTML</a> nos quedará de la siguiente forma:

      <pre lang="html4strict"><table>
  <tr>
    <th>

    </th>
        &lt;th axis=”gasto”>Comida&lt;/th>
        &lt;th axis=”gasto”>Hotel&lt;/th>
        &lt;th axis=”gasto”>Transporte&lt;/th>

  </tr>


  <tr>
    &lt;td axis=”ciudad”>Madrid&lt;/td>
        <td>

    </td>


    <td>

    </td>


    <td>

    </td>

  </tr>


  <tr>
    &lt;td axis=”fecha”>1 de marzo&lt;/td>
        <td>
      15
    </td>


    <td>
      120
    </td>


    <td>
      -
    </td>

  </tr>


  <tr>
    &lt;td axis=”fecha”>2 de marzo&lt;/td>
        <td>
      18
    </td>


    <td>
      120
    </td>


    <td>
      34
    </td>

  </tr>


  <tr>
    &lt;td axis=”fecha”>3 de marzo&lt;/td>
        <td>
      25
    </td>


    <td>
      120
    </td>


    <td>
      -
    </td>

  </tr>


  <tr>
    &lt;td axis=”ciudad”>Avila&lt;/td>
        <td>

    </td>


    <td>

    </td>


    <td>

    </td>

  </tr>


  <tr>
    &lt;td axis=”fecha”>4 de marzo&lt;/td>
        <td>
      10
    </td>


    <td>
      75
    </td>


    <td>
      12
    </td>

  </tr>


  <tr>
    &lt;td axis=”fecha”>5 de marzo&lt;/td>
        <td>
      12
    </td>


    <td>
      75
    </td>


    <td>
      14
    </td>

  </tr>

</table></pre>

      El atributo axis se combina con el atributo headers para poder dar suficiente información a los agentes de usuario no visuales sobre las tablas.


      <h3>
        Anchos de las tablas y columnas
      </h3>
      Aunque el formato de las tablas, tanto para la tabla en sí, como para sus filas y celdas se hará mediante

      <a href="http://www.manualweb.net/tutorial-css/">hojas de estilo CSS</a>, tenemos dos formas básicas de poder establecer el ancho de la tabla y el ancho de las columnas.

      En primer lugar podemos utilizar el <a href="http://www.w3api.com/wiki/HTML:Width">atributo width</a> del <a href="http://www.w3api.com/wiki/HTML:TABLE">elemento table</a>.

      <pre lang="html4strict">&lt;table width=”ancho”>...&lt;/table></pre>

      De esta forma podremos establecer en cualquier medida el ancho que queremos que ocupe la tabla. Ya sean px, em, tantos por ciento,...

      Por ejemplo podemos definir que ocupe todo el ancho de una página asignándole un valor de width del 100%.



      <pre lang="html4strict">&lt;table width=”100%”>...&lt;/table></pre>

      Para el caso de las columnas ya hemos visto que tanto los elementos

      <a href="http://www.w3api.com/wiki/HTML:COLGROUP">colgroup</a> como <a href="http://www.w3api.com/wiki/HTML:COL">col</a> también tenían el <a href="http://www.w3api.com/wiki/HTML:Width">atributo width</a>. Así que serán con estos elemento con los que de forma básica podamos establecer el ancho de una columna.

      De esta forma si tenemos 4 columnas y queremos que se distribuyan de forma igual, podríamos escribir el siguiente código.

      <pre lang="html4strict"><table>
  &lt;colgroup span=”4” width=”25%”>
  ....

</table></pre>

 [1]: http://www.w3api.com/wiki/HTML:TR
 [2]: http://www.manualweb.net/tutorial-html/
 [3]: http://www.w3api.com/wiki/HTML:THEAD
 [4]: http://www.w3api.com/wiki/HTML:TBODY
 [5]: http://www.w3api.com/wiki/HTML:TFOOT
 [6]: http://www.w3api.com/wiki/HTML:COLGROUP
 [7]: http://www.w3api.com/wiki/HTML:Width
