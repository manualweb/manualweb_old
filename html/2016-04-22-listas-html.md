---
ID: 812
post_title: '15 &#8211; Listas en HTML'
author: Víctor Cuervo
post_date: 2016-04-22 12:00:06
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/html/listas-html/
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
urlcharla:
  - >
    https://www.facebook.com/groups/html5.es/
urlvideo:
  - PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos:
  - >
    http://lineadecodigo.com/tag/html-listas/feed/
---
<span style="font-weight: 400;">Las listas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> nos permite crear conjuntos de elementos en forma de lista dentro de una página, todos los cuales irán precedidos, generalmente, por un guión o número.</span> <span style="font-weight: 400;">Los tipos de listas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> son los siguientes:</span> 
<li style="font-weight: 400;">
  <span style="font-weight: 400;">Listas ordenadas</span>
</li>
<li style="font-weight: 400;">
  <span style="font-weight: 400;">Listas desordenadas</span>
</li>
<li style="font-weight: 400;">
  <span style="font-weight: 400;">Listas de definiciones</span>
</li>

### Listas Ordenadas

<span style="font-weight: 400;">Las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> ordenadas son aquellas que nos muestran los elementos de la lista en orden. Para representar el orden tendremos los elementos numerados. Es decir, cada uno de los elementos irá precedido de un número o letra que establezca su orden.</span> <span style="font-weight: 400;">Las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> ordenadas se representan mediante el</span> [<span style="font-weight: 400;">elemento OL</span>][2]<span style="font-weight: 400;">.</span> <pre lang="html4strict"><ol>
  ... 
</ol></pre>

<span style="font-weight: 400;">Cada uno de los elementos de la lista ordenada se representará mediante el </span>[<span style="font-weight: 400;">elemento LI</span>][3]<span style="font-weight: 400;">.</span> <pre lang="html4strict"><ol>
  <li>
    Elemento 1
  </li>
    
  <li>
    Elemento 2
  </li>
    ...
    
  <li>
    Elemento N
  </li>
  
</ol></pre> Un ejemplo de lista ordenada sería el siguiente: 

<pre lang="html4strict"><ol>
  <li>
    Julio
  </li>
    
  <li>
    Carmen
  </li>
    
  <li>
    Ignacio
  </li>
    
  <li>
    Elena
  </li>
  
</ol></pre>

<span style="font-weight: 400;">Que produciría el siguiente efecto:</span> 
1.  Julio
2.  Carmen
3.  Ignacio
4.  Elena

#### Número de inicio de la lista: start

<span style="font-weight: 400;">El atributo start nos permite indicar el número por el cual queremos que empiece la lista, ya que por defecto las listas ordenadas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> empiezan por el número 1.</span> <pre lang="html4strict">&lt;ol start=”numero”> … &lt;/ol></pre>

<span style="font-weight: 400;">De esta forma, si queremos que la lista empiece por el número 5, escribiremos el siguiente código:</span> <pre lang="html4strict">&lt;ol start=”5”>
  <li>
  Julio
</li>
  
<li>
  Carmen
</li>
  
<li>
  Ignacio
</li>
  
<li>
  Elena
</li>
&lt;/ol></pre>

<span style="font-weight: 400;">Que produciría el siguiente efecto:</span> <ol start="5">
  <li>
    Julio
  </li>
  <li>
    Carmen
  </li>
  <li>
    Ignacio
  </li>
  <li>
    Elena
  </li>
</ol>

#### Tipo de lista ordenada: type

<span style="font-weight: 400;">De igual manera podemos indicar el tipo de lista ordenada en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> que queremos representar. Entre los tipos de listas que podemos representar tenemos:</span> 
<li style="font-weight: 400;">
  <span style="font-weight: 400;">1 - Listas decimales</span>
</li>
<li style="font-weight: 400;">
  <span style="font-weight: 400;">a - Listas alfabéticas en minúsculas</span>
