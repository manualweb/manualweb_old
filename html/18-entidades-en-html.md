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
|---|---|---|---|---|---|
| ! | &amp;#33; | -- | " | &amp;#34; | -- |
| # | &amp;#35; | -- | $ | &amp;#36; | -- |
| % | &amp;#37; | -- | & | &amp;#38; | -- |
| ' | &amp;#39; | -- | ( | &amp;#40; | -- |
| ) | &amp;#41; | -- | * | &amp;#42; | -- |
| + | &amp;#43; | -- | , | &amp;#44; | -- |
| - | &amp;#45; | -- | . | &amp;#46; | -- |
| / | &amp;#47; | -- | : | &amp;#58; | -- |
| ; | &amp;#59; | -- | < | &amp;#60; | -- |
| = | &amp;#61; | -- | > | &amp;#62; | -- |
| ? | &amp;#63; | -- | @ | &amp;#64; | -- |
| [ | &amp;#91; | -- | \ | &amp;#92; | -- |
| ] | &amp;#93; | -- | ^ | &amp;#94; | -- |
| _ | &amp;#95; | -- | ` | &amp;#96; | -- |
| { | &amp;#123; | -- | &#124; | &amp;#124; | -- |
| } | &amp;#125; | -- | ~ | &amp;#126; | -- |
|   | &amp;#160; | nbsp | ¡ | &amp;#161; | iexcl |
| ¢ | &amp;#162; | cent | £ | &amp;#163; | pound |
| ¤ | &amp;#164; | curren | ¥ | &amp;#165; | yen |
| ¦ | &amp;#166; | brvbar | § | &amp;#167; | sect |
| ¨ | &amp;#168; | uml | © | &amp;#169; | copy |
| ª | &amp;#170; | ordf | « | &amp;#171; | laquo |
| ¬ | &amp;#172; | not | | &amp;#173; | shy |
| ® | &amp;#174; | reg | ¯ | &amp;#175; | macr |
| ° | &amp;#176; | deg | ± | &amp;#177; | plusmn |
| ² | &amp;#178; | sup2 | ³ | &amp;#179; | sup3 |
| ´ | &amp;#180; | acute | µ | &amp;#181; | micro |
| ¶ | &amp;#182; | para | · | &amp;#183; | middot |
| ¸ | &amp;#184; | cedil | ¹ | &amp;#185; | sup1 |
| º | &amp;#186; | ordm | » | &amp;#187; | raquo |
| ¼ | &amp;#188; | frac14 | ½ | &amp;#189; | frac12 |
| ¾ | &amp;#190; | frac34 | ¿ | &amp;#191; | iquest |
| À | &amp;#192; | Agrave | Á | &amp;#193; | Aacute |
| Â | &amp;#194; | Acirc | Ã | &amp;#195; | Atilde |
| Ä | &amp;#196; | Auml | Å | &amp;#197; | Aring |
| Æ | &amp;#198; | AElig | Ç | &amp;#199; | Ccedil |
| È | &amp;#200; | Egrave | É | &amp;#201; | Eacute |
| Ê | &amp;#202; | Ecirc | Ë | &amp;#203; | Euml |
| Ì | &amp;#204; | Igrave | Í | &amp;#205; | Iacute |
| Î | &amp;#206; | Icirc | Ï | &amp;#207; | Iuml |
| Ð | &amp;#208; | ETH | Ñ | &amp;#209; | Ntilde |
| Ò | &amp;#210; | Ograve | Ó | &amp;#211; | Oacute |
| Ô | &amp;#212; | Ocirc | Õ | &amp;#213; | Otilde |
| Ö | &amp;#214; | Ouml | × | &amp;#215; | times |
| Ø | &amp;#216; | Oslash | Ù | &amp;#217; | Ugrave |
| Ú | &amp;#218; | Uacute | Û | &amp;#219; | Ucirc |
| Ü | &amp;#220; | Uuml | Ý | &amp;#221; | Yacute |
| Þ | &amp;#222; | THORN | ß | &amp;#223; | szlig |
| à | &amp;#224; | agrave | á | &amp;#225; | aacute |
| â | &amp;#226; | acirc | ã | &amp;#227; | atilde |
| ä | &amp;#228; | auml | å | &amp;#229; | aring |
| æ | &amp;#230; | aelig | ç | &amp;#231; | ccedil |
| è | &amp;#232; | egrave | é | &amp;#233; | eacute |
| ê | &amp;#234; | ecirc | ë | &amp;#235; | euml |
| ì | &amp;#236; | igrave | í | &amp;#237; | iacute |
| î | &amp;#238; | icirc | ï | &amp;#239; | iuml |
| ð | &amp;#240; | eth | ñ | &amp;#241; | ntilde |
| ò | &amp;#242; | ograve | ó | &amp;#243; | oacute |
| ô | &amp;#244; | ocirc | õ | &amp;#245; | otilde |
| ö | &amp;#246; | ouml | ÷ | &amp;#247; | divide |
| ø | &amp;#248; | oslash | ù | &amp;#249; | ugrave |
| ú | &amp;#250; | uacute | û | &amp;#251; | ucirc |
| ü | &amp;#252; | uuml | ý | &amp;#253; | yacute |
| þ | &amp;#254; | thorn | ÿ | &amp;#255; | yuml |
