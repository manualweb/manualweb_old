---
ID: 569
post_title: Métodos en AspEmail
author: Víctor Cuervo
post_date: 2014-06-23 01:38:31
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/aspemail/metodos-en-aspemail/
published: true
---
Los métodos del componente AspEmail son los siguientes:

<strong>AddAddress (email: String, nombre: String)</strong>
Mediante este método podemos añadir direcciones de email a las cuales irá dirigido el mensaje. Sería lo que se conoce como el campo TO. Opcionalmente podemos indicarle un nombre a la dirección de email.

<strong>AddCC (email: String, nombre: String)</strong>
Mediante este campo añadiremos direcciones de email al campo Carbon Copy (campo de copia) del mensaje. El nombre de los email también, en este caso, es opcional.

<strong>AddBcc (email: String, nombre: String)</strong>
Añade direcciones de email al campo BCC (campo de copia oculta). Al igual que los dos casos anteriores el nombre del email es opcional.

<strong>AddReplyTo (email: String, nombre: String)</strong>
Este método nos permite añadir la dirección a la cual se podrá responder el mensaje. El nombre del email es opcional.

<strong>AddAttachment (directorio: String)</strong>
Nos permite añadir un fichero (attachment) al mensaje. Para ello simplemente debemos de indicarle el directorio donde se encuentra situado el fichero. Este método se suele utilizar conjuntamente con el objeto AspUpload.

<strong>AddCustomHeader (cabecera: String)</strong>
Nos permite añadir una cabecera estándar. Por ejemplo podemos añadirle la cabecera "Reply-To: Linea de Codigo &lt;webmaster@lineadecodigo.com&gt; ".

<strong>AddEmbededImage (directorio: String, contentID: String)</strong>
Añade una imagen (situada en un directorio) al cuerpo del mensaje, el cual deberá ser HTML. Para hacer uso de la imagen en el cuerpo del mensaje, deberemos de usar el contentID, el cual no debe de contener espacios. Por ejemplo &lt;img src="contentID"&gt;.

<strong>AppendBodyFromFile (directorio: String)</strong>
Crea el cuerpo del mensaje a partir de un fichero ya existente. El fichero puede ser de texto o HTML.

<strong>Send ()</strong>
Envía el mensaje que hemos creado. En el caso de que se produzca un error lanza una excepción con un código de error.

<strong>SendToQueue (directorio: String)</strong>
Puede ser que no nos interese mandar el mensaje directamente, sino que nos interese mandarlo a la cola de mensajes del servidor SMTP. En el caso de no indicar el directorio donde permanecerá temporalmente el mensaje, el agente del AspEmail utilizará el directorio configurado en él por defecto.

<strong>SendEncrypted (mensaje: CryptoMessage)</strong>
Nos permite mandar un mensaje encriptado. La encriptación debe de realizarse a través del objeto de servidor AspEncrypt.

<strong>SendSigned (mensaje: CryptoMessage)</strong>
Nos permite mandar un mensaje firmado digitalmente. Al igual que el método anterior necesitamos del objeto de servidor AspEncrypt.

<strong>SendSignedAndEncrypted (mensaje1: CryptoMessage, mensaje2: CryptoMessage)</strong>
Nos permite mandar un mensaje encriptado y firmado digitalmente. Volvemos a necesitar del objeto de servidor AspEncrypt.

<strong>SendToNewsgroup (grupoDeNoticias: String)</strong>
Nos sirve para mandar el mensaje a un grupo de noticias. Si utilizamos este método, los métodos AddAddresses serán ignorados. Además el host al cual enviamos el mensaje ya no tendrá que ser un servidor de email SMTP, sino que deberá de ser un servidor de noticias NNTP y el puerto de envío debe de ser el 119.

<strong>Reset ()</strong>
Borra los contenidos de las direcciones y de los attachments. De tal manera que podemos mandar un nuevo mensaje utilizando el mismo objeto.

<strong>ResetAll ()</strong>
Hace que las propiedades del objeto AspEMail vuelvan a tomar sus valores originales.

<strong>EncodeHeader (cabecera: String): String</strong>
Codifica una cadena de tetxo que contiene caracteres que no son ASCII de acuerdo a la RFC 1522. Devuelve la cadena codificada.

<strong>LogonUser (dominio: String, userID: String, password: String)</strong>
Puede darse el caso que debamos de identificarnos en alguna maquina, sobre todo cuando mandamos el mensaje a una cola de mensajes. Al método le pasamos el dominio al que pertenece la máquina, nuestro identificativo de usuario y la password.

<strong>RevertToSelf ()</strong>
Finaliza la identificación lanzada a través del método LogonUser.