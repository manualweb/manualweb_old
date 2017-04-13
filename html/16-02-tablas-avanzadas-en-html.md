---
ID: 1412
post_title: 16.02 – Tablas Avanzadas en HTML
author: Víctor Cuervo
post_date: 2017-04-12 19:19:13
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/tablas-avanzadas-en-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-tabla/feed/
gitfolder: html
---
Dentro de las tablas avanzadas en HTML veremos:

[TOC]

### Grupos de Filas

Ya hemos visto que las tablas se van definiendo por filas mediante el [elemento tr][1]. Pues dentro de [HTML][2] podemos agrupar estas filas por funcionalidad.

Para ello podemos agrupar las filas en tres partes:

* **Cabecera**, representada por el [elemento thead][3].
* **Cuerpo**, representada por el [elemento tbody][4].
* **Pie**, representada por el [elemento tfoot][5].

Cada uno de estos elementos tendrá una o n filas, dependiendo de las que queramos agrupar. La estructura es la misma para los tres casos:

~~~html
<thead>
  <tr> <!-- fila(s) --></tr>
</thead>

<tbody>
  <tr> <!-- fila(s) --></tr>
</tbody>

<tfoot>
  <tr> <!-- fila(s) --></tr>
</tfoot>
~~~

Es importante saber que no es necesario que aparezcan en ese orden dentro de la tabla, este podría ser alterados. Si bien el navegador si que las representará en dicho orden.

De esta forma podríamos tener la siguiente tabla con agrupaciones:

~~~html
<table>
  <thead>
    <tr>
	<td scope=”row”>Mes</td>
      <td>Enero</td>
      <td>Febrero</td>
    </tr>
  </thead>
  <tfoot>
    <tr>
	<td>Total</td>
      <td>15</td>
      <td>25</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
	<td>Agua</td>
      <td>10</td>
      <td>15</td>
    </tr>
    <tr>
	<td>Gas</td>
      <td>5</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
~~~

Que representaría lo siguiente:

<table style="border: 1px solid black; width:100%">
  <thead>
    <tr style="background-color:#000;color:#fff">
      <td scope="”row”">
        Mes
      </td>

      <td>
        Enero
      </td>

      <td>
        Febrero
      </td>
    </tr>
  </thead>

  <tfoot style="background-color:#ccc">
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

### Grupos de columnas
Ya hemos visto que las tablas se definen por filas. Pero una de las cosas que nos ofrece [HTML][2] es la posibilidad de definir, sobre dichas filas, grupos de columnas que tengan una relación semántica entre ellas.

Por ejemplo en la siguiente tabla vemos que hay una relación semántica de las columnas relativa a los meses.

<table style="border: 1px solid black; width:100%">
  <colgroup span="2" width="25%" style="background-color:#e6b8af"></colgroup> <colgroup span="2" width="25%" style="background-color:#dd7e6b"></colgroup> <tr>
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
</table>

Para poder definir estas relaciones semánticas entre las columnas [HTML][2] nos ofrece el [elemento colgroup][6].

El [elemento colgroup][6] se define al principio de la tabla y tiene la siguiente estructura.

~~~html
<colgroup span=”numero-columnas” width=”ancho”></colgroup>
~~~

Dónde el atributo span indica el número de columnas que representa la agrupación. Empezando de izquierda a derecha. Además contamos con el

[atributo width][7] el cual nos permite especificar un ancho para la columna. En la tabla que hemos visto el código [HTML][2] quedaría de la siguiente forma:

<pre><table>
  <colgroup span="”2”" width="”100”"></colgroup>
        <colgroup span="”2”" width="”100”"></colgroup>
        <tr>
    <td colspan="”2”">
      Enero

    </td>




    <td colspan="”2”">
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



      <pre><code>  &lt;pre&gt;&lt;code&gt;  Si no queremos utilizar el atributo span o
