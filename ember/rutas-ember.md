

## Rutas Ember

Para crear una ruta deberemos de escribir el siguiente comando:

<kbd>$ember g route [nombre-ruta]</kbd>

Por ejemplo podríamos crear la ruta "saludo"

<kbd>$ember g route about</kbd>

<pre>installing route
  create app/routes/about.js
  create app/templates/about.hbs
updating router
  add route about
installing route-test
  create tests/unit/routes/about-test.js</pre>

Cuando ejecutamos la creación de la ruta, esta crea 3 ficheros:

* Una entrada en las rutas de Ember, dentro del fichero <code>/app/routes.js</code>
* Un fichero que contiene la ruta en <code>/app/routes/[nombre-ruta].js</code>
* Una plantilla asociada a la ruta en <code>/app/templates/[nombre-ruta].hbs</code>

Estos ficheros serán los que gestionen la navegación cuando el usuario acceda a <code>/[nombre-ruta]</code>






-----
[1]: http://www.manualweb.net/tutorial-ember/
[2]: https://babeljs.io/
[3]: https://nodejs.org/es/
[4]: https://www.npmjs.com/
[5]: http://www.manualweb.net/tutorial-html/
[6]: http://handlebarsjs.com/
[7]: http://www.manualweb.net/tutorial-javascript/
[8]: https://bower.io/
[9]: http://www.manualweb.net/tutorial-bootstrap/
[10]: http://www.manualweb.net/tutorial-css/
