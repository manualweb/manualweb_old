## Arrays en TypeScript



### Desestructurar un Array
Desde ECMAScript 2015 se puede desestructurar un array. Esto consiste en convertir parte del contenido del array en variables simples de una forma sencilla.

De esta manera, partiendo de un array:

~~~javascript
let miarray:number[] = [1,2,3,4,5];
~~~

Podremos convertir sus elementos en variables de la siguiente forma:

~~~javascript
let [uno,dos, ..resto] = myarray
console.log(uno);
console.log(dos);
console.log(resto);
~~~

En las variables `uno` y `dos` tendremos los primeros valores, mientras que en `resto` tendremos el resto del array.

Esta técnica nos puede valer, por ejemplo, para hacer swapping de variables.

~~~javascript
let numeros:number[] = [1,2];
let [x,y] = numeros;

// Hacemos el Swapping
[x,y] = [y,x];

console.log(x);
console.log(y);
~~~


### Extender un array
Otra de las cosas que podemos hacer con un array es el componerlo a base de otros arrays. Para ello lo primero que haremos será definir dos arrays.

~~~javascript
let arr1 = [2,3];
let arr2 = [5,6];
~~~

Para realizar la extensión o composición del nuevo array a partir de estos dos arrays definidos vamos a utilizar la sintaxis `...` seguida del nombre del array.

~~~javascript
let numeros = [0,1, ...arr1, 4, ...arr2];
~~~

La sintaxis `...` es la misma que utilizabamos cuando deconstruiamos el array y dejábamos una variable para el resto de elementos.