</code></pre>



      <p>
        <b>si bien queremos manipular los estilos gráficos de las columnas, tenemos otro elemento, este es el </b><a href="http://www.w3api.com/wiki/HTML:COL"><b>elemento col</b></a><b>.</b>
      </p>



      <p>
        El <a href="http://www.w3api.com/wiki/HTML:COL">elemento col</a> aparecerá dentro del <a href="http://www.w3api.com/wiki/HTML:COLGROUP">elemento colgroup</a> tantas veces como columnas queramos agrupar.
      </p>



      <p>
        La estructura de <a href="http://www.w3api.com/wiki/HTML:COL">elemento col</a> es:
      </p>



      <p>
        <pre lang="html4strict"><col span=”numero-columnas” width=”ancho-columna” /></pre>
      </p>



      <p>
        Es decir que también permite agrupar columnas mediante su atributo width y darles un ancho mediante el
      </p>



      <p>
        <a href="http://www.w3api.com/wiki/HTML:Width">atributo width</a>.
      </p>



      <p>
        El anterior ejemplo utilizando el <a href="http://www.w3api.com/wiki/HTML:COL">elemento col</a> quedaría de la siguiente forma:
      </p>



      <p>
        <pre lang="html4strict"><table>
        </code></pre>
      </p>



      <pre><code>  &lt;p&gt;
    &lt;colgroup&gt;
          &lt;col width="”100”"&gt;
          &lt;col width="”100”"&gt;
        &lt;/colgroup&gt;
        &lt;colgroup&gt;
          &lt;col width="”100”"&gt;
          &lt;col width="”100”"&gt;
        &lt;/colgroup&gt;
        &lt;tr&gt;
      &lt;td colspan="”2”"&gt;
        Enero
      &lt;/td&gt;


      &lt;td colspan="”2”"&gt;
        Febrero
      &lt;/td&gt;&lt;/p&gt;



      &lt;p&gt;
        &lt;/tr&gt;
      &lt;/p&gt;



      &lt;p&gt;
        &lt;tr&gt;
          &lt;td&gt;
            Ingresos

          &lt;/td&gt;&lt;/p&gt;



          &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        Gastos
        </td>
      </p>



      <p>
        <td>
          Ingresos
        </td>
      </p>



      <p>
        <td>
          Gastos
        </td>
        </code></pre>
      </p>



      <pre><code>          &lt;p&gt;
            &lt;/tr&gt;
          &lt;/p&gt;



          &lt;p&gt;
            &lt;tr&gt;
              &lt;td&gt;
                1.000€

              &lt;/td&gt;&lt;/p&gt;



              &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        700€/td>
              <td>
            1.100€
          </td>
      </p>



      <p>
        <td>
            580€
          </td>
            </tr>
      </p>



      <p>
        <tr>
            <td>
              1.800€
            </td>
      </p>



      <pre><code>&lt;td&gt;
  920€
&lt;/td&gt;


&lt;td&gt;
  1.750€
&lt;/td&gt;


&lt;td&gt;
  920€
&lt;/td&gt;
</code></pre>



      <p>
        </tr>
          </table></pre>
      </p>



      <p>
        <h3>
            Tablas para agentes de usuario no visuales
          </h3>
          Las tablas no siempre serán representadas por un navegador web o agente de usuario visual. Hay otro tipo de agentes de usuario que son no visuales y que suelen estar adaptados para discapacitados.
      </p>



      <p>
        <h4>
            Asociar celdas a cabeceras
          </h4>
          En este sentido tenemos que saber cómo dar formato a las tablas para que estos agentes de usuario no visuales puedan interpretar la información de forma correcta.
      </p>



      <p>
        El elemento sobre el que nos podemos apoyar es el atributo header. El atributo header relaciona una celda con una celda de la cabecera, para poder establecer esta relación semántica.
      </p>



      <p>
        Partamos de la siguiente tabla...
      </p>



      <p>
        <table width="100%" border="1">
            <tr>
              <td>
                Nombre
              </td>
      </p>



      <pre><code>  &lt;td&gt;
    Edad
  &lt;/td&gt;


  &lt;td&gt;
    Localidad
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td&gt;
    Víctor
  &lt;/td&gt;


  &lt;td&gt;
    38
  &lt;/td&gt;


  &lt;td&gt;
    Madrid
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td&gt;
    Esther
  &lt;/td&gt;


  &lt;td&gt;
    25
  &lt;/td&gt;


  &lt;td&gt;
    Salamanca
  &lt;/td&gt;

&lt;/tr&gt;
</code></pre>



      <p>
        </table>
      </p>



      <p>
        Para ello lo primero que hay que hacer es darle un
      </p>



      <p>
        <a href="http://www.w3api.com/wiki/HTML:Id">atributo id</a> a las celdas de cabecera.
      </p>



      <p>
        <pre lang="html4strict"><tr>
        </code></pre>
      </p>



      <pre><code>              &lt;p&gt;
                &lt;th id=”nombre”&gt;Nombre&lt;/th&gt;
                    &lt;th id=”edad”&gt;Edad&lt;/th&gt;
                    &lt;th id=”localidad”&gt;Localidad&lt;/th&gt;
              &lt;/p&gt;



              &lt;p&gt;
                &lt;/tr&gt;&lt;/pre&gt;
              &lt;/p&gt;



              &lt;pre&gt;&lt;code&gt;  Ahora, para cada celda deberemos de asociar el identificador,
