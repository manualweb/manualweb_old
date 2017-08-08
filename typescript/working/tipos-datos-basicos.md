# Tipos Datos Básicos


Una de las principales característias de [TypeScript][1] es que las variables son tipadas. De esta manera en el momento de la codificación podemos realizar comprobaciones de tipo.

Para poder asignar un tipo a una variable en [TypeScript][1] utilizaremos el siguiente código:

~~~javascript
let variable:tipo = valor
~~~

Por ejemplo si queremos crear una variable que sea una cadena de texto, escribiremos lo siguiente:

~~~javascript
let cadena:string = 'hola'
~~~

Aquí ya vemos que `string` es el tipo de dato que representa una cadena de texto.

Dentro de [TypeScript][1] podemos encontrar los siguientes tipos de datos básicos:

* Booleanos
* Number
* String
* Array
* Tuplas
* Enumerados
* Any
* Void
* Null y Undefined
* Never

## Booleanos
Es el tipo de dato que representa un valor `true`o `false`. Para definir una variable en [TypeScript][1] de tipo booleano escribiremos lo siguiente:

~~~javascript
let mivariable:boolean = false;
~~~

En este caso hemos definido la variable `mivariable`de tipo booleano, y con el valor `false`.

## Number
Como en [Javascript][2] dentro de [TypeScript][1] todos los números se definen en forma de coma flotante.

Así podremos tener como números los decimales, hexadecimales, octales y binarios. Para definir una variable de tipo number escribiremos lo siguiente:

~~~javascript
let variable:number = valor;
~~~

Así podremos tener las siguientes definiciones de números en [TypeScript][1]:

~~~javascript
let decimal:number = 9;
let hexadecimal:number = 0xf00d;
let octal:number = 0o744;
let binario:number = 0b1110;
~~~

## String
Para representar a las cadenas de texto tenemos el tipo de dato `string`. Las cadenas de texto son conjuntos de carácteres delimitados por comillas simples o complejas.

Para definir una variable de tipo `string` utilizaremos la siguiente estructura:

~~~javascript
let cadena:string = 'valor';
~~~

Así podremos definir las siguientes variables:

~~~javascript
let saludo:string = "Hola Mundo";
let nombre:string = 'Carmen';
~~~

## Array
Nos permite definir una lista (o array) de elementos de un tipo en concreto. Para definir un array en [TypeScript][1] podemos hacerlo de dos formas:

La primera será indicando el tipo de elemento que almacena seguida del operador `[]`.

~~~javascript
let miarray: number[] = [1,2,3,4,5];
~~~

En el segundo caso utilizaremos la clase `Array`:

~~~javascript
let miarray: Array<number> = [1,2,3,4,5];
~~~

Para acceder al `Array` simplemente deberemos de acceder al elemento en cuestión mediante el operador `[]`.

~~~javascript
miarray[2]; // Acceso al elemento de la tercera posición
~~~


## Tuplas
Una tupla es un array que tiene los elementos que contiene tipados. De esta manera, cuando intentemos insertar un elemento sobre la tupla, se hará la comprobación en tiempo de compilación de que los tipos son compatibles.

Para definir una tupla lo haremos de la siguiente manera:

~~~javascript
let variable:[tipo1,tipo2];
~~~

Por ejemplo podemos definir una tupla de una cadena y un número de la siguiente forma:

~~~javascript
let x:[string,number];
x = ["texto",3];
~~~

## Enumerados
Un enumerado nos sirve para poder dar valores identificables a un conjunto de valores. Para definir un enumerado en [TypeScript][1] utilizaremos la sentencia `enum`.

~~~javascript
enum Enumerado {valor1,valor2,valor3,...,valorN};
~~~

Por ejemplo podemos definir un enumerado de colores de la siguiente manera:

~~~javascript
enum Color {Rojo,Verde,Azul};
~~~

Para poder utilizar el enumerado simplemente definimos una variable del tipo del enumerado.

~~~javascript
let c:Color = Color.Rojo;
~~~

Los enumerados tienen un valor numérico que empieza en 0 y se va incrementando de forma unitaria a los siguientes valores. De esta manera, si volcamos el contenido de `Color.Rojo` por consola, veremos que se nos muestra un 0.

Si queremos asignar un valor de otra forma deberemos de hacerlo indicando el valor asignado a cada uno de los enumerados en la creación.

~~~javascript
enum Color {Rojo=14,Verde=16,Azul=18};
~~~

Además podemos acceder al valor textual que tiene el enumerado utilizando el operador `[]` de la siguiente manera:

~~~javascript
let c:string = Color[2]
console.log(c)
~~~

## Any
El hecho de que [TypeScript][1] sea un lenguaje tipado hace que todas las variables tengan que estar tipadas. Si bien puede ser que no sepamos el tipo de una determinada variable o que este vaya a cambiar con el paso del tiempo. En este caso podremos definir dicha variable del tipo `Any` de la siguiente forma:

~~~javascript
let variable:any = valor;
~~~

Así una variable `Any` puede cambiar con el paso del tiempo:

~~~javascript
let x:any = 3;
console.log(x);

x = 'soy una cadena de texto';
console.log(x);

x = true;
console.log(x);
~~~

## Void
El tipo `void`se utilizará para aquellas funciones que no devuelvan ningún valor. Por ejemplo, imaginemos que hay una función que simplemente vuelca un contenido a consola. La definiremos de la siguiente forma utilizando un tipo de dato básico `void`.

~~~javascript
function alerta(texto:string): void {
  console.log(texto);
}
~~~

## Null y Undefined
Estos tipos están definidos por `null` y `undefined`. Ambos tipos son subtipos del resto de tipos. Es por ello que una variable de tipo `string` puede tener en un determinado momento un valor `null`.

## Never
El tipo de dato `never` representa a aquellos valores que nunca existen. Por ejemplo, pueden ser retorno de una función que lance una excepción. Como nunca va a exitir un retorno, se puede definir que el valor de retorno de la función es `never`.

## Forzar el tipo de la variable (Type Assertion)
Hay una forma en [TypeScript][1] en la cual podemos forzar el tipo de la variable. En este caso es el programador el que está indicando el valor que va a tener dicha variable y por lo tanto será utilizado por el compilador para ignorar las comprobaciones.


Por ejemplo podríamos forzar en código a que una variable de tipo `any` en algún momento fuese utilizada como `string`.

Hay dos formas de forzar el tipo de varible. La primera es mediante el operador `<>` y la segunda es utilizando la sentencia `as`.




[1]: http://www.manualweb.net/tutorial-typescript/
[2]: http://www.manualweb.net/tutorial-javascript/
