---
ID: 1477
post_title: 18 – Entidades en HTML
author: Víctor Cuervo
post_date: 2017-04-15 18:32:44
post_excerpt: ""
layout: post
permalink: http://www.manualweb.net/html/entidades-html/
published: true
nombreforo: HTML
urlforo: http://dudasprogramacion.com/html
urlmanual: http://www.manualweb.net/tutorial-html/
urltest: http://www.testprogramacion.com/html
urlcurso: http://www.aulaprogramacion.com/curso-html/
urlvideo: PLLVIhySQmrVaaLfsbi9VHVffq3Kk8KAST
urlejemplos: http://lineadecodigo.com/tag/html-entidades/feed/
gitfolder: html
---
Cuando estemos insertando texto en nuestros documentos HTML puede darse el caso de que necesitemos insertar símbolos. Bien ya sean símbolos de la codificación que estemos utilizando o símbolos de carácter general. Esto pueden ser monedas, símbolos de puntuación,...

Para ello HTML nos ofrece las entidades. Las entidades son unas estructuras que, mediante el uso de una codificación, nos permiten representar un símbolo.

La estructura de la entidad HTML es un ampersand seguido del código o nombre de la entidad y terminado en un punto y coma.

~~~html
&codigo;
~~~

En el caso de que utilicemos los códigos, estos se anteponen de una almohadilla.

Algunos de las entidades más utilizadas son los acentos:

~~~html
á	&aacute;
é	&eacute;
í	&iacute;
~~~

Los símbolos que utiliza el propio lenguaje HTML:

~~~html
&	&amp;
<	&lt;
>	&gt;
~~~

U otros comunes:

~~~html
€	&euro;
£	&pound;
©	&copy;
®	&reg;
~~~

### Principales entidades HTML

| Carácter | Código | Entidad | Carácter | Código | Entidad |
| -------- | ------ | ------- | -------- | ------ | ------- |
| !        | !      | --      | "        | "      | --      |
| #        | #      | --      | $        | $      | --      |
| %        | %      | --      | &        | &      | --      |
| '        | '      | --      | (        | (      | --      |
| )        | )      | --      | *        | *      | --      |
| +        | +      | --      | ,        | ,      | --      |
| -        | -      | --      | .        | .      | --      |
| /        | /      | --      | :        | :      | --      |
| ;        | ;      | --      | <        | <      | --      |
| =        | =      | --      | >        | >      | --      |
| ?        | ?      | --      | @        | @      | --      |
| [        | [      | --      |          | \      | --      |
| ]        | ]      | --      | ^        | ^      | --      |
| _        | _      | --      | `|`      | --     |         |
| {        | {      | --      |          |        | | | --  |
| }        | }      | --      | ~        | ~      | --      |
|          |        | nbsp    | ¡        | ¡      | iexcl   |
| ¢        | ¢      | cent    | £        | £      | pound   |
| ¤        | ¤      | curren  | ¥        | ¥      | yen     |
| ¦        | ¦      | brvbar  | §        | §      | sect    |
| ¨        | ¨      | uml     | ©        | ©      | copy    |
| ª        | ª      | ordf    | «        | «      | laquo   |
| ¬        | ¬      | not     |          | ­      | shy     |
| ®        | ®      | reg     | ¯        | ¯      | macr    |
| °        | °      | deg     | ±        | ±      | plusmn  |
| ²        | ²      | sup2    | ³        | ³      | sup3    |
| ´        | ´      | acute   | µ        | µ      | micro   |
| ¶        | ¶      | para    | ·        | ·      | middot  |
| ¸        | ¸      | cedil   | ¹        | ¹      | sup1    |
| º        | º      | ordm    | »        | »      | raquo   |
| ¼        | ¼      | frac14  | ½        | ½      | frac12  |
| ¾        | ¾      | frac34  | ¿        | ¿      | iquest  |
| À        | À      | Agrave  | Á        | Á      | Aacute  |
| Â        | Â      | Acirc   | Ã        | Ã      | Atilde  |
| Ä        | Ä      | Auml    | Å        | Å      | Aring   |
| Æ        | Æ      | AElig   | Ç        | Ç      | Ccedil  |
| È        | È      | Egrave  | É        | É      | Eacute  |
| Ê        | Ê      | Ecirc   | Ë        | Ë      | Euml    |
| Ì        | Ì      | Igrave  | Í        | Í      | Iacute  |
| Î        | Î      | Icirc   | Ï        | Ï      | Iuml    |
| Ð        | Ð      | ETH     | Ñ        | Ñ      | Ntilde  |
| Ò        | Ò      | Ograve  | Ó        | Ó      | Oacute  |
| Ô        | Ô      | Ocirc   | Õ        | Õ      | Otilde  |
| Ö        | Ö      | Ouml    | ×        | ×      | times   |
| Ø        | Ø      | Oslash  | Ù        | Ù      | Ugrave  |
| Ú        | Ú      | Uacute  | Û        | Û      | Ucirc   |
| Ü        | Ü      | Uuml    | Ý        | Ý      | Yacute  |
| Þ        | Þ      | THORN   | ß        | ß      | szlig   |
| à        | à      | agrave  | á        | á      | aacute  |
| â        | â      | acirc   | ã        | ã      | atilde  |
| ä        | ä      | auml    | å        | å      | aring   |
| æ        | æ      | aelig   | ç        | ç      | ccedil  |
| è        | è      | egrave  | é        | é      | eacute  |
| ê        | ê      | ecirc   | ë        | ë      | euml    |
| ì        | ì      | igrave  | í        | í      | iacute  |
| î        | î      | icirc   | ï        | ï      | iuml    |
| ð        | ð      | eth     | ñ        | ñ      | ntilde  |
| ò        | ò      | ograve  | ó        | ó      | oacute  |
| ô        | ô      | ocirc   | õ        | õ      | otilde  |
| ö        | ö      | ouml    | ÷        | ÷      | divide  |
| ø        | ø      | oslash  | ù        | ù      | ugrave  |
| ú        | ú      | uacute  | û        | û      | ucirc   |
| ü        | ü      | uuml    | ý        | ý      | yacute  |
| þ        | þ      | thorn   | ÿ        | ÿ      | yuml    |