</code></pre>



      <p>
        <a href="http://www.w3api.com/wiki/HTML:Id">atributo id</a>, de la cabecera que les aplique en el atributo headers.
      </p>



      <p>
        <pre lang="html4strict"><tr>
        </code></pre>
      </p>



      <pre><code>              &lt;p&gt;
                &lt;th headers=”nombre”&gt;Víctor&lt;/th&gt;
                    &lt;th headers=”edad”&gt;38&lt;/th&gt;
                    &lt;th headers=”localidad”&gt;Madrid&lt;/th&gt;
              &lt;/p&gt;



              &lt;p&gt;
                &lt;/tr&gt;
              &lt;/p&gt;



              &lt;p&gt;
                &lt;tr&gt;
                  &lt;th headers=”nombre”&gt;Esther&lt;/th&gt;
                      &lt;th headers=”edad”&gt;25&lt;/th&gt;
                      &lt;th headers=”localidad”&gt;Salamanca&lt;/th&gt;&lt;/p&gt;

                  &lt;p&gt;
                    &lt;/tr&gt;&lt;/pre&gt;
                  &lt;/p&gt;



                  &lt;pre&gt;&lt;code&gt;  Así, el agente de usuario no visual, cuando vaya leyendo la fila hará lo siguiente:
</code></pre>



      <p>
        <pre>“Nombre, Víctor. Edad, 38. Localidad, Madrid.
        </code></pre>
      </p>



      <pre><code>                  &lt;p&gt;
                    Nombre, Esther. Edad, 25. Localidad, Salamanca.”&lt;/pre&gt;
                  &lt;/p&gt;



                  &lt;pre&gt;&lt;code&gt;  &lt;h4&gt;
Categorizar Celdas
</code></pre>



      <p>
        </h4>
          Otra de las cosas que podemos hacer para los agentes de usuario no visuales es categorizar las celdas. En
      </p>



      <p>
        <a href="http://www.manualweb.net/tutorial-html/">HTML</a> tenemos un atributo que es axis, de esta manera podemos establecer ejes de agrupación.
      </p>



      <p>
        El <b>atributo axis</b> aplica a las <a href="http://www.w3api.com/wiki/HTML:TD">celdas td</a> y celdas de <a href="http://www.w3api.com/wiki/HTML:TH">cabecera th</a>. Y permite darle una categoría textual.
      </p>



      <p>
        La estructura sería:
      </p>



      <p>
        <pre lang="html4strict"><td axis=”categoria”>...</td></pre>
      </p>



      <p>
        <table width="100%" border="1">
            <tr style="background-color:#ccc;">
              <td>
      </p>



      <pre><code>  &lt;/td&gt;


  &lt;td&gt;
    Comida
  &lt;/td&gt;


  &lt;td&gt;
    Hotel
  &lt;/td&gt;


  &lt;td&gt;
    Transporte
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr style="background-color:#b1b1b1;"&gt;
  &lt;td&gt;
    Madrid
  &lt;/td&gt;


  &lt;td&gt;

  &lt;/td&gt;


  &lt;td&gt;

  &lt;/td&gt;


  &lt;td&gt;

  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td style="background-color:#ccc;"&gt;
    1 de marzo
  &lt;/td&gt;


  &lt;td&gt;
    15
  &lt;/td&gt;


  &lt;td&gt;
    120
  &lt;/td&gt;


  &lt;td&gt;
    -
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td style="background-color:#ccc;"&gt;
    2 de marzo
  &lt;/td&gt;


  &lt;td&gt;
    18
  &lt;/td&gt;


  &lt;td&gt;
    120
  &lt;/td&gt;


  &lt;td&gt;
    34
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td style="background-color:#ccc;"&gt;
    3 de marzo
  &lt;/td&gt;


  &lt;td&gt;
    25
  &lt;/td&gt;


  &lt;td&gt;
    120
  &lt;/td&gt;


  &lt;td&gt;
    -
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr style="background-color:#b1b1b1;"&gt;
  &lt;td&gt;
    Ávila
  &lt;/td&gt;


  &lt;td&gt;

  &lt;/td&gt;


  &lt;td&gt;

  &lt;/td&gt;


  &lt;td&gt;

  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td style="background-color:#ccc;"&gt;
    4 de marzo
  &lt;/td&gt;


  &lt;td&gt;
    10
  &lt;/td&gt;


  &lt;td&gt;
    75
  &lt;/td&gt;


  &lt;td&gt;
    12
  &lt;/td&gt;

