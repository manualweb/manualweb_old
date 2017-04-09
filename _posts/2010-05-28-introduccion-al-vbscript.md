---
ID: 260
post_title: '01 &#8211; Introducción al VBScript'
author: Víctor Cuervo
post_date: 2010-05-28 22:44:11
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/vbscript/introduccion-al-vbscript/
published: true
nombreforo:
  - VBScript
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/vbscript
---
<!--TOC--> VBScript es un subconjunto de Visual Basic for Applications. Es un lenguaje script cuyo uso se extiende tanto en páginas web de maquinas cliente como en páginas activas de servidor (ASP), si bien, es en este segundo caso, donde adquiere mayor importancia. 

### Comentarios Para introducir un comentario deberemos de usar la apostrofe ' o bien la palabra REM. 

<pre>REM Esto es un comentario
' Esto es un comentario</pre>

### Tipos de Datos Lo primero que debemos de indicar es que en VBScript no es necesario darle un tipo a la variable. Es decir, podremos tener variables sin tipo a las cuales podremos asignarles cualquier valor. Estas variables serían de tipo variant. Los tipos básicos que tiene VBScript son: 

*   **Byte**, enteros entre 0 y 255
*   **Integer**, enteros entre -32.786 y 32.767
*   **Long**, enteros entre -2.147.483.648 y 2.147.483.647
*   **Single**, números reales de precisión simple
*   **Double**, números reales de doble precisión
*   **Currency**, cifras monetarias
*   **Date**, fechas entre 01/01/100 y 31/12/9999
*   **String**, cadenas de hasta 2 millones de caracteres
*   **Boolean**, valor booleano. Puede tomar true o false.
*   **Null**, valor nulo. No contiene nada.
*   **Empty**, es el tipo que toma una variable variant cuando está sin inicializar (0 si es numérica y "" si es cadena).
*   **Error**, sería el tipo error. Existen una serie de funciones que nos servirán para ver cual es el tipo de las variables. Estas funciones son: 

*   **IsEmpty (variable)**, devuelve True si la variable es de tipo Empty
*   **IsError (variable)**, devuelve True si la variable es de tipo Error.
*   **IsNull (variable)**, devuelve True si la variable es de tipo Null.
*   **IsNumeric (variable)**, devuelve True si la variable es un número de cualquier tipo.
*   **IsObject (variable)**, devuelve True si la variable pertenece al tipo Object. Si bien, existe una función que devuelve el tipo de la variable, independientemente del tipo que esta sea. Esta función es 

**vartype (variable)**. Los posibles valores que puede devolver son: 
*   0-Null
*   1-Empty
*   2 -Integer
*   3-Long
*   4-Single
*   5-Double
*   6-Currency
*   7-Date
*   8-String
*   9-Objeto de automatización
*   10-Error
*   11-Boolean
*   12-Variant
*   13-Objeto de acceso a datos
*   17-Byte
*   8192-Array También tenemos unas funciones que nos van a ayudar a cambiar el tipo de las variables. Estas son las funciones de conversión: 

*   **CBool (variable),** convierte la variable en booleana. Si la variable vale 0 se convertirá en true. Otro valor se convertira en false.
*   **CByte (variable),** convierte la variable en Byte.
*   **CInt (variable), **convierte la variable en Integer.
*   **CLng (variable)**, convierte la variable en Long.
*   **CSng (variable)**, convierte la variable en Single.
*   **CDbl (variable)**, convierte la variable en Double.
*   **CCur (variable)**, convierte la variable en Currency.
*   **CDate (variable)**, convierte la variable en Date.
*   **CStr (variable)**, convierte la variable en String.

### Variables Para declarar una variable lo haremos de la siguiente manera: 

<pre>DIM nombre_variable1, nombre_variable2,..., nombre_variableN</pre> Los nombres de las variables deben de comenzar por una letra, no pueden contener el carácter punto y no deben de exceder de 255 caracteres. El ámbito de las variables será global a todos el código script de la página, o bien local si la variable ha sido declarada en un procedimiento. 

### Constantes Para declarar una constante deberemos de hacerlo de la siguiente manera: 

<pre>CONST nombre_constante = valor</pre> El valor que se le asigne a la variable no podrá alterarse. 

### Ejemplos de código relacionados

*   [Cómo definir una constante en VBScript][1]
*   [Comentar código en VBScript][2]

 [1]: http://lineadecodigo.com/vbscript/como-definir-una-constante-en-vbscript/ "Como definir una variable en VBScript"
 [2]: http://lineadecodigo.com/vbscript/comentar-codigo-en-vbscript/ "Comentar código en VBScript"