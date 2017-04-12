---
ID: 1386
post_title: 16 – Tablas en HTML
author: Víctor Cuervo
post_date: 2017-04-12 18:45:40
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/tablas-en-html/
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
### ¿Qué son las tablas en HTML?

<span style="font-weight: 400">Las tablas es el elemento del lenguaje </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> que utilizaremos para mostrar información de forma agrupada. Ya sea texto, imágenes, vídeos,...</span> <span style="font-weight: 400">El </span>[<span style="font-weight: 400">elemento table</span>][2]<span style="font-weight: 400"> será el que nos ayudará para crear las tablas en </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">.</span> <span style="font-weight: 400">Un mal uso de las tablas en </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400"> es el motivo de maquetación, uso que se dió a las tablas en los principios del lenguaje </span>[<span style="font-weight: 400">HTML</span>][1]<span style="font-weight: 400">. Algo que hoy en día es una mala práctica. Cambiando por un modelo de maquetación apoyado en capas.</span>

### Crear una tabla simple

<span style="font-weight: 400">Para crear una tabla vamos a necesitar conocer, al menos, tres elementos: </span>[<span style="font-weight: 400">table</span>][2]<span style="font-weight: 400">, </span>[<span style="font-weight: 400">tr</span>][3]<span style="font-weight: 400"> y </span>[<span style="font-weight: 400">td</span>][4]<span style="font-weight: 400">. Si bien existen otros cuantos que nos permitirán ampliar la funcionalidad de las tablas.</span> <span style="font-weight: 400">El primer elemento es </span>[<span style="font-weight: 400">table</span>][2]<span style="font-weight: 400">. </span>[<span style="font-weight: 400">table</span>][2]<span style="font-weight: 400"> es el elemento que representa las tablas y será el que agrupe al resto de elementos. Por lo tanto tiene sus etiquetas de inicio y cierre.</span>

<pre><table>
  …
    
  
</table></pre>

<span style="font-weight: 400">Siguiendo con la construcción de la tabla el siguiente elemento que necesitamos es </span>[<span style="font-weight: 400">tr</span>][3]<span style="font-weight: 400">. El </span>[<span style="font-weight: 400">elemento tr</span>][3]<span style="font-weight: 400"> representa a una fila de la tabla. Por lo tanto tendremos tantos </span>[<span style="font-weight: 400">elementos tr</span>][3]<span style="font-weight: 400"> como filas tenga la tabla.</span> <span style="font-weight: 400">Así, si queremos tener una tabla de tres filas tendremos un código como el que sigue:</span>

<pre><table>
  <tr>
    …
          
      
  </tr>
    
    
      
    
    
  
  <tr>
    …
          
      
  </tr>
    
    
      
    
    
  
  <tr>
    …
          
      
  </tr>
    
    
  
</table></pre>

<span style="font-weight: 400">El último elemento que necesitamos conocer es </span>[<span style="font-weight: 400">td</span>][4]<span style="font-weight: 400">. El </span>[<span style="font-weight: 400">elemento td</span>][4]<span style="font-weight: 400"> es el que representa de una forma unitaria a una celda. Por lo tanto los </span>[<span style="font-weight: 400">elementos tr</span>][3]<span style="font-weight: 400"> tendrán tantos </span>[<span style="font-weight: 400">elementos td</span>][4]<span style="font-weight: 400"> en su interior como celdas contenga la fila.</span> <span style="font-weight: 400">El contenido que haya entre los </span>[<span style="font-weight: 400">elementos td</span>][4]<span style="font-weight: 400"> será el contenido de la celda.</span> <span style="font-weight: 400">Una tabla de tres filas por cuatro columnas quedaría de la siguiente forma:</span>

<pre><table>
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
    
    
      
    
    
  
  <tr>
    <td>
      Fila 2 Columna 1
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 2 Columna 2
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 2 Columna 3
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 2 Columna 4
                
          
    </td>
        
          
      
  </tr>
    
    
      
    
    
  
  <tr>
    <td>
      Fila 3 Columna 1
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 3 Columna 2
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 3 Columna 3
                
          
    </td>
        
        
            
        
        
    
    <td>
      Fila 3 Columna 4
                
          
    </td>
        
          
      
  </tr>
    
    
  
</table></pre>

<span style="font-weight: 400">Así con los tres elementos </span>[<span style="font-weight: 400">table</span>][2]<span style="font-weight: 400">, </span>[<span style="font-weight: 400">tr</span>][3]<span style="font-weight: 400"> y </span>[<span style="font-weight: 400">td</span>][4]<span style="font-weight: 400"> tenemos construida nuestra tabla.</span> <span style="font-weight: 400">Visualmente tendríamos algo así:</span>

<table border="1" width="100%">
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
  
  <tr>
    <td>
      Fila 2 Columna 1
    </td>
    
    <td>
      Fila 2 Columna 2
    </td>
    
    <td>
      Fila 2 Columna 3
    </td>
    
    <td>
      Fila 2 Columna 4
    </td>
  </tr>
  
  <tr>
    <td>
      Fila 3 Columna 1
    </td>
    
    <td>
      Fila 3 Columna 2
    </td>
    
    <td>
      Fila 3 Columna 3
    </td>
    
    <td>
      Fila 3 Columna 4
    </td>
  </tr>
</table>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:TABLE
 [3]: http://www.w3api.com/wiki/HTML:TR
 [4]: http://www.w3api.com/wiki/HTML:TD