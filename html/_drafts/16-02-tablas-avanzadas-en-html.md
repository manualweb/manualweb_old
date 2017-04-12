---
ID: 1412
post_title: '16.02 &#8211; Tablas Avanzadas en HTML'
author: Víctor Cuervo
post_date: 2017-04-12 19:10:57
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1412
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
    http://lineadecodigo.com/tag/html-tabla/feed/
gitfolder:
  - html
---
Dentro de las tablas avanzadas en HTML veremos: [TOC]

### Grupos de Filas Ya hemos visto que las tablas se van definiendo por filas mediante el

[elemento tr][1]. Pues dentro de [HTML][2] podemos agrupar estas filas por funcionalidad. Para ello podemos agrupar las filas en tres partes: * **Cabecera**, representada por el [elemento thead][3]. * **Cuerpo**, representada por el [elemento tbody][4]. * **Pie**, representada por el [elemento tfoot][5]. Cada uno de estos elementos tendrá una o n filas, dependiendo de las que queramos agrupar. La estructura es la misma para los tres casos:

<pre><thead>
  <tr>
    <!-- fila(s) -->
      
  </tr>
  
  
</thead></pre>

<pre><tbody>
  <tr>
    <!-- fila(s) -->
      
  </tr>
  
  
</tbody></pre>

<pre><tfoot>
  <tr>
    <!-- fila(s) -->
      
  </tr>
  
  
</tfoot></pre>

Es importante saber que no es necesario que aparezcan en ese orden dentro de la tabla, este podría ser alterados. Si bien el navegador si que las representará en dicho orden. De esta forma podríamos tener la siguiente tabla con agrupaciones:

<pre><table>
  <thead>
    <tr>
      &lt;td scope=”row”&gt;Mes&lt;/td&gt;
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
  
  
</table></pre>

Que representaría lo siguiente:

<table width="100%" border="1">
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

### Grupos de columnas Ya hemos visto que las tablas se definen por filas. Pero una de las cosas que nos ofrece

[HTML][2] es la posibilidad de definir, sobre dichas filas, grupos de columnas que tengan una relación semántica entre ellas. Por ejemplo en la siguiente tabla vemos que hay una relación semántica de las columnas relativa a los meses.

<table width="100%" border="1">
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

Para poder definir estas relaciones semánticas entre las columnas

[HTML][2] nos ofrece el [elemento colgroup][6]. El [elemento colgroup][6] se define al principio de la tabla y tiene la siguiente estructura.

<pre>&lt;colgroup span=”numero-columnas” width=”ancho”&gt;&lt;/colgroup&gt;</pre>

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
      
      
      
      <pre><code>  Si no queremos utilizar el atributo span o

  &lt;b&gt;si bien queremos manipular los estilos gráficos de las columnas, tenemos otro elemento, este es el &lt;/b&gt;&lt;a href="http://www.w3api.com/wiki/HTML:COL"&gt;&lt;b&gt;elemento col&lt;/b&gt;&lt;/a&gt;&lt;b&gt;.&lt;/b&gt;

  El &lt;a href="http://www.w3api.com/wiki/HTML:COL"&gt;elemento col&lt;/a&gt; aparecerá dentro del &lt;a href="http://www.w3api.com/wiki/HTML:COLGROUP"&gt;elemento colgroup&lt;/a&gt; tantas veces como columnas queramos agrupar.

  La estructura de &lt;a href="http://www.w3api.com/wiki/HTML:COL"&gt;elemento col&lt;/a&gt; es:

  &lt;pre lang="html4strict"&gt;&lt;col span=”numero-columnas” width=”ancho-columna” /&gt;&lt;/pre&gt;

  Es decir que también permite agrupar columnas mediante su atributo width y darles un ancho mediante el

  &lt;a href="http://www.w3api.com/wiki/HTML:Width"&gt;atributo width&lt;/a&gt;.

  El anterior ejemplo utilizando el &lt;a href="http://www.w3api.com/wiki/HTML:COL"&gt;elemento col&lt;/a&gt; quedaría de la siguiente forma:

  &lt;pre lang="html4strict"&gt;&lt;table&gt;
