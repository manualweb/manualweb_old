
## Interfaces en TypeScript

Una de las principales características de [TypeScript][1] es el ser un lenguaje tipado. Es decir, las variables que definamos tienen que tener un tipo.



¿Para qué nos sirven los interfaces?

### Definir un Interface

Para definir un interface utilizamos la sentencia `interface` seguida del nombre del interface.

~~~javascript
interface nombreInterface { ... }
~~~

Dentro del interface definiremos las propiedades que lo componen, con su tipo asociado.

~~~javascript
interface nombreInterface {
  propiedad1: tipo-dato;
  propiedad2: tipo-dato;
}
~~~

Por ejemplo podremos definir un interface Persona en el cual aparezcan dos propiedades referidas al nombre y la edad.

~~~javascript
interface Persona {
  nombre: string;
  edad: number;
}
~~~

Una vez que tenemos definido el inteface, este lo podemos utilizar para controlar el tipo de datos que pasamos a las funciones. En este caso podríamos definir una función cuyo dato de entrada tuviese que cumplir con el interface.

~~~javascript
function datosPersona(p: Persona) {
  console.log("La persona se llama " + p.nombre + ".");
  console.log("Y tiene " + p.edad + " años.");
}
~~~

Vemos que los tipos de datos que contengan estos dos atributos. Obligatoriamente ambos atributos. Podrán utilizarse para invocar a la función.

Definamos una serie de objetos con atributos:

~~~javascript
let p1 = {nombre:"Carmen", edad:38};
datosPersona(p1);

let p2 = {nombre:"David", edad:22, ciudad:"Salamanca"};
datosPersona(p2);

let p3 = {nombre:"Rocío"};
datosPersona(p3); // error
~~~

Cualquier objeto que, al menos, contenga estas dos propiedades va a funcionar. No es el caso del objeto `p3` que solo contiene una de ellas.

### Interface Propiedades Opcionales
Puede ser que todas las propiedades del interface no sean necesarias. Es por ello que podemos definir propiedades que sean opcionales.

En este caso deberemos de añadir el operador `?` detrás del nombre de la propiedad.

~~~javascript
interface nombreInterface {
  propiedad1?: tipo-dato;
  propiedad2?: tipo-dato;
}
~~~

Así, si volvemos a nuestro interface `Persona` podemos indicar que la propiedad `edad` sea opcional de la siguiente forma:

~~~javascript
interface Persona {
  nombre: string;
  edad?: number;
}
~~~

De esta forma, el objeto definido con solo el nombre funcionará al invocar a la función `datosPersona`.

~~~javascript
function datosPersona(p: Persona) {
  console.log("La persona se llama " + p.nombre + ".");
  if (p.edad)
    console.log("Y tiene " + p.edad + " años.");
}

let p3 = {nombre:"Rocío"};
datosPersona(p3);
~~~

### Interface propiedades solo lectura
Con [TypeScript][1] podemos definir interfaces que tengan propiedades de solo lectura. Es decir, que una vez creado el objeto no podamos modificar el valor de sus propiedades.

Para definir una propiedad de solo lectura deberemos de utilizar `readonly` delante de la propiedad del interface.

~~~javascript
interface nombreInterface {
  readonly propiedad: tipo-dato;
}
~~~

Por ejemplo podemos definir el siguiente interface `Rectangulo`.

~~~javascript
interface Rectangulo {
  readonly alto:number;
  readonly ancho:number;
}
~~~

En el caso de que pasemos este interface a una función, veremos que no hay manera de modificar el contenido de sus propiedades.

~~~javascript
function area(r:Rectangulo): number {
  // No se puede asignar ya que es readonly y dará error
  r.alto = 10;  
  return r.alto*r.ancho
}
~~~

> Utilizaremos `readonly` dentro de las propiedades de un interface, mientras que utilizaremos `const` para las variables.

### Exceso de validación de los interfaces
El uso de los interfaces nos obliga a ser muy estrictos en la definición de las propiedades. Es por ello que el uso de propiedades no esperadas puede llegar a ser un problema en códigos extensos.

Es por ello que en [TypeScript][1] podemos saltarnos el exceso de validación de los interfaces de tres maneras:

#### Uso de Index Signature
La idea es definir una índice genérico dentro del interface sobre el que pueda ir cualquier tipo de variable.

~~~javascript
interface Cuadrado {
  lado: number;
  color?: string;
  [propName:string]: any;
}
~~~

De esta manera las propiedades que no sean `lado`, ni `color` se almacenarán en la genérica.

#### Forzar el tipo
Podemos forzar al tipo del interface mediante un type assertion.

~~~javascript
interface Circulo {
  radio: number;
  color?: string;
}

function calcularAreaCirculo(datos:Circulo): number {
  let a = 2*Math.PI*datos.radio;
  return a;
}

calcularAreaCirculo({radio:2,colour:'red'} as Circulo);
~~~

#### Usar una variable intermedia
En este caso bastará con asignar le objeto definido a una variable intermedia.

~~~javascript
interface Circulo {
  radio: number;
  color?: string;
}

function calcularAreaCirculo(datos:Circulo): number {
  let a = 2*Math.PI*datos.radio;
  return a;
}

let c1 = {radio:2,colour:'red'};
calcularAreaCirculo(c1);
~~~

## Interfaces para funciones
Otra de las capacidades que tenemos con los interfaces es realizar interfaces para funciones. La idea es que al definir un función en concreto esta cumpla con un interface.

Para definir **interfaces para funciones** deberemos de seguir la estructura:

~~~javascript
interface nombreInterface {
  (parametro1:tipo1, parametro2:tipo2,... parametroN:tipoN):tipo-retorno;  
}
~~~