</li>
<li style="font-weight: 400;">
  <span style="font-weight: 400;">A - Listas alfabéticas en mayúsculas</span>
</li>
<li style="font-weight: 400;">
  <span style="font-weight: 400;">i - Listas de números romanos en minúsculas</span>
</li>
<li style="font-weight: 400;">
  <span style="font-weight: 400;">I - Listas de números romanos en mayúsculas</span>
</li>

<span style="font-weight: 400;">Los valores indicados al principio son los que le podemos asignar al </span>[<span style="font-weight: 400;">atributo type</span>][4]<span style="font-weight: 400;"> de la lista ordenada en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;">.</span> <pre lang="html4strict">&lt;ol type=”tipo”> … &lt;/ol></pre>

<span style="font-weight: 400;">Si queremos que nuestra lista aparezca ordenada mediante letras en mayúsculas escribimos lo siguiente:</span> <pre lang="html4strict">&lt;ol type=”A”>
  <li>
  Julio
</li>
  
<li>
  Carmen
</li>
  
<li>
  Ignacio
</li>
  
<li>
  Elena
</li>
&lt;/ol></pre> En este caso la lista se representará de la siguiente forma: 

<ol type="A">
  <li>
    Julio
  </li>
  <li>
    Carmen
  </li>
  <li>
    Ignacio
  </li>
  <li>
    Elena
  </li>
</ol>

#### Atributos start/type en HTML 4.01

<span style="font-weight: 400;">Aunque en </span>[<span style="font-weight: 400;">HTML 5</span>][5]<span style="font-weight: 400;"> han vuelto a la especificación los </span>[<span style="font-weight: 400;">atributos type</span>][4]<span style="font-weight: 400;"> y start hay que tener cuidado con ellos, ya que en ciertas versiones como HTML 4.01 fueron declarados obsoletos, por lo cual si usamos tipos de documentos HTML 4.01 strict podríamos tener un problema en su definición.</span> <span style="font-weight: 400;">Para estos casos (y para todos en general) podemos utilizar las hojas de estilo </span>[<span style="font-weight: 400;">CSS</span>][6]<span style="font-weight: 400;"> de cara a dar estilo a las listas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;">. </span> <span style="font-weight: 400;">De esta forma en </span>[<span style="font-weight: 400;">CSS</span>][6]<span style="font-weight: 400;"> podemos escribir lo siguiente:</span> <pre lang="html4strict">&lt;style type=”text/css”>
ol {
  list-style-type: lower-roman;
}
&lt;/style></pre>

<span style="font-weight: 400;">Lo cual hará que las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> ordenadas se muestren en números romanos y en minúsculas.</span> 
#### Listas en orden inverso: reversed

<span style="font-weight: 400;">En </span>[<span style="font-weight: 400;">HTML 5</span>][5]<span style="font-weight: 400;"> aparece el atributo reversed para las listas ordenadas. El atributo reversed nos permite invertir el orden de la lista. Es decir, realiza la numeración de la lista de forma inversa.</span> <span style="font-weight: 400;">Para utilizarlo simplemente indicamos el atributo reversed sobre el elemento OL.</span> <pre lang="html4strict"><ol reversed>
  … 
</ol></pre>

<span style="font-weight: 400;">En este caso, si escribimos la siguiente lista:</span> <pre lang="html4strict"><ol reversed>
  <li>
    Julio
  </li>
    
  <li>
    Carmen
  </li>
    
  <li>
    Ignacio
  </li>
    
  <li>
    Elena
  </li>
  
</ol></pre>

<span style="font-weight: 400;">Lo que obtendremos por pantalla será lo siguiente:</span> <ol reversed>
  <li>
    Julio
  </li>
  <li>
    Carmen
  </li>
  <li>
    Ignacio
  </li>
  <li>
    Elena
  </li>
</ol>

### Listas Desordenadas

