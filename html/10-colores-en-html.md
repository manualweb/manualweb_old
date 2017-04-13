---
ID: 1376
post_title: 10 – Colores en HTML
author: Víctor Cuervo
post_date: 2017-04-12 00:33:11
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/colores-en-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-texto/feed/
gitfolder: html
---

### Colores RGB

Los colores en [HTML][1] se especifican mediante el estándar RGB (Red Green and Blue). Este estándar indica que una combinación de los tres colores básicos: rojo, verde y azul puede dar lugar a cualquier otro color.

Los valores que se les da al RGB son valores hexadecimales que van desde el 00 hasta el FF. Al valor del color se le antepone una almohadilla.

De esta forma un color rojo sería aquel que solo tiene activado el Red, el verde solo la parte del Green y el azul la parte del Blue. Así los colores básicos en [HTML][1] serán:

<pre>
Rojo    #FF0000
Verde   #00FF00
Azul    #0000FF
</pre>

Otras combinaciones generales de colores serían el negro (activando todos los colores), el blanco (desactivando todos los colores), amarillo (combinando Red y Blue), fucsia (combinando todo el rojo y todo el azul)


<pre>
Negro     #FFFFFF
Blanco    #000000
Amarillo  #FFFF00
Fucsia    #FF00FF
</pre>

Y luego ya combinaciones de los múltiples valores hexadecimales

<pre>
Gris Plata    #C0C0C0
Azul Marino   #000080
Verde Oliva   #808000
…
</pre>

Aunque lo más recomendable es utilizar el código hexadecimal para representar un valor, tenemos la alternativa de referirnos a los colores por su nombre en inglés. Este valor también será entendido por el navegador web. Así tendremos:

* Rojo - red
* Verde - green
* Azul - blue
* Blanco - white
* Negro - black
* Naranja - orange
* …

### Utilizar los colores en HTML

Los colores al ser elementos de estilo son utilizados en las [CSS][2]. Ya que [HTML][1] solo define la estructura de la página.

Pero vamos a ver, por encima, cómo podríamos cambiar el color de un texto. Para ello vamos a utilizar el [atributo style][3]. El atributo style nos permite asignar un estilo [CSS][2] a un elemento [HTML][1].

El estilo que vamos a manipular es color. A ese atributo color le asignaremos un valor RGB.

~~~html
<elemento style=”color:#RGB” />
~~~

Por ejemplo si queremos cambiar el color a un header podríamos hacer lo siguiente.

~~~html
<h1 style=”color:#FF0000”>Cabecera 1</h1>
~~~

Otro atributo [CSS][2] al que podríamos dar un colo es el color de fondo. Para ello deberemos de manipular [el atributo background-color][4]. De esta forma si queremos poner un color de fondo a una capa podríamos hacer lo siguiente.

~~~html
<div style=”background-color:#FFFF00”>Mi Capa</div>
~~~

Es interesante que le eches un ojo al [Manual de CSS][2] para aprender más sobre el uso de colores en páginas web.

### Guía de Colores Hexadecimales

A modo de apoyo aquí tenemos una guía de colores generales, sus valores hexadecimales y nombre en inglés