</code></pre>
      
      
      
      <p>
        <colgroup>
              <col width="”100”">
              <col width="”100”">
            </colgroup>
            <colgroup>
              <col width="”100”">
              <col width="”100”">
            </colgroup>
            <tr>
          <td colspan="”2”">
            Enero
          </td>
                  
          
          <td colspan="”2”">
            Febrero
          </td></p>
          
          
          
          <p>
            </tr>
          </p>
          
          
          
          <p>
            <tr>
              <td>
                Ingresos
                    
              </td></p>
              
              
              
              <pre><code>&lt;td&gt;
  Gastos
&lt;/td&gt;


&lt;td&gt;
  Ingresos
&lt;/td&gt;


&lt;td&gt;
  Gastos
&lt;/td&gt;
</code></pre>
              
              
              
              <p>
                </tr>
              </p>
              
              
              
              <p>
                <tr>
                  <td>
                    1.000€
                        
                  </td></p>
                  
                  
                  
                  <pre><code>&lt;td&gt;
  700€/td&gt;
      &lt;td&gt;
    1.100€
  &lt;/td&gt;


  &lt;td&gt;
    580€
  &lt;/td&gt;
    &lt;/tr&gt;


  &lt;tr&gt;
    &lt;td&gt;
      1.800€
    &lt;/td&gt;


    &lt;td&gt;
      920€
    &lt;/td&gt;


    &lt;td&gt;
      1.750€
    &lt;/td&gt;


    &lt;td&gt;
      920€
    &lt;/td&gt;

  &lt;/tr&gt;
  &lt;/table&gt;&lt;/pre&gt;



  &lt;h3&gt;
    Tablas para agentes de usuario no visuales
  &lt;/h3&gt;
  Las tablas no siempre serán representadas por un navegador web o agente de usuario visual. Hay otro tipo de agentes de usuario que son no visuales y que suelen estar adaptados para discapacitados.



  &lt;h4&gt;
    Asociar celdas a cabeceras
  &lt;/h4&gt;
  En este sentido tenemos que saber cómo dar formato a las tablas para que estos agentes de usuario no visuales puedan interpretar la información de forma correcta.

  El elemento sobre el que nos podemos apoyar es el atributo header. El atributo header relaciona una celda con una celda de la cabecera, para poder establecer esta relación semántica.

  Partamos de la siguiente tabla...



  &lt;table width="100%" border="1"&gt;
    &lt;tr&gt;
      &lt;td&gt;
        Nombre
      &lt;/td&gt;


      &lt;td&gt;
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

  &lt;/table&gt;

  Para ello lo primero que hay que hacer es darle un

  &lt;a href="http://www.w3api.com/wiki/HTML:Id"&gt;atributo id&lt;/a&gt; a las celdas de cabecera.

  &lt;pre lang="html4strict"&gt;&lt;tr&gt;
</code></pre>
                  
                  
                  
                  <p>
                    <th id=”nombre”>Nombre</th>
                        <th id=”edad”>Edad</th>
                        <th id=”localidad”>Localidad</th>
                  </p>
                  
                  
                  
                  <p>
                    </tr></pre>
                  </p>
                  
                  
                  
                  <pre><code>  Ahora, para cada celda deberemos de asociar el identificador,

  &lt;a href="http://www.w3api.com/wiki/HTML:Id"&gt;atributo id&lt;/a&gt;, de la cabecera que les aplique en el atributo headers.

  &lt;pre lang="html4strict"&gt;&lt;tr&gt;
</code></pre>
                  
                  
                  
                  <p>
                    <th headers=”nombre”>Víctor</th>
                        <th headers=”edad”>38</th>
                        <th headers=”localidad”>Madrid</th>
                  </p>
                  
                  
                  
                  <p>
                    </tr>
                  </p>
                  
                  
                  
                  <p>
                    <tr>
                      <th headers=”nombre”>Esther</th>
                          <th headers=”edad”>25</th>
                          <th headers=”localidad”>Salamanca</th></p>
                      
                      <p>
                        </tr></pre>
                      </p>
                      
                      
                      
                      <pre><code>  Así, el agente de usuario no visual, cuando vaya leyendo la fila hará lo siguiente:



  &lt;pre&gt;“Nombre, Víctor. Edad, 38. Localidad, Madrid.