<span style="font-weight: 400;">Las listas desordenadas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> nos sirven para mostrar los elementos sin ningún tipo de orden, simplemente precedidos por una viñeta que puede ser un punto, un cuadrado,...</span> <span style="font-weight: 400;">Para definir una lista desordenada en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> utilizamos el </span>[<span style="font-weight: 400;">elemento ul</span>][7]<span style="font-weight: 400;">.</span> <pre lang="html4strict"><ul>
  … 
</ul></pre>

<span style="font-weight: 400;">Para representar los elementos de la lista desordenada utilizamos el mismo elemento que con las listas ordenadas, es decir, el </span>[<span style="font-weight: 400;">elemento li</span>][3]<span style="font-weight: 400;">.</span> <pre lang="html4strict"><ul>
  <li>
    Elemento 1
  </li>
    
  <li>
    Elemento 2
  </li>
    ...
    
  <li>
    Elemento N
  </li>
  
</ul></pre>

<span style="font-weight: 400;">De esa forma podríamos tener el siguiente código </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;">:</span> <pre lang="html4strict"><ul>
  <li>
    FC. Barcelona
  </li>
    
  <li>
    Real Madrid
  </li>
    
  <li>
    Real Betis
  </li>
    
  <li>
    Atlético de Madrid
  </li>
  
</ul></pre>

<span style="font-weight: 400;">Lo que nos mostrará por pantalla:</span> 
*   FC. Barcelona
*   Real Madrid
*   Real Betis
*   Atlético de Madrid

#### Tipos de lista desordenada

<span style="font-weight: 400;">En el caso de las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> desordenadas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> no podemos indicarle el tipo de lista mediante </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;">. En este caso tenemos que recurrir a </span>[<span style="font-weight: 400;">CSS</span>][6]<span style="font-weight: 400;"> para poder indicar el tipo de lista utilizando el </span>[<span style="font-weight: 400;">atributo list-style-type</span>][8] <pre lang="html4strict">&lt;style type=”text/css”>
ul {
  list-style-type: circle;
}
&lt;/style></pre>

### Listas de Definiciones

<span style="font-weight: 400;">Las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> de definiciones en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> nos sirven para montar listas en las que tenemos la estructura valor y definición. Suelen ser listas para definir términos, como si fuese un diccionario, si bien pueden ser cualquier par valor-definición.</span> <span style="font-weight: 400;">Las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> de definiciones en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> se construyen mediante el </span>[<span style="font-weight: 400;">elemento dl</span>][9]<span style="font-weight: 400;">.</span> <pre lang="html4strict"><dl>
  … 
</dl></pre>

<span style="font-weight: 400;">En este caso, dentro de las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> de definiciones tenemos dos elementos anidados, el que representa al valor </span>[<span style="font-weight: 400;">dt</span>][10]<span style="font-weight: 400;"> y el que representa a la definición </span>[<span style="font-weight: 400;">dd</span>][11]<span style="font-weight: 400;">.</span> <span style="font-weight: 400;">De esta forma la estructura de las listas en <a href="http://www.manualweb.net/tutorial-html/">HTML</a> de definiciones es la siguiente:</span> <pre lang="html4strict"><dl>
  <dt>
    Término1
  </dt>
    
  
  <dd>
    Definición 1
  </dd>
    
  
  <dt>
    Término 2
  </dt>
    
  
  <dd>
    Definición 2
  </dd>
    …
    
  
  <dt>
    Término N
  </dt>
    
  
  <dd>
    Definición N
  </dd>
  
</dl></pre> Si queremos crear una lista en 

[HTML][1] con definiciones de palabras, podemos escribir lo siguiente: <pre lang="html4strict"><dl>
  <dt>
    Pizpireta
  </dt>
    
  
  <dd>
    Dicho de una mujer: Viva, pronta y aguda.
  </dd>
    
  
  <dt>
    Pulular
  </dt>
    
  
  <dd>
    Dicho de las personas, animales o cosas: Abundar y bullir en un lugar.
  </dd>
    
  
  <dt>
    Concupiscencia
  </dt>
    
  
  <dd>
    En la moral católica, deseo de bienes terrenos y, en especial, apetito desordenado de placeres deshonestos.
  </dd>
  