<table>
  <tbody>
    <tr>
      <td style:"backgroud:blue;" class="c10" colspan="1" rowspan="1">
        <p>
          Aliceblue
        </p>

        <p>
          F0F8FF
        </p>
      </td>

      <td class="c55" colspan="1" rowspan="1">
        <p>
          Antiquewhite
        </p>

        <p>
          FAEBD7
        </p>
      </td>

      <td class="c79" colspan="1" rowspan="1">
        <p>
          Aqua
        </p>

        <p>
          00FFFF
        </p>
      </td>

      <td class="c64" colspan="1" rowspan="1">
        <p>
          Aquamarine
        </p>

        <p>
          7FFFD4
        </p>
      </td>
    </tr>

    <tr>
      <td class="c84" colspan="1" rowspan="1">
        <p>
          Azure
        </p>

        <p>
          F0FFFF
        </p>
      </td>

      <td class="c107" colspan="1" rowspan="1">
        <p>
          Beige
        </p>

        <p>
          F5F5DC
        </p>
      </td>

      <td class="c73" colspan="1" rowspan="1">
        <p>
          Bisque
        </p>

        <p>
          FFE4C4
        </p>
      </td>

      <td class="c151" colspan="1" rowspan="1">
        <p>
          Black
        </p>

        <p>
          000000
        </p>
      </td>
    </tr>

    <tr>
      <td class="c93" colspan="1" rowspan="1">
        <p>
          Blanchedalmond
        </p>

        <p>
          FFEBCD
        </p>
      </td>

      <td class="c148" colspan="1" rowspan="1">
        <p>
          Blue
        </p>

        <p>
          0000FF
        </p>
      </td>

      <td class="c66" colspan="1" rowspan="1">
        <p>
          Blueviolet
        </p>

        <p>
          8A2BE2
        </p>
      </td>

      <td class="c30" colspan="1" rowspan="1">
        <p>
          Brown
        </p>

        <p>
          A52A2A
        </p>
      </td>
    </tr>

    <tr>
      <td class="c128" colspan="1" rowspan="1">
        <p>
          Burlywood
        </p>

        <p>
          DEB887
        </p>
      </td>

      <td class="c121" colspan="1" rowspan="1">
        <p>
          Cadetblue
        </p>

        <p>
          5F9EA0
        </p>
      </td>

      <td class="c72" colspan="1" rowspan="1">
        <p>
          Chartreuse
        </p>

        <p>
          7FFF00
        </p>
      </td>

      <td class="c143" colspan="1" rowspan="1">
        <p>
          Chocolate
        </p>

        <p>
          D2691E
        </p>
      </td>
    </tr>

    <tr>
      <td class="c37" colspan="1" rowspan="1">
        <p>
          Coral
        </p>

        <p>
          FF7F50
        </p>
      </td>

      <td class="c126" colspan="1" rowspan="1">
        <p>
          Cornflowerblue
        </p>

        <p>
          6495ED
        </p>
      </td>

      <td class="c103" colspan="1" rowspan="1">
        <p>
          Cornsilk
        </p>

        <p>
          FFF8DC
        </p>
      </td>

      <td class="c3" colspan="1" rowspan="1">
        <p>
          Crimson
        </p>

        <p>
          DC143C
        </p>
      </td>
    </tr>

    <tr>
      <td class="c7" colspan="1" rowspan="1">
        <p>
          Cyan
        </p>

        <p>
          00FFFF
        </p>
      </td>

      <td class="c50" colspan="1" rowspan="1">
        <p>
          Darkblue
        </p>

        <p>
          00008B
        </p>
      </td>

      <td class="c35" colspan="1" rowspan="1">
        <p>
          Darkcyan
        </p>

        <p>
          008B8B
        </p>
      </td>

      <td class="c153" colspan="1" rowspan="1">
        <p>
          Darkgoldenrod
        </p>

        <p>
          B8860B
        </p>
      </td>
    </tr>

    <tr>
      <td class="c139" colspan="1" rowspan="1">
        <p>
          Darkgray
        </p>

        <p>
          A9A9A9
        </p>
      </td>

      <td class="c115" colspan="1" rowspan="1">
        <p>
          Darkgreen
        </p>

        <p>
          006400
        </p>
      </td>

      <td class="c129" colspan="1" rowspan="1">
        <p>
          Darkkhaki
        </p>

        <p>
          BDB76B
        </p>
      </td>

      <td class="c142" colspan="1" rowspan="1">
        <p>
          Darkmagenta
        </p>

        <p>
          8B008B
        </p>
      </td>
    </tr>

    <tr>
      <td class="c101" colspan="1" rowspan="1">
        <p>
          Darkolivegreen 556B2F
        </p>
      </td>

      <td class="c48" colspan="1" rowspan="1">
        <p>
          Darkorange
        </p>

        <p>
          FF8C00
        </p>
      </td>

      <td class="c144" colspan="1" rowspan="1">
        <p>
          Darkorchid
        </p>

        <p>
          9932CC
        </p>
      </td>

      <td class="c58" colspan="1" rowspan="1">
        <p>
          Darkred
        </p>

        <p>
          8B0000
        </p>
      </td>
    </tr>

    <tr>
      <td class="c16" colspan="1" rowspan="1">
        <p>
          Darksalmon
        </p>

        <p>
          E9967A
        </p>
      </td>

      <td class="c25" colspan="1" rowspan="1">
        <p>
          Darkseagreen
        </p>

        <p>
          8FBC8F
        </p>
      </td>

      <td class="c9" colspan="1" rowspan="1">
        <p>
          Darkslateblue
        </p>

        <p>
          483D8B
        </p>
      </td>

      <td class="c134" colspan="1" rowspan="1">
        <p>
          Darkslategray
        </p>

        <p>
          2F4F4F
        </p>
      </td>
    </tr>

    <tr>
      <td class="c104" colspan="1" rowspan="1">
        <p>
          Darkturquoise 00CED1
        </p>
      </td>

      <td class="c67" colspan="1" rowspan="1">
        <p>
          Darkviolet
        </p>

        <p>
          9400D3
        </p>
      </td>

      <td class="c132" colspan="1" rowspan="1">
        <p>
          deeppink
        </p>

        <p>
          FF1493
        </p>
      </td>

      <td class="c78" colspan="1" rowspan="1">
        <p>
          Deepskyblue
        </p>

        <p>
          00BFFF
        </p>
      </td>
    </tr>

    <tr>
      <td class="c44" colspan="1" rowspan="1">
        <p>
          Dimgray
        </p>

        <p>
          696969
        </p>
      </td>

      <td class="c97" colspan="1" rowspan="1">
        <p>
          Dodgerblue
        </p>

        <p>
          1E90FF
        </p>
      </td>

      <td class="c109" colspan="1" rowspan="1">
        <p>
          Firebrick
        </p>

        <p>
          B22222
        </p>
      </td>

      <td class="c90" colspan="1" rowspan="1">
        <p>
          Floralwhite
        </p>

        <p>
          FFFAF0
        </p>
      </td>
    </tr>

    <tr>
      <td class="c99" colspan="1" rowspan="1">
        <p>
          Forestgreen
        </p>

        <p>
          228B22
        </p>
      </td>

      <td class="c56" colspan="1" rowspan="1">
        <p>
          Fuchsia
        </p>

        <p>
          FF00FF
        </p>
      </td>

      <td class="c47" colspan="1" rowspan="1">
        <p>
          Gainsboro
        </p>

        <p>
          DCDCDC
        </p>
      </td>

      <td class="c87" colspan="1" rowspan="1">
        <p>
          Ghostwhite
        </p>

        <p>
          F8F8FF
        </p>
      </td>
    </tr>

    <tr>
      <td class="c106" colspan="1" rowspan="1">
        <p>
          Gold
        </p>

        <p>
          FFD700
        </p>
      </td>

      <td class="c52" colspan="1" rowspan="1">
        <p>
          Goldenrod
        </p>

        <p>
          DAA520
        </p>
      </td>

      <td class="c14" colspan="1" rowspan="1">
        <p>
          Gray
        </p>

        <p>
          808080
        </p>
      </td>

      <td class="c82" colspan="1" rowspan="1">
        <p>
          Green
        </p>

        <p>
          008000
        </p>
      </td>
    </tr>

    <tr>
      <td class="c69" colspan="1" rowspan="1">
        <p>
          Greenyellow
        </p>

        <p>
          ADFF2F
        </p>
      </td>

      <td class="c152" colspan="1" rowspan="1">
        <p>
          Honeydew
        </p>

        <p>
          F0FFF0
        </p>
      </td>

      <td class="c130" colspan="1" rowspan="1">
        <p>
          Hotpink
        </p>

        <p>
          FF69B4
        </p>
      </td>

      <td class="c92" colspan="1" rowspan="1">
        <p>
          Indianred
        </p>

        <p>
          CD5C5C
        </p>
      </td>
    </tr>

    <tr>
      <td class="c120" colspan="1" rowspan="1">
        <p>
          Indigo
        </p>

        <p>
          4B0082
        </p>
      </td>

      <td class="c85" colspan="1" rowspan="1">
        <p>
          Ivory
        </p>

        <p>
          FFFFF0
        </p>
      </td>

      <td class="c53" colspan="1" rowspan="1">
        <p>
          Khaki
        </p>

        <p>
          F0E68C
        </p>
      </td>

      <td class="c15" colspan="1" rowspan="1">
        <p>
          Lavendar
        </p>

        <p>
          E6E6FA
        </p>
      </td>
    </tr>

    <tr>
      <td class="c149" colspan="1" rowspan="1">
        <p>
          Lavenderblush FFF0F5
        </p>
      </td>

      <td class="c124" colspan="1" rowspan="1">
        <p>
          Lawngreen
        </p>

        <p>
          7CFC00
        </p>
      </td>

      <td class="c108" colspan="1" rowspan="1">
        <p>
          Lemonchiffon
        </p>

        <p>
          FFFACD
        </p>
      </td>

      <td class="c75" colspan="1" rowspan="1">
        <p>
          Lightblue
        </p>

        <p>
          ADD8E6
        </p>
      </td>
    </tr>

    <tr>
      <td class="c131" colspan="1" rowspan="1">
        <p>
          Lightcoral
        </p>

        <p>
          F08080
        </p>
      </td>

      <td class="c63" colspan="1" rowspan="1">
        <p>
          Lightcyan
        </p>

        <p>
          E0FFFF
        </p>
      </td>

      <td class="c146" colspan="1" rowspan="1">
        <p>
          Lightgoldenrodyellow
        </p>

        <p>
          FAFAD2
        </p>
      </td>

      <td class="c81" colspan="1" rowspan="1">
        <p>
          Lightgreen
        </p>

        <p>
          90EE90
        </p>
      </td>
    </tr>

    <tr>
      <td class="c74" colspan="1" rowspan="1">
        <p>
          Lightgrey
        </p>

        <p>
          D3D3D3
        </p>
      </td>

      <td class="c28" colspan="1" rowspan="1">
        <p>
          Lightpink
        </p>

        <p>
          FFB6C1
        </p>
      </td>

      <td class="c105" colspan="1" rowspan="1">
        <p>
          Lightsalmon
        </p>

        <p>
          FFA07A
        </p>
      </td>

      <td class="c119" colspan="1" rowspan="1">
        <p>
          Lightseagreen
        </p>

        <p>
          20B2AA
        </p>
      </td>
    </tr>

    <tr>
      <td class="c39" colspan="1" rowspan="1">
        <p>
          Lightskyblue
        </p>

        <p>
          87CEFA
        </p>
      </td>

      <td class="c140" colspan="1" rowspan="1">
        <p>
          Lightslategray
        </p>

        <p>
          778899
        </p>
      </td>

      <td class="c29" colspan="1" rowspan="1">
        <p>
          Lightsteelblue
        </p>

        <p>
          B0C4DE
        </p>
      </td>

      <td class="c18" colspan="1" rowspan="1">
        <p>
          Lightyellow
        </p>

        <p>
          FFFFE0
        </p>
      </td>
    </tr>

    <tr>
      <td class="c36" colspan="1" rowspan="1">
        <p>
          Lime
        </p>

        <p>
          00FF00
        </p>
      </td>

      <td class="c137" colspan="1" rowspan="1">
        <p>
          Limegreen
        </p>

        <p>
          32CD32
        </p>
      </td>

      <td class="c110" colspan="1" rowspan="1">
        <p>
          Linen
        </p>

        <p>
          FAF0E6
        </p>
      </td>

      <td class="c57" colspan="1" rowspan="1">
        <p>
          Magenta
        </p>

        <p>
          FF00FF
        </p>
      </td>
    </tr>

    <tr>
      <td class="c54" colspan="1" rowspan="1">
        <p>
          Maroon
        </p>

        <p>
          800000
        </p>
      </td>

      <td class="c20" colspan="1" rowspan="1">
        <p>
          Mediumauqamarine
        </p>

        <p>
          66CDAA
        </p>
      </td>

      <td class="c76" colspan="1" rowspan="1">
        <p>
          Mediumblue
        </p>

        <p>
          0000CD
        </p>
      </td>

      <td class="c70" colspan="1" rowspan="1">
        <p>
          Mediumorchid
        </p>

        <p>
          BA55D3
        </p>
      </td>
    </tr>

    <tr>
      <td class="c49" colspan="1" rowspan="1">
        <p>
          Mediumpurple 9370D8
        </p>
      </td>

      <td class="c46" colspan="1" rowspan="1">
        <p>
          Mediumseagreen
        </p>

        <p>
          3CB371
        </p>
      </td>

      <td class="c127" colspan="1" rowspan="1">
        <p>
          Mediumslateblue
        </p>

        <p>
          7B68EE
        </p>
      </td>

      <td class="c136" colspan="1" rowspan="1">
        <p>
          Mediumspringgreen 00FA9A
        </p>
      </td>
    </tr>

    <tr>
      <td class="c125" colspan="1" rowspan="1">
        <p>
          Mediumturquoise
        </p>

        <p>
          48D1CC
        </p>
      </td>

      <td class="c86" colspan="1" rowspan="1">
        <p>
          Mediumvioletred
        </p>

        <p>
          C71585
        </p>
      </td>

      <td class="c42" colspan="1" rowspan="1">
        <p>
          Midnightblue
        </p>

        <p>
          191970
        </p>
      </td>

      <td class="c59" colspan="1" rowspan="1">
        <p>
          Mintcream
        </p>

        <p>
          F5FFFA
        </p>
      </td>
    </tr>

    <tr>
      <td class="c88" colspan="1" rowspan="1">
        <p>
          Mistyrose
        </p>

        <p>
          FFE4E1
        </p>
      </td>

      <td class="c71" colspan="1" rowspan="1">
        <p>
          Moccasin
        </p>

        <p>
          FFE4B5
        </p>
      </td>

      <td class="c98" colspan="1" rowspan="1">
        <p>
          Navajowhite
        </p>

        <p>
          FFDEAD
        </p>
      </td>

      <td class="c23" colspan="1" rowspan="1">
        <p>
          Navy
        </p>

        <p>
          000080
        </p>
      </td>
    </tr>

    <tr>
      <td class="c89" colspan="1" rowspan="1">
        <p>
          Oldlace
        </p>

        <p>
          FDF5E6
        </p>
      </td>

      <td class="c141" colspan="1" rowspan="1">
        <p>
          Olive
        </p>

        <p>
          808000
        </p>
      </td>

      <td class="c26" colspan="1" rowspan="1">
        <p>
          Olivedrab
        </p>

        <p>
          688E23
        </p>
      </td>

      <td class="c34" colspan="1" rowspan="1">
        <p>
          Orange
        </p>

        <p>
          FFA500
        </p>
      </td>
    </tr>

    <tr>
      <td class="c12" colspan="1" rowspan="1">
        <p>
          Orangered
        </p>

        <p>
          FF4500
        </p>
      </td>

      <td class="c145" colspan="1" rowspan="1">
        <p>
          Orchid
        </p>

        <p>
          DA70D6
        </p>
      </td>

      <td class="c117" colspan="1" rowspan="1">
        <p>
          Palegoldenrod
        </p>

        <p>
          EEE8AA
        </p>
      </td>

      <td class="c45" colspan="1" rowspan="1">
        <p>
          Palegreen
        </p>

        <p>
          98FB98
        </p>
      </td>
    </tr>

    <tr>
      <td class="c11" colspan="1" rowspan="1">
        <p>
          Paleturquoise
        </p>

        <p>
          AFEEEE
        </p>
      </td>

      <td class="c61" colspan="1" rowspan="1">
        <p>
          Palevioletred
        </p>

        <p>
          D87093
        </p>
      </td>

      <td class="c91" colspan="1" rowspan="1">
        <p>
          Papayawhip
        </p>

        <p>
          FFEFD5
        </p>
      </td>

      <td class="c138" colspan="1" rowspan="1">
        <p>
          Peachpuff
        </p>

        <p>
          FFDAB9
        </p>
      </td>
    </tr>

    <tr>
      <td class="c96" colspan="1" rowspan="1">
        <p>
          Peru
        </p>

        <p>
          CD853F
        </p>
      </td>

      <td class="c80" colspan="1" rowspan="1">
        <p>
          Pink
        </p>

        <p>
          FFC0CB
        </p>
      </td>

      <td class="c133" colspan="1" rowspan="1">
        <p>
          Plum
        </p>

        <p>
          DDA0DD
        </p>
      </td>

      <td class="c6" colspan="1" rowspan="1">
        <p>
          Powderblue
        </p>

        <p>
          B0E0E6
        </p>
      </td>
    </tr>

    <tr>
      <td class="c113" colspan="1" rowspan="1">
        <p>
          Purple
        </p>

        <p>
          800080
        </p>
      </td>

      <td class="c94" colspan="1" rowspan="1">
        <p>
          Red
        </p>

        <p>
          FF0000
        </p>
      </td>

      <td class="c147" colspan="1" rowspan="1">
        <p>
          Rosybrown
        </p>

        <p>
          BC8F8F
        </p>
      </td>

      <td class="c33" colspan="1" rowspan="1">
        <p>
          Royalblue
        </p>

        <p>
          4169E1
        </p>
      </td>
    </tr>

    <tr>
      <td class="c43" colspan="1" rowspan="1">
        <p>
          Saddlebrown
        </p>

        <p>
          8B4513
        </p>
      </td>

      <td class="c135" colspan="1" rowspan="1">
        <p>
          Salmon
        </p>

        <p>
          FA8072
        </p>
      </td>

      <td class="c116" colspan="1" rowspan="1">
        <p>
          Sandybrown
        </p>

        <p>
          F4A460
        </p>
      </td>

      <td class="c112" colspan="1" rowspan="1">
        <p>
          Seagreen
        </p>

        <p>
          2E8B57
        </p>
      </td>
    </tr>

    <tr>
      <td class="c13" colspan="1" rowspan="1">
        <p>
          Seashell
        </p>

        <p>
          FFF5EE
        </p>
      </td>

      <td class="c122" colspan="1" rowspan="1">
        <p>
          Sienna
        </p>

        <p>
          A0522D
        </p>
      </td>

      <td class="c31" colspan="1" rowspan="1">
        <p>
          Silver
        </p>

        <p>
          C0C0C0
        </p>
      </td>

      <td class="c114" colspan="1" rowspan="1">
        <p>
          Skyblue
        </p>

        <p>
          87CEEB
        </p>
      </td>
    </tr>

    <tr>
      <td class="c83" colspan="1" rowspan="1">
        <p>
          Slateblue
        </p>

        <p>
          6A5ACD
        </p>
      </td>

      <td class="c38" colspan="1" rowspan="1">
        <p>
          Slategray
        </p>

        <p>
          708090
        </p>
      </td>

      <td class="c51" colspan="1" rowspan="1">
        <p>
          Snow
        </p>

        <p>
          FFFAFA
        </p>
      </td>

      <td class="c95" colspan="1" rowspan="1">
        <p>
          Springgreen
        </p>

        <p>
          00FF7F
        </p>
      </td>
    </tr>

    <tr>
      <td class="c27" colspan="1" rowspan="1">
        <p>
          Steelblue
        </p>

        <p>
          4682B4
        </p>
      </td>

      <td class="c65" colspan="1" rowspan="1">
        <p>
          Tan
        </p>

        <p>
          D2B48C
        </p>
      </td>

      <td class="c21" colspan="1" rowspan="1">
        <p>
          Teal
        </p>

        <p>
          008080
        </p>
      </td>

      <td class="c17" colspan="1" rowspan="1">
        <p>
          Thistle
        </p>

        <p>
          D8BFD8
        </p>
      </td>
    </tr>

    <tr>
      <td class="c40" colspan="1" rowspan="1">
        <p>
          Tomato
        </p>

        <p>
          FF6347
        </p>
      </td>

      <td class="c77" colspan="1" rowspan="1">
        <p>
          Turquoise
        </p>

        <p>
          40E0D0
        </p>
      </td>

      <td class="c62" colspan="1" rowspan="1">
        <p>
          Violet
        </p>

        <p>
          EE82EE
        </p>
      </td>

      <td class="c118" colspan="1" rowspan="1">
        <p>
          Wheat
        </p>

        <p>
          F5DEB3
        </p>
      </td>
    </tr>

    <tr>
      <td colspan="1" rowspan="1">
        <p>
          White
        </p>

        <p>
          FFFFFF
        </p>
      </td>

      <td class="c123" colspan="1" rowspan="1">
        <p>
          Whitesmoke
        </p>

        <p>
          F5F5F5
        </p>
      </td>

      <td class="c111" colspan="1" rowspan="1">
        <p>
          Yellow
        </p>

        <p>
          FFFF00
        </p>
      </td>

      <td class="c19" colspan="1" rowspan="1">
        <p>
          YellowGreen
        </p>

        <p>
          9ACD32
        </p>
      </td>
    </tr>
  </tbody>
</table>

 [1]: http://www.manualweb.net/tutorial-html/
 [2]: http://www.manualweb.net/tutorial-css/
 [3]: http://www.w3api.com/wiki/HTML:Style
 [4]: http://www.w3api.com/wiki/CSS:Background-color
