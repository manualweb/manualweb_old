---
ID: 564
post_title: Introducción a AspEmail
author: Víctor Cuervo
post_date: 2014-06-23 01:35:14
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/aspemail/introduccion-aspemail/
published: true
---
AspEMail no es un objeto estándar dentro del lenguaje [ASP][1], si bien, su presencia en una gran cantidad de servidores me han impulsado a escribir este documento explicando el funcionamiento de dicho objeto. AspEMail es un objeto activo de servidor que nos va a servir para mandar mensajes de email utilizando un servidor SMTP, el cual podemos utilizar en nuestras páginas [ASP][1]. Es un objeto desarrollado por la empresa [Persits Software, Inc][2]. Para utilizar el objeto AspMail deberemos de crear una instancia del objeto Persits.MailSender utilizando el método CreateObject, método que utilizaremos siempre para crear instancias de objetos de servidor. 
<pre>Set Mail = Server.CreateObject("Persits.MailSender")</pre> Una vez que hemos creado el objeto AspEMail podremos utilizar sus métodos y atributos para realizar diferentes funcionalidades. Para descargarnos el software de AspEmail podemos hacerlo desde 

[http://www.aspemail.com/download.html][3]

 [1]: /tag/serverpages/asp/ "ASP"
 [2]: http://www.persits.com/ "Persits Software"
 [3]: http://www.aspemail.com/download.html "Descargarnos el Software de AspEmail"