</code></pre>
                      
                      
                      
                      <p>
                        Nombre, Esther. Edad, 25. Localidad, Salamanca.”</pre>
                      </p>
                      
                      
                      
                      <pre><code>  &lt;h4&gt;
    Categorizar Celdas
  &lt;/h4&gt;
  Otra de las cosas que podemos hacer para los agentes de usuario no visuales es categorizar las celdas. En

  &lt;a href="http://www.manualweb.net/tutorial-html/"&gt;HTML&lt;/a&gt; tenemos un atributo que es axis, de esta manera podemos establecer ejes de agrupación.

  El &lt;b&gt;atributo axis&lt;/b&gt; aplica a las &lt;a href="http://www.w3api.com/wiki/HTML:TD"&gt;celdas td&lt;/a&gt; y celdas de &lt;a href="http://www.w3api.com/wiki/HTML:TH"&gt;cabecera th&lt;/a&gt;. Y permite darle una categoría textual.

  La estructura sería:

  &lt;pre lang="html4strict"&gt;&lt;td axis=”categoria”&gt;...&lt;/td&gt;&lt;/pre&gt;



  &lt;table width="100%" border="1"&gt;
    &lt;tr style="background-color:#ccc;"&gt;
      &lt;td&gt;

      &lt;/td&gt;


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

  &lt;/table&gt;

  En esta tabla podemos establecer que haya 3 tipos de categorías. Los gastos (comida, hotel y transporte), las ciudades (Madrid y Ávila) y las fechas.

  Así que deberemos de marcar esas celdas con la categoría correspondiente, mediante el atributo axis. El código en

  &lt;a href="http://www.manualweb.net/tutorial-html/"&gt;HTML&lt;/a&gt; nos quedará de la siguiente forma:

  &lt;pre lang="html4strict"&gt;&lt;table&gt;
</code></pre>
                      
                      
                      
                      <p>
                        <tr>
                          <th>
                            </p>
                            
                            <pre><code>&lt;/th&gt;
    &lt;th axis=”gasto”&gt;Comida&lt;/th&gt;
    &lt;th axis=”gasto”&gt;Hotel&lt;/th&gt;
    &lt;th axis=”gasto”&gt;Transporte&lt;/th&gt;
</code></pre>
                            
                            
                            
                            <p>
                              </tr>
                            </p>
                            
                            
                            
                            <p>
                              <tr>
                                <td axis=”ciudad”>Madrid</td>
                                        <td>
                                  </p>
                                  
                                  <pre><code>&lt;/td&gt;


&lt;td&gt;

&lt;/td&gt;


&lt;td&gt;

&lt;/td&gt;
</code></pre>
                                  
                                  
                                  
                                  <p>
                                    </tr>
                                  </p>
                                  
                                  
                                  
                                  <p>
                                    <tr>
                                      <td axis=”fecha”>1 de marzo</td>
                                              <td>
                                        15
                                            
                                      </td></p>
                                      
                                      
                                      
                                      <pre><code>&lt;td&gt;
  120
&lt;/td&gt;


&lt;td&gt;
  -
&lt;/td&gt;
</code></pre>
                                      
                                      
                                      
                                      <p>
                                        </tr>
                                      </p>
                                      
                                      
                                      
                                      <p>
                                        <tr>
                                          <td axis=”fecha”>2 de marzo</td>
                                                  <td>
                                            18
                                                
                                          </td></p>
                                          
                                          
                                          
                                          <pre><code>&lt;td&gt;
  120
&lt;/td&gt;


&lt;td&gt;
  34
&lt;/td&gt;
</code></pre>
                                          
                                          
                                          
                                          <p>
                                            </tr>
                                          </p>
                                          
                                          
                                          
                                          <p>
                                            <tr>
                                              <td axis=”fecha”>3 de marzo</td>
                                                      <td>
                                                25
                                                    
                                              </td></p>
                                              
                                              
                                              
                                              <pre><code>&lt;td&gt;
  120
&lt;/td&gt;


&lt;td&gt;
  -
&lt;/td&gt;
</code></pre>
                                              
                                              
                                              
                                              <p>
                                                </tr>
                                              </p>
                                              
                                              
                                              
                                              <p>
                                                <tr>
                                                  <td axis=”ciudad”>Avila</td>
                                                          <td>
                                                    </p>
                                                    
                                                    <pre><code>&lt;/td&gt;


&lt;td&gt;