</dl></pre>

Pizpireta
:   Dicho de una mujer: Viva, pronta y aguda.

Pulular
:   Dicho de las personas, animales o cosas: Abundar y bullir en un lugar.

Concupiscencia
:   En la moral católica, deseo de bienes terrenos y, en especial, apetito desordenado de placeres deshonestos.

<span style="font-weight: 400;">Por defecto los navegadores dejan el término y en la siguiente líne, junto con un tabulador, la definición.</span> 
### Listas anidadas

<span style="font-weight: 400;">Cuando estemos manejando listas podemos anidar unas en otras independientemente del tipo de lista que estemos anidando.</span> <span style="font-weight: 400;">Para crear listas anidadas en </span>[<span style="font-weight: 400;">HTML</span>][1]<span style="font-weight: 400;"> simplemente tenemos que hacer que el elemento de una de las listas sea a su vez una lista. Es decir, el esquema de listas sería parecido al siguiente:</span> <pre lang="html4strict"><ul>
  <li>
    Elemento 1
  </li>
    
  <li>
    Elemento 2
  </li>
    
  <li>
    <ol>
      <li>
        Elemento 2.1
      </li>
             
      <li>
        Elemento 2.2
      </li>
             …
             
      <li>
        Elemento 2.N
      </li>
          
    </ol>
      
  </li>
    
  
  <li>
    Elemento 3
  </li>
    …
    
  <li>
    Elemento N
  </li>
  
</ul></pre>

<span style="font-weight: 400;">En este caso hemos anidado una lista ordenada dentro del tercer </span>[<span style="font-weight: 400;">elemento li</span>][3]<span style="font-weight: 400;"> de una lista desordenada.</span> <span style="font-weight: 400;">Hay que tener cuidado de poner el </span>[<span style="font-weight: 400;">elemento li</span>][3]<span style="font-weight: 400;"> dentro de la lista anidada, ya que si no lo ponemos estaremos generando un código incorrecto.</span> <span style="font-weight: 400;">Las anidaciones de listas puede ser de cualquier tipo de lista y sin límite de anidación.</span> <span style="font-weight: 400;">Un ejemplo de listas anidadas sería una clasificación de animales como la siguiente:</span> <pre lang="html4strict"><ul>
  <li>
    Carnívoro
        <ul>
      <li>
        León
      </li>
            
      <li>
        Buitre
      </li>
            
      <li>
        Hiena
      </li>
          
    </ul>
      
  </li>
    
  
  <li>
    Herbívoro
        <ul>
      <li>
        Cabra
      </li>
            
      <li>
        Vaca
      </li>
          
    </ul>
      
  </li>
    
  
  <li>
    Omnívoro
        <ul>
      <li>
        Oso
      </li>
            
      <li>
        Urraca
      </li>
          
    </ul>
      
  </li>
  
</ul></pre> El efecto que obtendríamos sería el siguiente: 

*   Carnívoro 
    *   León
    *   Buitre
    *   Hiena
*   Herbívoro 
    *   Cabra
    *   Vaca
*   Omnívoro 
    *   Oso
    *   Urraca

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.w3api.com/wiki/HTML:OL
 [3]: http://www.w3api.com/wiki/HTML:LI
 [4]: http://www.w3api.com/wiki/HTML:Type
 [5]: http://www.manualweb.net/tutorial-html5/
 [6]: http://www.manualweb.net/tutorial-css/
 [7]: http://www.w3api.com/wiki/HTML:UL
 [8]: http://www.w3api.com/wiki/CSS:List-style-type
 [9]: http://www.w3api.com/wiki/HTML:DL
 [10]: http://www.w3api.com/wiki/HTML:DT
 [11]: http://www.w3api.com/wiki/HTML:DD