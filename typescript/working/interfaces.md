
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



  let p1 = {nombre:"Carmen", edad:38};

  datosPersona(p1);




[1]: http://www.manualweb.net/tutorial-typescript/
[2]: http://www.manualweb.net/tutorial-javascript/
