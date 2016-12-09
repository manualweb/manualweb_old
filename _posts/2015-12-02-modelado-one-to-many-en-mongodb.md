---
ID: 677
post_title: '09.02 &#8211; Modelado One-to-Many en MongoDB'
author: Víctor Cuervo
post_date: 2015-12-02 18:00:11
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/mongodb/modelado-one-to-many-en-mongodb/
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
En el caso del modelado one-to-many en <a href="http://www.manualweb.net/tutorial-mongodb/">MongoDB</a> vamos a partir de dos entidades de datos en las cuales por cada instancia de la entidad demarcada con la cardinalidad unitaria existen N elementos de la entidad de cardinalidad N.

Un ejemplo de entidades de datos para un modelado one-to-many en <a href="http://www.manualweb.net/tutorial-mongodb/">MongoDB</a> sería la entrada de un blog y los comentarios que se realicen sobre la entrada del blog.

<a href="http://www.manualweb.net/wp-content/uploads/2015/12/relacion1_n.png"><img class="aligncenter wp-image-679 size-medium" src="http://www.manualweb.net/wp-content/uploads/2015/12/relacion1_n-300x57.png" alt="relacion1_n" width="300" height="57" /></a>

En este caso los documentos JSON con los que contamos serán, por un lado la entrada del blog:

<pre lang="javascript">{
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar"
}</pre>

Y por otro los N comentarios que existan:

<pre lang="javascript">{
  name: “Daniel Hernandez",
  created_on: ISODate("2015-12-01T10:01:22Z"),
  comment: “Me gusta tu blog"
}

{
  name: “Fran Honrubia",
  created_on: ISODate("2015-12-01T14:15:10Z"),
  comment: “Gran trabajo"
}</pre>

Las estrategias para modelar la relación one-to-many son tres. Por un lado podemos realizar, al igual que sucedía con el modelado one-to-one una estrategia de <strong>embedding</strong> y de <strong>linking</strong>. Y en este caso tenemos otra estrategia que complementa las dos anteriores que se llama <strong>bucketing</strong>.
<h3>One-to-Many. Embedding</h3>
En este caso vamos a tener una sola colección de documentos que será la de los post. Por cada una de las entradas del blog tendremos anidados tantos comentarios como se vayan realizando.

Los comentarios se modelarán mediante un array de documentos.

<pre lang="javascript">{
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar",
  comments: [
    {
      name: “Daniel Hernandez",
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

La parte positiva de un modelado one-to-many en <a href="http://www.manualweb.net/tutorial-mongodb/">MongoDB</a> <strong>mediante una estrategia de embedding es que una sola consulta nos va a recuperar todos los comentarios asociados a la entrada del blog</strong>.

<pre lang="javascript">db.post.find({title:”Línea de Código”},{comments:1});</pre>

Si bien, como contraprestación negativa tenemos que tener cuidado con:
<ul>
	<li>No superar el <strong>tamaño máximo del documento que es de 16 MB.</strong></li>
	<li>El rendimiento de la escritura. Al ir añadiendo subdocumentos al array <a href="http://www.manualweb.net/tutorial-mongodb/">MongoDB</a> tiene que ir calculando el padding del documento y puede impactar en el rendimiento de la escritura.</li>
	<li>Si tenemos muchos comentarios no podremos pedirles de forma paginada ya que la consulta nos devolverá todos los documentos. Así que la paginación quedará de mano de la aplicación.</li>
</ul>
<h3>One-to-Many. Linking</h3>
En este caso vamos a crear una clave en la entidad del Blog y utilizaremos esta clave como foreing key en los comentarios. De esta forma tendremos por un lado la entrada del blog:

<pre lang="javascript">{
  _id:1,
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar"
}</pre>

Y por otro lado cada uno de los comentarios con el _id como foreing key.

<pre lang="javascript">{
  blog_entry: 1,
  name: “Daniel Hernandez",
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

<pre lang="javascript">var post_id = db.post.find({title:”Línea de Código”},{_id:1});
  db.comments.find({blog_entry: post_id}).foreach(doc) {
    print (doc.name + doc.comment)
}</pre>

<h3>One-to-Many. Bucketing</h3>
La estrategia de Bucketing es una estrategia intermedia entre la estrategia de embedding y la estrategia de linking. La idea es crear una colección dónde vayamos insertando los documentos, si bien, esta colección tendrá un tamaño máximo y reducido. De esta manera evitamos los problemas de padding y reposicionamiento.

La colección de bucketing estará enlazada a la entidad blog mediante una estrategia de linking.

Así, tendremos primero la colección de post:

<pre lang="javascript">{
  _id:1,
  title: “Línea de Código",
  url: “http://lineadecodigo.com",
  text: “Aprende a Programar"
}</pre>

Y luego cada uno de los “buckets”:

<pre lang="javascript">{
  blog_entry: 1,
  page: 1,
  comments: [
    {
      name: “Daniel Hernandez",
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

Una de las cosas que hay que hacer es identificar el indicador a utilizar en la estrategia de bucketing. Puede ser el número de página de comentarios (utilizado en el ejemplo) o cualquier otro indicador, por ejemplo la fecha. Siempre hay que buscar un indicador que los distribuya lo más uniformemente.

A la hora de realizar la consulta habrá que utilizar el indicador que hayamos puesto en el “bucket”.

<pre lang="javascript">var post_id = db.post.find({title:”Línea de Código”},{_id:1});
var pageid = 2;
db.comments.find({blog_entry: post_id, page=pageid}).foreach(doc) {
  print (doc.name + doc.comment)
}</pre>