&lt;/tr&gt;


&lt;tr&gt;
  &lt;td style="background-color:#ccc;"&gt;
    5 de marzo
  &lt;/td&gt;


  &lt;td&gt;
    12
  &lt;/td&gt;


  &lt;td&gt;
    75
  &lt;/td&gt;


  &lt;td&gt;
    14
  &lt;/td&gt;

&lt;/tr&gt;
</code></pre>



      <p>
        </table>
      </p>



      <p>
        En esta tabla podemos establecer que haya 3 tipos de categorías. Los gastos (comida, hotel y transporte), las ciudades (Madrid y Ávila) y las fechas.
      </p>



      <p>
        Así que deberemos de marcar esas celdas con la categoría correspondiente, mediante el atributo axis. El código en
      </p>



      <p>
        <a href="http://www.manualweb.net/tutorial-html/">HTML</a> nos quedará de la siguiente forma:
      </p>



      <p>
        <pre lang="html4strict"><table>
        </code></pre>
      </p>



      <pre><code>                  &lt;p&gt;
                    &lt;tr&gt;
                      &lt;th&gt;
                        &lt;/p&gt;

                        &lt;pre&gt;&lt;code&gt;&lt;/th&gt;
&lt;th axis=”gasto”&gt;Comida&lt;/th&gt;
&lt;th axis=”gasto”&gt;Hotel&lt;/th&gt;
&lt;th axis=”gasto”&gt;Transporte&lt;/th&gt;
</code></pre>



      <p>
        </code></pre>
      </p>



      <pre><code>                        &lt;p&gt;
                          &lt;/tr&gt;
                        &lt;/p&gt;



                        &lt;p&gt;
                          &lt;tr&gt;
                            &lt;td axis=”ciudad”&gt;Madrid&lt;/td&gt;
                                    &lt;td&gt;
                              &lt;/p&gt;

                              &lt;pre&gt;&lt;code&gt;&lt;/td&gt;
</code></pre>



      <p>
        <td>
      </p>



      <p>
        </td>
      </p>



      <p>
        <td>
      </p>



      <p>
        </td>
        </code></pre>
      </p>



      <pre><code>                              &lt;p&gt;
                                &lt;/tr&gt;
                              &lt;/p&gt;



                              &lt;p&gt;
                                &lt;tr&gt;
                                  &lt;td axis=”fecha”&gt;1 de marzo&lt;/td&gt;
                                          &lt;td&gt;
                                    15

                                  &lt;/td&gt;&lt;/p&gt;



                                  &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        120
        </td>
      </p>



      <p>
        <td>
          -
        </td>
        </code></pre>
      </p>



      <pre><code>                                  &lt;p&gt;
                                    &lt;/tr&gt;
                                  &lt;/p&gt;



                                  &lt;p&gt;
                                    &lt;tr&gt;
                                      &lt;td axis=”fecha”&gt;2 de marzo&lt;/td&gt;
                                              &lt;td&gt;
                                        18

                                      &lt;/td&gt;&lt;/p&gt;



                                      &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        120
        </td>
      </p>



      <p>
        <td>
          34
        </td>
        </code></pre>
      </p>



      <pre><code>                                      &lt;p&gt;
                                        &lt;/tr&gt;
                                      &lt;/p&gt;



                                      &lt;p&gt;
                                        &lt;tr&gt;
                                          &lt;td axis=”fecha”&gt;3 de marzo&lt;/td&gt;
                                                  &lt;td&gt;
                                            25

                                          &lt;/td&gt;&lt;/p&gt;



                                          &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        120
        </td>
      </p>



      <p>
        <td>
          -
        </td>
        </code></pre>
      </p>



      <pre><code>                                          &lt;p&gt;
                                            &lt;/tr&gt;
                                          &lt;/p&gt;



                                          &lt;p&gt;
                                            &lt;tr&gt;
                                              &lt;td axis=”ciudad”&gt;Avila&lt;/td&gt;
                                                      &lt;td&gt;
                                                &lt;/p&gt;

                                                &lt;pre&gt;&lt;code&gt;&lt;/td&gt;
