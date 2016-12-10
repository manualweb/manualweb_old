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
Si tuviésemos que explicar qué es [MongoDB][1] podríamos decir que es una **base de datos opensource NOSQL basada en documentos** desarrollada por la gente de [10gen][2]. Aunque una vez que cogió auge la base de datos[MongoDB][1] pasaron a llamarse con el mismo nombre y ahora *la empresa y el producto se llaman [MongoDB][1]*. El nombre de [MongoDB][1] proviene de *“hu**mongo**us”*, que significa enorme en inglés. [MongoDB][1] es una base de datos NOSQL, opensource, escrita en C++, escalable y de alto rendimiento. 
### MongoDB y los documentos El elemento principal de 

[MongoDB][1] es como almacena la información. [MongoDB][1] almacena toda la información en **documentos JSON**. <pre lang="javascript">{
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
}</pre> El almacenar la información en documentos JSON permite a 

[MongoDB][1] tener independencia del schema de almacenamiento, es decir, pueden existir más o menos campos en el documento dentro de una misma colección de documentos. Una de las cosas importantes de los documentos es que estos van tipados. Además los documentos nos permiten nuevas estructuras como arrays o subdocumentos que permitirán que de una sola consulta se recupere toda la información y evite así la necesidad de ejecutar consultas de tipo join. 
### Principales características de MongoDB Aunque en los siguientes capítulos iremos viendo en detalle todas las funcionalidades de 

[MongoDB][1], podríamos decir que las principales características de [MongoDB][1] son: 
#### Alto rendimiento El alto rendimiento para la persistencia en 

[MongoDB][1] se basa en dos puntos: La posibilidad de tener documentos con la información anidada, evitando, de esta forma, un número elevado de operaciones de I/O. Y el soporte de índices y la posibilidad de crear índices sobre arrays y subdocumentos. 
#### Alta disponibilidad

[MongoDB][1] proporciona alta disponibilidad mediante la réplica automática conocida como *replica set*, la cual proporciona redundancia de datos y failover automático, es decir, la transferencia automática a un nuevo nodo cuando se encuentra un fallo en uno de los nodos. 
#### Escalado Automático

[MongoDB][1] nos ofrece un escalado horizontal. Para ello el *sistema de sharding* nos permite distribuir información por diferentes cluster de máquinas.

 [1]: http://www.mongodb.org/
 [2]: http://www.mongodb.org