Cómo vemos indicamos los parámetros que se le pasan, así como el tipo de datos de dichos parámetros y luego el tipo de dato que devolverá la función.

Por ejemplo podemos definir un interface para función que represente el cálculo de un área de un triángulo de la siguiente forma:

~~~javascript
interface CalculoAreaTriangulo {
  (base:number, altura:number):number;
}
~~~

Ahora definiremos la variable que implementará la función. Esta variable será del tipo definido por el interface:

~~~javascript
let miCalculo: CalculoAreaTriangulo;
~~~

Ahora simplemente deberemos de definir una función que cumpla dicha estructura. Por ejemplo la siguiente función:

~~~javascript
miCalculo = function(b:number,a:number) {
  return (b*a)/2;
}
~~~

## Interfaces de Tipos Indexables
Otro tipo de interfaces que podemos definir es para controlar elementos indexables, es decir, arrays.
Para poder definir un interface que tenga un tipo indexable utilizamos la siguiente estructura de `interface`:

~~~javascript
interface nombreInterface {
  [indice:tipo-indice]: tipo-retorno;
}
~~~

Dónde `tipo-indice` es el tipo por el cual accedemos al índice del array y el `tipo-retorno` es el tipo de dato que devuelve el array.

Por ejemplo si queremos definir un interface que sea accedido mediante un índice numérico y que devuelva una cadena codificaremos lo siguiente:

~~~javascript
interface ArrayCadenas {
  [index:number]: string;
}
~~~

Ahora lo que haremos será definir este interface en una variable:

~~~javascript
let nombres:ArrayCadenas;
~~~

Y le asignamos el array del tipo que hemos definido. En este caso una cadena:

~~~javascript
nombres = ['Víctor','Nacho','Marta'];

let n1:string = nombres[1];
console.log(nombre);
~~~

> El `tipo-indice` que soporta el interface de tipo índice solo será con tipos `string` y `number`.

Si utilizamos interfaces de tipos indexables que manejen un índice `string` hay que tener en cuenta que el tipo devuelto por el interface `number` debe de ser un subtipo del interface devuelto por el interface `string`.

Esto es debido a que ambos índices van a ser tratados como cadenas en [Javascript][2], por lo tanto deberán de devolver algo consistente.

Además en los interfaces de tipos indexables podemos conseguir que la colección sea solo lectura indicando que el índice sea `readonly`.

~~~javascript
interface ArrayCadenas {
  readonly [index:number]: string;
}
~~~

## Interfaces para clases
Hasta ahora hemos visto el uso de interfaces para poder controlar los datos que pasamos en una función, la función en si misma o para definir una colección o array.

Pero si vienes del mundo de la orientación a objetos sabrás que el uso típico del **interface** es el de servir como contrato de una clase.

Lo que conseguimos es que la clase implemente aquello que tenga definido el **interface**.

Así, si tenemos un **interface** `Figura`:

~~~javascript
interface Figura {
  area:number;
  setArea(area:number);
}
~~~

Podemos hacer que una clase lo implemente utilizando la sentencia `implements`:

~~~javascript
class Cuadrado implements Figura {
  area:number;
  setArea(a:number){
    this.area = a;
  }
}
~~~

Para que la clase `Cuadrado` sea correcta, esta deberá de contener todas las propiedades y funciones definidas en el **interface**.

## Extender Interfaces
Al igual que las clases, en [TypeScript][1] se pueden extender los **interfaces**. De esta manera podemos incluir las definiciones de propiedades y funciones definidas dentro de un interface en otros.

Para extender un interface en [TypeScript][1] utilizaremos la sentencia `extends`.

Así, definimos nuevamente nuestro **interface** `Figura`:

~~~javascript
interface Figura {
  area:number;
}
~~~

Y podemos definir un **interface** `Cuadrado` que extienda de `Figura`:

~~~javascript
interface Cuadrado extends Figura {
  lado:number;
}
~~~

Incluso, un **interface** puede extender de varios interfaces. De esta manera si tenemos el **interface** `Borde`:

~~~javascript
interface Borde {
  colorBorde:string;
  anchoBorde:string;
}
~~~

Podemos definir el **interface** Cuadrado extendiendo de este también:

~~~javascript
interface Cuadrado extends Figura, Borde {
  lado:number;
}

let cd1 = <Cuadrado>{};
cd1.lado = 2;
cd1.area = 4;
cd1.colorBorde = 'black';
~~~

## Interfaces extendiendo de clases
Aunque lo más normal sea que trabajemos con Clases que extienden de interfaces, vamos a ver cómo podemos extender un interfaces a partir de una clase.

En este caso el **interface** solo va a extender sus miembros, pero no la implementación. Extenderá todos los tipos de miembros de la clase, incluidos protegidos y privados.

A la hora de crear interfaces extendiendo de clases lo que conseguimos es que el interface solo sea implementado por esa clase o por una subclase del mismo.

De esta manera podemos tener una **clase** que represente un borde:

~~~javascript
class Borde {
  anchoBorde:number;
  colorBorde:string;
}
~~~

Y ahora definimos un interface que la extienda:

~~~javascript
interface FiguraConBorde extends Borde {
  cambiarColor(color:string);
}
~~~

Una vez que utilicemos el interface `FiguraConBorde` como implementación de una clase, lo que estamos diciendo es que esta clase deberá de ser obligatoriamente una extensión de la clase `Borde`:

~~~javascript
class Figura extends Borde implements FiguraConBorde {
  area:number;
  cambiarColor(c:string) {
    this.colorBorde = c;
  }
}
~~~

De esta manera estamos consiguiendo poner un poco control en herencias complejas dentro de clases.







[1]: http://www.manualweb.net/tutorial-typescript/
[2]: http://www.manualweb.net/tutorial-javascript/
