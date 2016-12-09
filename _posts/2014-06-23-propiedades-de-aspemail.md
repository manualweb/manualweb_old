---
ID: 567
post_title: Propiedades de AspEmail
author: Víctor Cuervo
post_date: 2014-06-23 01:37:21
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/aspemail/propiedades-de-aspemail/
published: true
---
Las propiedades del componente AspEmail son las siguientes:

<strong>Host: String</strong>
Indica el nombre del servidor SMTP que vamos a utilizar para mandar mensajes. Por ejemplo, nuestro servidor SMTP puede ser mail.lineadecodigo.com.

<strong>Port: String</strong>
El puerto que estemos utilizando para el servidor SMTP. Por defecto es el puerto 25.

<strong>From: String</strong>
Dirección de email del usuario que manda el mensaje.

<strong>FromName: String</strong>
Nombre que hace referencia a la dirección email del usuario que manda el mensaje. Por ejemplo, el From podría ser "webmaster@lineadecodigo.com", mientras que el FromName sería "El Webmaster de Linea de Codigo"

<strong>Subject: String</strong>
Sería el tema del mensaje.

<strong>Body:String</strong>
Cuerpo del mensaje.

<strong>IsHtml: Boolean</strong>
Propiedad que indica si el mensaje que vamos a mandar está en formato HTML o no. Por defecto el valor es false, es decir, que el mensaje no se envía como página web.

<strong>Priority: String</strong>
Indica la prioridad del mensaje. Sus posibles valores son 0 (sin especificar), 1 (alta), 3 (normal) y 5 (baja). Por defecto está sin especificar.

<strong>Helo: String</strong>
Cuando se establece una conexión con el servidor SMTP por defecto se le envía la palabra "HELO", mediante esta propiedad podemos indicarle otra palabra.

<strong>ContentTransferEncoding As String</strong>
Indica el tipo de codificación que se va a realizar en los contenidos de la cabecera. Por defecto es "7bit".

<strong>CharSet As String</strong>
Especifica el conjunto de caracteres usados en la cabecera Content-Type. Por defecto es "ISO-8859-1".

<strong>Timestamp:Date</strong>
Indica cuando debe de ser enviado el mensaje. Este mensaje se encontrará en una cola de mensajes. Para enviar el mensaje a una cola de mensajes usaremos el método SendToQueue.

<strong>UserName: String</strong>
Si el servidor SMTP requiere de autentificación mediante esta propiedad le indicaremos el nombre de usuario.

<strong>Password: String</strong>
La misma autentificación requerirá de una password, la cual indicaremos a través de esta propiedad.

<strong>Timeout: Long</strong>
Sirve para especificar el tiempo de espera del socket de conexión.

<strong>AltBody: String</strong>
En el caso de que estemos enviando un texto HTML como cuerpo del mensaje, tenemos la posibilidad de especificar un texto alternativo mediante esta propiedad. Dicho texto será un texto plano, el cual vendrá bien si el cliente que recibe el mensaje no puede visualizar mensajes en modo HTML.

<strong>Expires: Date</strong>
Es una propiedad de solo lectura, la cual nos devuelve la fecha en la cual termina la licencia del software AspEMail