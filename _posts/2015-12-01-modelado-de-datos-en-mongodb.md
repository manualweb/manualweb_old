---
ID: 666
post_title: '09 &#8211; Modelado de Datos en MongoDB'
author: Víctor Cuervo
post_date: 2015-12-01 18:59:00
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/mongodb/modelado-de-datos-en-mongodb/
published: true
nombreforo:
  - MongoDB
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
descargar:
  - >
    https://github.com/victorcuervo/manualweb_mongodb
errorcodigo:
  - >
    https://github.com/victorcuervo/manualweb_mongodb/issues
---
Cuando estamos modelando entidades de datos en un modelo ER existen una serie de patrones de modelización enfocados a evitar la redundancia, proteger la integridad de los datos,... estos son conocidos como las <strong>formas normales</strong>, y van desde la <strong>1FN</strong> hasta la <strong>5FN</strong>.

Cuando utilizamos un modelo NOSQL basado en documentos, como es el caso del modelado de datos en <a href="http://www.manualweb.net/tutorial-mongodb/">MongoDB</a>, la forma de modelar las relaciones entre las entidades cambia. Ya que existen una serie de conceptos básicos diferentes a los modelos ER que deberemos de tener en cuenta en el modelado como son: ausencia de joins, no existencia de modelos two-phase-commit y acceso atómico a los datos.

Así que vamos a ver cómo podemos modelar las tres relaciones típicas entre entidades de datos:
<ul>
	<li>Modelado one-to-one (1:1)</li>
	<li>Modelado one-to-many (1:N)</li>
	<li>Modelado many-to-many (N:M)</li>
</ul>