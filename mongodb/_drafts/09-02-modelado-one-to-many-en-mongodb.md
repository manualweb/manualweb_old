---
ID: 1322
post_title: '09.02 &#8211; Modelado One-to-Many en MongoDB'
author: Víctor Cuervo
post_date: 2017-04-10 23:43:04
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1322
published: false
nombreforo:
  - MongoDB
urlforo:
  - >
    http://dudasprogramacion.com/bases-de-datos/mongodb
urlejemplos:
  - >
    http://lineadecodigo.com/categoria/mongodb/feed/
urlvideo:
  - PLLVIhySQmrVZGA6RpEkZJEH3rQOrHbi_c
urlmanual:
  - >
    http://www.manualweb.net/tutorial-mongodb/
urltest:
  - http://www.testprogramacion.com/mongodb
urlcurso:
  - >
    http://www.aulaprogramacion.com/curso-mongodb/
gitfolder:
  - mongodb
---
En el caso del modelado one-to-many en [MongoDB][1] vamos a partir de dos entidades de datos en las cuales por cada instancia de la entidad demarcada con la cardinalidad unitaria existen N elementos de la entidad de cardinalidad N. Un ejemplo de entidades de datos para un modelado one-to-many en [MongoDB][1] sería la entrada de un blog y los comentarios que se realicen sobre la entrada del blog.

[<img class="aligncenter wp-image-679 size-medium" src="http://www.manualweb.net/wp-content/uploads/2015/12/relacion1_n-300x57.png" alt="relacion1_n" width="300" height="57" />][2]

En este caso los documentos JSON con los que contamos serán, por un lado la entrada del blog:

<pre>{
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar"
}</pre>

Y por otro los N comentarios que existan:

<pre>{
  name: “Carlos Camacho",
  created_on: ISODate("2015-12-01T10:01:22Z"),
  comment: “Me gusta tu blog"
}

{
  name: “Fran Honrubia",
  created_on: ISODate("2015-12-01T14:15:10Z"),
  comment: “Gran trabajo"
}</pre>

Las estrategias para modelar la relación one-to-many son tres. Por un lado podemos realizar, al igual que sucedía con el modelado one-to-one una estrategia de **embedding** y de **linking**. Y en este caso tenemos otra estrategia que complementa las dos anteriores que se llama **bucketing**.

### One-to-Many.

Embedding En este caso vamos a tener una sola colección de documentos que será la de los post. Por cada una de las entradas del blog tendremos anidados tantos comentarios como se vayan realizando. Los comentarios se modelarán mediante un array de documentos.

<pre>{
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar",
  comments: [
    {
      name: “Carlos Camacho",
      created_on: ISODate("2015-12-01T10:01:22Z"),
      comment: “Me gusta tu blog"
    },
    {
      name: “Fran Honrubia",
      created_on: ISODate("2015-12-01T14:15:10Z"),
      comment: “Gran trabajo"
    }
  ]
}</pre>

La parte positiva de un modelado one-to-many en [MongoDB][1] **mediante una estrategia de embedding es que una sola consulta nos va a recuperar todos los comentarios asociados a la entrada del blog**.

<pre>db.post.find({title:”Línea de Código”},{comments:1});</pre>

Si bien, como contraprestación negativa tenemos que tener cuidado con:

*   No superar el **tamaño máximo del documento que es de 16 MB.**
*   El rendimiento de la escritura. Al ir añadiendo subdocumentos al array [MongoDB][1] tiene que ir calculando el padding del documento y puede impactar en el rendimiento de la escritura.
*   Si tenemos muchos comentarios no podremos pedirles de forma paginada ya que la consulta nos devolverá todos los documentos. Así que la paginación quedará de mano de la aplicación.

### One-to-Many. Linking

En este caso vamos a crear una clave en la entidad del Blog y utilizaremos esta clave como foreing key en los comentarios. De esta forma tendremos por un lado la entrada del blog:

<pre>{
  _id:1,
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar"
}</pre>

Y por otro lado cada uno de los comentarios con el _id como foreing key.

<pre>{
  blog_entry: 1,
  name: “Carlos Camacho",
  created_on: ISODate("2015-12-01T10:01:22Z"),
  comment: “Me gusta tu blog"
}

{
  blog_entry: 1,
  name: “Fran Honrubia",
  created_on: ISODate("2015-12-01T14:15:10Z"),
  comment: “Gran trabajo"
}</pre>

Al igual que pasaba en el modelado one-to-many vamos a tener que realizar una lectura por cada uno de los comentarios que tenga asociada la entrada del blog. Así, si hay 1000 comentarios en el blog deberemos de realizar 1000 lecturas. Si bien es verdad que permite realizar otras estrategias como la de paginación de comentarios, recuperando únicamente los necesarios.

<pre>var post_id = db.post.find({title:”Línea de Código”},{_id:1});
  db.comments.find({blog_entry: post_id}).foreach(doc) {
    print (doc.name + doc.comment)
}</pre>

### One-to-Many. Bucketing

La estrategia de Bucketing es una estrategia intermedia entre la estrategia de embedding y la estrategia de linking. La idea es crear una colección dónde vayamos insertando los documentos, si bien, esta colección tendrá un tamaño máximo y reducido. De esta manera evitamos los problemas de padding y reposicionamiento. La colección de bucketing estará enlazada a la entidad blog mediante una estrategia de linking. Así, tendremos primero la colección de post:

<pre>{
  _id:1,
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar"
}</pre>

Y luego cada uno de los “buckets”:

<pre>{
  blog_entry: 1,
  page: 1,
  comments: [
    {
      name: “Carlos Camacho",
      created_on: ISODate("2015-12-01T10:01:22Z"),
      comment: “Me gusta tu blog"
    },
    {}
  ]
}

{
  blog_entry: 1,
  page: 2,
  comments: [
    {
      name: “Fran Honrubia",
      created_on: ISODate("2015-12-01T14:15:10Z"),
      comment: “Gran trabajo"
    },
    {}
  ]
}</pre>

Una de las cosas que hay que hacer es identificar el indicador a utilizar en la estrategia de bucketing. Puede ser el número de página de comentarios (utilizado en el ejemplo) o cualquier otro indicador, por ejemplo la fecha. Siempre hay que buscar un indicador que los distribuya lo más uniformemente. A la hora de realizar la consulta habrá que utilizar el indicador que hayamos puesto en el “bucket”.

<pre>var post_id = db.post.find({title:”Línea de Código”},{_id:1});
var pageid = 2;
db.comments.find({blog_entry: post_id, page=pageid}).foreach(doc) {
  print (doc.name + doc.comment)
}</pre>

 [1]: http://www.manualweb.net/tutorial-mongodb/
 [2]: http://www.manualweb.net/wp-content/uploads/2015/12/relacion1_n.png