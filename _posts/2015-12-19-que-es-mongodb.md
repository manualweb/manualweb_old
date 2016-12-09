---
ID: 636
post_title: '01 &#8211; ¿Qué es MongoDB?'
author: Víctor Cuervo
post_date: 2015-12-19 09:00:27
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/mongodb/que-es-mongodb/
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
Si tuviésemos que explicar qué es <a href="http://www.mongodb.org/">MongoDB</a> podríamos decir que es una <strong>base de datos opensource NOSQL basada en documentos</strong> desarrollada por la gente de <a href="http://www.mongodb.org">10gen</a>. Aunque una vez que cogió auge la base de datos<a href="http://www.mongodb.org/">MongoDB</a> pasaron a llamarse con el mismo nombre y ahora <em>la empresa y el producto se llaman <a href="http://www.mongodb.org/">MongoDB</a></em>.

El nombre de <a href="http://www.mongodb.org/">MongoDB</a> proviene de <em>“hu<strong>mongo</strong>us”</em>, que significa enorme en inglés.

<a href="http://www.mongodb.org/">MongoDB</a> es una base de datos NOSQL, opensource, escrita en C++, escalable y de alto rendimiento.
<h3>MongoDB y los documentos</h3>
El elemento principal de <a href="http://www.mongodb.org/">MongoDB</a> es como almacena la información. <a href="http://www.mongodb.org/">MongoDB</a> almacena toda la información en <strong>documentos JSON</strong>.

<pre lang="javascript">{
  web: “Manual Web”,
  url: “http://www.manualweb.net”,
  description: “Tutoriales sobre Programación”,
  email: “contactar@manualweb.net”,
  lenguajes: [‘java’,’html5’,’javascript’,’mongodb’],
  social:
    {
      twitter: ‘manual_web’,
      facebook: ‘ManualWeb’
    }
}</pre>

El almacenar la información en documentos JSON permite a <a href="http://www.mongodb.org/">MongoDB</a> tener independencia del schema de almacenamiento, es decir, pueden existir más o menos campos en el documento dentro de una misma colección de documentos.

Una de las cosas importantes de los documentos es que estos van tipados.

Además los documentos nos permiten nuevas estructuras como arrays o subdocumentos que permitirán que de una sola consulta se recupere toda la información y evite así la necesidad de ejecutar consultas de tipo join.
<h3>Principales características de MongoDB</h3>
Aunque en los siguientes capítulos iremos viendo en detalle todas las funcionalidades de <a href="http://www.mongodb.org/">MongoDB</a>, podríamos decir que las principales características de <a href="http://www.mongodb.org/">MongoDB</a> son:
<h4>Alto rendimiento</h4>
El alto rendimiento para la persistencia en <a href="http://www.mongodb.org/">MongoDB</a> se basa en dos puntos: La posibilidad de tener documentos con la información anidada, evitando, de esta forma, un número elevado de operaciones de I/O. Y el soporte de índices y la posibilidad de crear índices sobre arrays y subdocumentos.
<h4>Alta disponibilidad</h4>
<a href="http://www.mongodb.org/">MongoDB</a> proporciona alta disponibilidad mediante la réplica automática conocida como <em>replica set</em>, la cual proporciona redundancia de datos y failover automático, es decir, la transferencia automática a un nuevo nodo cuando se encuentra un fallo en uno de los nodos.
<h4>Escalado Automático</h4>
<a href="http://www.mongodb.org/">MongoDB</a> nos ofrece un escalado horizontal. Para ello el <em>sistema de sharding</em> nos permite distribuir información por diferentes cluster de máquinas.