</code></pre>



      <p>
        <td>
      </p>



      <p>
        </td>
      </p>



      <p>
        <td>
      </p>



      <p>
        </td>
        </code></pre>
      </p>



      <pre><code>                                                &lt;p&gt;
                                                  &lt;/tr&gt;
                                                &lt;/p&gt;



                                                &lt;p&gt;
                                                  &lt;tr&gt;
                                                    &lt;td axis=”fecha”&gt;4 de marzo&lt;/td&gt;
                                                            &lt;td&gt;
                                                      10

                                                    &lt;/td&gt;&lt;/p&gt;



                                                    &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        75
        </td>
      </p>



      <p>
        <td>
          12
        </td>
        </code></pre>
      </p>



      <pre><code>                                                    &lt;p&gt;
                                                      &lt;/tr&gt;
                                                    &lt;/p&gt;



                                                    &lt;p&gt;
                                                      &lt;tr&gt;
                                                        &lt;td axis=”fecha”&gt;5 de marzo&lt;/td&gt;
                                                                &lt;td&gt;
                                                          12

                                                        &lt;/td&gt;&lt;/p&gt;



                                                        &lt;pre&gt;&lt;code&gt;&lt;td&gt;
</code></pre>



      <p>
        75
        </td>
      </p>



      <p>
        <td>
          14
        </td>
        </code></pre>
      </p>



      <pre><code>                                                        &lt;p&gt;
                                                          &lt;/tr&gt;
                                                        &lt;/p&gt;



                                                        &lt;p&gt;
                                                          &lt;/table&gt;&lt;/pre&gt;
                                                        &lt;/p&gt;



                                                        &lt;pre&gt;&lt;code&gt;  El atributo axis se combina con el atributo headers para poder dar suficiente información a los agentes de usuario no visuales sobre las tablas.
</code></pre>



      <p>
        <h3>
            Anchos de las tablas y columnas
          </h3>
          Aunque el formato de las tablas, tanto para la tabla en sí, como para sus filas y celdas se hará mediante
      </p>



      <p>
        <a href="http://www.manualweb.net/tutorial-css/">hojas de estilo CSS</a>, tenemos dos formas básicas de poder establecer el ancho de la tabla y el ancho de las columnas.
      </p>



      <p>
        En primer lugar podemos utilizar el <a href="http://www.w3api.com/wiki/HTML:Width">atributo width</a> del <a href="http://www.w3api.com/wiki/HTML:TABLE">elemento table</a>.
      </p>



      <p>
        <pre lang="html4strict"><table width=”ancho”>...</table></pre>
      </p>



      <p>
        De esta forma podremos establecer en cualquier medida el ancho que queremos que ocupe la tabla. Ya sean px, em, tantos por ciento,...
      </p>



      <p>
        Por ejemplo podemos definir que ocupe todo el ancho de una página asignándole un valor de width del 100%.
      </p>



      <p>
        <pre lang="html4strict"><table width=”100%”>...</table></pre>
      </p>



      <p>
        Para el caso de las columnas ya hemos visto que tanto los elementos
      </p>



      <p>
        <a href="http://www.w3api.com/wiki/HTML:COLGROUP">colgroup</a> como <a href="http://www.w3api.com/wiki/HTML:COL">col</a> también tenían el <a href="http://www.w3api.com/wiki/HTML:Width">atributo width</a>. Así que serán con estos elemento con los que de forma básica podamos establecer el ancho de una columna.
      </p>



      <p>
        De esta forma si tenemos 4 columnas y queremos que se distribuyan de forma igual, podríamos escribir el siguiente código.
      </p>



      <p>
        <pre lang="html4strict"><table>
        </code></pre>
      </p>



      <pre><code>                                                        &lt;p&gt;
                                                          &lt;colgroup span=”4” width=”25%”&gt;
                                                            ....
                                                        &lt;/p&gt;



                                                        &lt;p&gt;
                                                          &lt;/table&gt;&lt;/pre&gt;
                                                        &lt;/p&gt;
</code></pre>

 [1]: http://www.w3api.com/wiki/HTML:TR
 [2]: http://www.manualweb.net/tutorial-html/
 [3]: http://www.w3api.com/wiki/HTML:THEAD
 [4]: http://www.w3api.com/wiki/HTML:TBODY
 [5]: http://www.w3api.com/wiki/HTML:TFOOT
 [6]: http://www.w3api.com/wiki/HTML:COLGROUP
 [7]: http://www.w3api.com/wiki/HTML:Width
