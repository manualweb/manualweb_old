---
ID: 658
post_title: '09.01 &#8211; Modelado One-to-One en MongoDB'
author: Víctor Cuervo
post_date: 2015-12-01 18:31:08
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/mongodb/modelado-one-one-en-mongodb/
published: true
nombreforo:
  - MongoDB
descargar:
  - >
    https://github.com/victorcuervo/manualweb_mongodb
errorcodigo:
  - >
    https://github.com/victorcuervo/manualweb_mongodb/issues
urlforo:
  - >
    http://www.dudasprogramacion.com/forum/bases-de-datos/mongodb/
urlmanual:
  - >
    http://www.manualweb.net/tutorial-mongodb/
urltest:
  - http://www.testprogramacion.com/mongodb
urlcurso:
  - >
    http://www.aulaprogramacion.com/curso-mongodb
urlcharla:
  - >
    https://www.facebook.com/groups/mongodb.es/
urlvideo:
  - >
    https://www.youtube.com/playlist?list=PLLVIhySQmrVZGA6RpEkZJEH3rQOrHbi_c
---
En este caso vamos a realizar un modelado one-to-one en [MongoDB][1], para ello vamos a utilizar las entidades Persona y Domicilio. Una persona tendrá asociado la dirección de un domicilio. Estas entidades las modelaríamos de la siguiente forma: [<img src="http://www.manualweb.net/wp-content/uploads/2015/12/image00-300x57.png" alt="image00" width="300" height="57" class="alignright size-medium wp-image-673" />][2] Los documentos JSON de ejemplo que representan a estas personas son, para el caso de la persona: 
<pre>{
  nombre: “Víctor Cuervo”,
  edad: 38
}</pre> Y para el caso del domicilio es: 

<pre>{
  calle: “Alcala, 15”,
  codigo: 28022,
  ciudad: “Madrid”
}</pre> Para resolver el modelado one-to-one tenemos dos estrategia. La primera será la de embedding, es decir, incrustar la entidad Domicilio dentro de la entidad Persona. La segunda será la de linking, en este caso se utilizará una foreing key para mantener las relaciones. 

### One-to-One Embedding En este primer caso insertamos el domicilio en la colección de personas. Será un subdocumento dentro de la persona. 

<pre>{
  nombre: “Víctor Cuervo”,
  edad: 38,
  dirección: {
    calle: “Alcala, 15”,
    codigo: 28022,
    ciudad: “Madrid”
  }
}</pre> Lo bueno de esta estrategia es que para recuperar el domicilio de una persona simplemente tendremos que realizar una única operación de consulta. 

<pre>db.personas.find({nombre:”Víctor Cuervo},{direccion:1})</pre>

### One-to-One. Linking En este caso vamos a crear una clave dentro de la colección de personas y posteriormente la utilizaremos como foreign key dentro de la colección de domicilios. El documento de la persona tendrá un id: 

<pre>{
  _id: 1,
  nombre: “Víctor Cuervo”,
  edad: 38
}</pre> Y ese id será utilizado dentro del documento del domicilio: 

<pre>{
  userid: 1,
  calle: “Alcala, 15”,
  codigo: 28022,
  ciudad: “Madrid”
}</pre> Para recuperar la información tendremos que realizar dos consultas. En la primera recuperaremos el id del usuario y con dicho id tendremos que acceder a la segunda colección a recuperar la dirección 

<pre>var id = db.personas.find({nombre:”Víctor Cuervo},{_id:1})
db.domicilios.find({username:id})</pre> El modelo de linking sería el más parecido a los modelo ER. Si bien 

**es preferible aplicar una estrategia de embedding para el modelado de relaciones One-to-One en [MongoDB][1]**.

 [1]: http://www.manualweb.net/tutorial-mongodb/
 [2]: http://www.manualweb.net/wp-content/uploads/2015/12/image00.png