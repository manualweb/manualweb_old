## Variables en TypeScript

Se verá el uso de `var`, `const` y `let`.

### var

¡¡¡¡ REVISAR EL CONTENIDO DEL TUTORIAL SOBRE VAR ¡¡¡

En [Javascript][2] las variables se declaran mediante la estructura:

~~~javascript
var nombre_variable = valor;
~~~

Por ejemplo podemos definir:

~~~javascript
var cantidad = 10;
~~~

Podemos definir variables dentro del ámbito de una función.

~~~javascript
function mifuncion(){
  var mivariable = 10;
  return mivariable;
}
~~~

.....

## let
La estructura de una definición de variables mediante `let` es:

~~~javascript
let nombre_variable = 'valor';
~~~

Por ejemplo podemos definir:

~~~javascript
let saludo = "Hola";
~~~

`let` aparece para resolver los problemas de ambito (scope) que se producian mediante la declaración de variables utilizando `var`.

### Ámbito de Bloque con let
Una variable definida mediante `let` solo es visible dentro de su bloque. Nunca en el bloque que la contiene u otro ámbito de bloque.

Por ejemplo, si echamos un vistazo al siguiente código:

~~~javascript
function mifuncion(validar:boolean) {

  let a = 1;

  if (validar) {
    // Se puede acceder a 'a' ya que es parte del bloque.
    let b = a + 1;
  }

  // Ya no hay acceso a la variable 'b'
  return b;
}
~~~

Vemos que la variable `b` está definida en un bloque superior, por lo cual no se tiene acceso desde el bloque que intenta devolverla.

### Redeclarar una variable let
Mientras que las variables de tipo `var` pueden declararse las veces que queramos, aunque siempre nos quedemos con la última...

~~~javascript
var x = 2;
var x = 3;
~~~

... para el caso de las variable `let` solo podremos declararlas una vez. Así el código...

~~~javascript
let x = 2;
let x = 3;
~~~

... daría un error.

## const
Mediante la clausula `const` podemos definir variables que no cambien de valor en todo el ciclo de vida del programa.

Para declarar una variable de tipo `const`lo haremos de la siguiente forma:

~~~javascript
const nombre_variable = valor;
~~~

Así podemos definir la siguiente constante:

~~~javascript
const mayor_de_edad = 18;
~~~

Su comportamiento en el ámbito de visibilidad es el mismo que se utiliza para las variables definidas mediante `let`.



[1]: http://www.manualweb.net/tutorial-typescript/
[2]: http://www.manualweb.net/tutorial-javascript/
