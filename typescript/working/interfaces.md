
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




[1]: http://www.manualweb.net/tutorial-typescript/
[2]: http://www.manualweb.net/tutorial-javascript/
