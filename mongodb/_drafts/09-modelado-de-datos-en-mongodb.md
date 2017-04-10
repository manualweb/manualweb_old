---
ID: 1315
post_title: '09 &#8211; Modelado de Datos en MongoDB'
author: Víctor Cuervo
post_date: 2017-04-10 23:21:56
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/?p=1315
published: false
slug:
  - tutorial-mongodb
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
Cuando estamos modelando entidades de datos en un modelo ER existen una serie de patrones de modelización enfocados a evitar la redundancia, proteger la integridad de los datos,... estos son conocidos como las **formas normales**, y van desde la **1FN** hasta la **5FN**. Cuando utilizamos un modelo NOSQL basado en documentos, como es el caso del modelado de datos en [MongoDB][1], la forma de modelar las relaciones entre las entidades cambia. Ya que existen una serie de conceptos básicos diferentes a los modelos ER que deberemos de tener en cuenta en el modelado como son: ausencia de joins, no existencia de modelos two-phase-commit y acceso atómico a los datos. Así que vamos a ver cómo podemos modelar las tres relaciones típicas entre entidades de datos: * Modelado one-to-one (1:1) * Modelado one-to-many (1:N) * Modelado many-to-many (N:M)

 [1]: http://www.manualweb.net/tutorial-mongodb/