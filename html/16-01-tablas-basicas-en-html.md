---
ID: 1414
post_title: 16.01 – Tablas Básicas en HTML
author: Víctor Cuervo
post_date: 2017-04-12 19:15:26
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/tablas-basicas-en-html/
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
    http://lineadecodigo.com/tag/html-tabla/feed/
gitfolder:
  - html
---
Dentro de las tablas básicas en [HTML][1] vamos a ver los siguientes conceptos: [TOC]

### Poner título a la tabla Ahora que conocemos cómo se construye una tabla básica con

[HTML][1] vamos a ir viendo qué posibilidades adicionales tenemos sobre las tablas. Lo primero que haremos será poner un título a la tabla. Para ello vamos a utilizar el [elemento caption][2]. El contenido del [elemento caption][2] será el título que le asignemos a la tabla. Añadimos el [elemento caption][2] antes de cualquier definición de filas dentro de la tabla. Así, el código para poner el título a la tabla sería:

<pre><table>
  &lt;caption&gt;Mi tabla de ejemplo&lt;/caption&gt;
        <tr>
    <td>
      Fila 1 Columna 1
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 1 Columna 2
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 1 Columna 3
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 1 Columna 4
                
          
    </td>
        
          
      
  </tr>
    
    
  
</table></pre>

### Resumen de la tabla Aunque el título suele ser el elemento descriptivo de la tabla existe un atributo a nivel del

[elemento table][3] de especial importancia. Este es el **atributo summary**. El **atributo summary** nos permite adjuntar un resumen de la información que contiene la tabla. Este atributo será de gran interés para cuando nuestras páginas web sean interpretadas por programas para discapacitados, ya que la información que contiene una tabla suele ser de difícil interpretación. Es por ello que es muy recomendable que siempre añadamos un resumen a nuestra tabla. El código es tan sencillo como este:

<pre>&lt;table summary=”Tabla que contiene datos de ejemplo para poder explicar como construir tablas con el lenguaje HTML”&gt;
  &lt;caption&gt;Mi tabla de ejemplo&lt;/caption&gt;
  <tr>
  <td>
    Fila 1 Columna 1
          
      
  </td>
    
    
      
    
    
  
  <td>
    Fila 1 Columna 2
          
      
  </td>
    
    
      
    
    
  
  <td>
    Fila 1 Columna 3
          
      
  </td>
    
    
      
    
    
  
  <td>
    Fila 1 Columna 4
          
      
  </td>
    
    
  
</tr>
&lt;/table&gt;</pre>

### Definiendo Una Cabecera en la Tabla Una cosa que vemos es que las tablas suelen tener una primera fila de encabezado. Dentro de las tablas en

[HTML][1] podemos identificar esta fila mediante el [elemento th][4]. Es decir, para las celdas de la fila de cabecera en vez de utilizar un [elemento td][5] utilizaremos un [elemento th][4]. Así, la cabecera de una tabla quedará de la siguiente forma:

<pre><table>
  <tr>
    <th>
      Cabecera 1
                
          
    </th>
        
        
            
        
        
    
    <th>
      Cabecera 2
                
          
    </th>
        
        
            
        
        
    
    <th>
      Cabecera 3
                
          
    </th>
        
          
      
  </tr>
    
    
      
    
    
  
  <tr>
    <td>
      Fila 1 Columna 1
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 1 Columna 2
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 1 Columna 3
                
          
    </td>
        
          
      
  </tr>
    
    
  
</table></pre>

### El atributo scope Hay celdas de cabecera que necesiten una pequeña explicación sobre si la información que representan es la de las columnas o la de las filas. Suele suceder, normalmente, con la primera celda.

<table width="100%" border="1">
  <tr>
    <td width="33%" style="text-align:center;background-color:#cecece">
      Columna o Fila
    </td>
    
    <td width="33%" style="text-align:center">
      ?
    </td>
    
    <td width="33%" style="text-align:center">
      ?
    </td>
  </tr>
  
  <tr>
    <td style="text-align:center">
      ?
    </td>
    
    <td>
    </td>
    
    <td>
    </td>
  </tr>
  
  <tr>
    <td style="text-align:center">
      ?
    </td>
    
    <td>
    </td>
    
    <td>
    </td>
  </tr>
</table>

Para resolver este problema tenemos el atributo scope. El atributo scope solo se puede aplicar a las celdas de una cabecera. Y sus valores son: “col”, “row”, “colgroup” o “rowgroup”. De esta forma si queremos que esta celda sea representativa de columnas la definiremos como:

<pre>&lt;td scope=”col”&gt;Contenido de la Celda&lt;/td&gt;</pre>

### Agrupando Celdas A la hora de presentar datos en una tabla nos puede surgir la necesidad de agrupar celdas, ya que el contenido a presentar refleja una agrupación de datos. Imaginemos una tabla que nos saca los ingresos y gastos por meses. Existirá una columna con el mes, la cual agrupará dos columnas: ingresos y gastos. Algo como lo siguiente:

<table width="100%" border="1">
  <tr>
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
  </tr></tbody>
</table>

En este caso lo que estamos diciendo es que una celda ocupa dos espacios. Para ello vamos a utilizar el [atributo colspan][6] sobre el [elemento td][5] de la celda. Así indicaremos que el colspan de esa celda es 2. Ya que ocupa dos celdas.

<pre>&lt;td colspan=”2”&gt;Enero&lt;/td&gt;</pre>

El código completo sería:

<pre><table>
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
      
      
      
      <pre><code>  &lt;pre&gt;&lt;code&gt;  De igual manera nos puede suceder en sentido horizontal. Es decir, que queramos que una celda ocupe dos filas.
</code></pre>
      
      
      
      <p>
        Si lo vemos sobre nuestro ejemplo veremos que podemos añadir una columna que simplemente ponga que los valores numéricos tengan el literal “Datos Económicos”. En este caso tendremos que indicar que esa celda ocupa dos filas.
      </p>
      
      
      
      <p>
        <table width="100%" border="1">
            <tbody>
              <tr>
                <td>
      </p>
      
      
      
      <pre><code>    &lt;/td&gt;


    &lt;td colspan="2"&gt;
      Enero
    &lt;/td&gt;


    &lt;td colspan="2"&gt;
      Febrero
    &lt;/td&gt;

  &lt;/tr&gt;


  &lt;tr&gt;
    &lt;td rowspan="3"&gt;
      Datos Económicos
    &lt;/td&gt;


    &lt;td&gt;
      Ingresos
    &lt;/td&gt;


    &lt;td&gt;
      Gastos
    &lt;/td&gt;


    &lt;td&gt;
      Ingresos
    &lt;/td&gt;


    &lt;td&gt;
      Gastos
    &lt;/td&gt;

  &lt;/tr&gt;


  &lt;tr&gt;
    &lt;td&gt;
      1.000€
    &lt;/td&gt;


    &lt;td&gt;
      700€
    &lt;/td&gt;


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

&lt;/tbody&gt;
</code></pre>
      
      
      
      <p>
        </table>
      </p>
      
      
      
      <p>
        Para la agrupación de filas tenemos otro atributo que es rowspan. Este atributo, al igual que colspan se aplica sobre la
      </p>
      
      
      
      <p>
        <a href="http://www.w3api.com/wiki/HTML:TD">celda td</a>.
      </p>
      
      
      
      <p>
        <pre lang="html4strict"><td rowspan=”3”>Datos Económicos</td></pre>
      </p>
      
      
      
      <p>
        El código completo de la tabla sería el siguiente:
      </p>
      
      
      
      <p>
        <pre lang="html4strict"><table>
        </code></pre>
      </p>
      
      
      
      <pre><code>  &lt;p&gt;
    &lt;tr&gt;
      &lt;td&gt;
        &lt;/p&gt;

        &lt;pre&gt;&lt;code&gt;&lt;/td&gt;
&lt;td colspan=”2”&gt;Enero&lt;/td&gt;
&lt;td colspan=”2”&gt;Febrero&lt;/td&gt;
</code></pre>
      
      
      
      <p>
        </code></pre>
      </p>
      
      
      
      <pre><code>        &lt;p&gt;
          &lt;/tr&gt;
        &lt;/p&gt;



        &lt;p&gt;
          &lt;tr&gt;
            &lt;td rowspan="”3”"&gt;
              Datos Económicos
            &lt;/td&gt;


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
      
      
      
      <pre><code>            &lt;p&gt;
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
        </code></pre>
      </p>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:CAPTION
 [3]: http://www.w3api.com/wiki/HTML:TABLE
 [4]: http://www.w3api.com/wiki/HTML:TH
 [5]: http://www.w3api.com/wiki/HTML:TD
 [6]: http://www.w3api.com/wiki/HTML:Colspan