&lt;/td&gt;


&lt;td&gt;

&lt;/td&gt;
</code></pre>
                                                    
                                                    
                                                    
                                                    <p>
                                                      </tr>
                                                    </p>
                                                    
                                                    
                                                    
                                                    <p>
                                                      <tr>
                                                        <td axis=”fecha”>4 de marzo</td>
                                                                <td>
                                                          10
                                                              
                                                        </td></p>
                                                        
                                                        
                                                        
                                                        <pre><code>&lt;td&gt;
  75
&lt;/td&gt;


&lt;td&gt;
  12
&lt;/td&gt;
</code></pre>
                                                        
                                                        
                                                        
                                                        <p>
                                                          </tr>
                                                        </p>
                                                        
                                                        
                                                        
                                                        <p>
                                                          <tr>
                                                            <td axis=”fecha”>5 de marzo</td>
                                                                    <td>
                                                              12
                                                                  
                                                            </td></p>
                                                            
                                                            
                                                            
                                                            <pre><code>&lt;td&gt;
  75
&lt;/td&gt;


&lt;td&gt;
  14
&lt;/td&gt;
</code></pre>
                                                            
                                                            
                                                            
                                                            <p>
                                                              </tr>
                                                            </p>
                                                            
                                                            
                                                            
                                                            <p>
                                                              </table></pre>
                                                            </p>
                                                            
                                                            
                                                            
                                                            <pre><code>  El atributo axis se combina con el atributo headers para poder dar suficiente información a los agentes de usuario no visuales sobre las tablas.


  &lt;h3&gt;
    Anchos de las tablas y columnas
  &lt;/h3&gt;
  Aunque el formato de las tablas, tanto para la tabla en sí, como para sus filas y celdas se hará mediante

  &lt;a href="http://www.manualweb.net/tutorial-css/"&gt;hojas de estilo CSS&lt;/a&gt;, tenemos dos formas básicas de poder establecer el ancho de la tabla y el ancho de las columnas.

  En primer lugar podemos utilizar el &lt;a href="http://www.w3api.com/wiki/HTML:Width"&gt;atributo width&lt;/a&gt; del &lt;a href="http://www.w3api.com/wiki/HTML:TABLE"&gt;elemento table&lt;/a&gt;.

  &lt;pre lang="html4strict"&gt;&lt;table width=”ancho”&gt;...&lt;/table&gt;&lt;/pre&gt;

  De esta forma podremos establecer en cualquier medida el ancho que queremos que ocupe la tabla. Ya sean px, em, tantos por ciento,...

  Por ejemplo podemos definir que ocupe todo el ancho de una página asignándole un valor de width del 100%.



  &lt;pre lang="html4strict"&gt;&lt;table width=”100%”&gt;...&lt;/table&gt;&lt;/pre&gt;

  Para el caso de las columnas ya hemos visto que tanto los elementos

  &lt;a href="http://www.w3api.com/wiki/HTML:COLGROUP"&gt;colgroup&lt;/a&gt; como &lt;a href="http://www.w3api.com/wiki/HTML:COL"&gt;col&lt;/a&gt; también tenían el &lt;a href="http://www.w3api.com/wiki/HTML:Width"&gt;atributo width&lt;/a&gt;. Así que serán con estos elemento con los que de forma básica podamos establecer el ancho de una columna.

  De esta forma si tenemos 4 columnas y queremos que se distribuyan de forma igual, podríamos escribir el siguiente código.

  &lt;pre lang="html4strict"&gt;&lt;table&gt;
</code></pre>
                                                            
                                                            
                                                            
                                                            <p>
                                                              <colgroup span=”4” width=”25%”>
                                                                ....
                                                            </p>
                                                            
                                                            
                                                            
                                                            <p>
                                                              </table></pre>
                                                            </p>

 [1]: http://www.w3api.com/wiki/HTML:TR
 [2]: http://www.manualweb.net/tutorial-html/
 [3]: http://www.w3api.com/wiki/HTML:THEAD
 [4]: http://www.w3api.com/wiki/HTML:TBODY
 [5]: http://www.w3api.com/wiki/HTML:TFOOT
 [6]: http://www.w3api.com/wiki/HTML:COLGROUP
 [7]: http://www.w3api.com/wiki/HTML:Width