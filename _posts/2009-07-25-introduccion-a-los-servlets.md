---
ID: 143
post_title: Introducción a los Servlets
author: Víctor Cuervo
post_date: 2009-07-25 00:18:48
post_excerpt: ""
layout: post
permalink: >
  http://www.manualweb.net/java-ee/introduccion-a-los-servlets/
published: true
---
<!--TOC-->
<h3>¿Qué son los servlets?</h3>
Los servlets son modulos java que nos sirven para extender las capacidades de los servidores web. Aunque es una definición un poco ambigua los servlets son programas para los servidores, mientras que los applets son programas para los clientes y los middlets los programas para microdispositivos.

Dentro de una evolución cronologica los servlets son la siguiente etapa de los CGI. En algunas bibliografias son referenciados como CGI de 2ª generación, la cual comparten con lenguajes como <a title="ASP" href="http://www.manualweb.net/tutorial-asp/">ASP</a>, <a title="PHP" href="http://www.manualweb.net/tutorial-php/">PHP</a> y <a title="JSP" href="http://www.manualweb.net/tutorial-jsp/">JSP</a> (que al fin y al cabo son servlets).

El uso de los servlets viene a ser en un tanto por ciento elevando el del desarrollo de páginas web dinámicas (en contenido y diseño) apoyandose además en la potencia que nos proporciona el lenguaje Java.
<h3>Para qué podemos utilizar los servlets</h3>
Podremos desarrollar desde un simple servlet que nos muestre una página web simple saludandonos hasta uno que se conecte a una base de datos utilizando un pool de conexiones, encriptando la información en su envio, accediendo a bases de datos distribuidas y manteniendo su información de forma persistente en un EJB. Todo ello para conseguir una información dinámica. A partir de aqui las posibilidades son "infinitas".
<h3>Ciclo de vida del servlet</h3>
Describir un servlet es como describir una maquina de estados. Desde el momento que inicializamos el servlet hasta que el servlet es destruido, este, pasará por una serie de estados dependiendo de cada una de las situaciones ante las que se encuentre.

Muy por encima podríamos decir que la secuencia de acciones que se producen en un servlet son las siguientes. La primera vez que realicemos una petición sobre el servlet se ejecutará un método de inicio, denominado <a title="init()" href="http://www.w3api.com/wiki/Java:Servlet.init()">init</a>, en el cual inicializaremos las variables generales. Una vez que nos hemos inicializado nos pondremos a la escucha en espera de peticiones. Cada una de las peticiones que recibamos serán atendidas en hilos de ejecución diferentes, a no ser que indiquemos lo contrario. Dependiendo de como llegen los datos (mediante post o get) al servlet se ejecutará un método u otro <a title="doPost()" href="http://w3api.com/wiki/Java:HttpServlet.doPost()">doPost</a> o <a title="doGet()" href="http://www.w3api.com/wiki/Java:HttpServlet.doGet()">doGet</a>. Por último el servlet tendrá un estado de finalización en el cual eliminará las variables creadas en su inicialización, conexiones a bases de datos,... este el el método destroy.
<h3>Escribiendo un primer servlet</h3>
A la hora de codificar lo primero que debemos de saber es que nuestro servlet deberá de heredar de la clase <a title="HttpServlet" href="http://www.w3api.com/wiki/Java:HttpServlet">HttpServlet</a> la cual contendrá todos los métodos necesarios para generar un servlet. Dicha clase la podemos encontrar en el <a title="javax.servlet" href="http://w3api.com/wiki/Categor%C3%ADa:Java_Servlet">paquete javax.servlet</a>.
<pre lang="java" lineno="1">import javax.servlet.*;
public class MiServlet extends HttpServlet {}</pre>
Solamente deberemos de sobrescribir aquellos métodos que consideremos oportunos a implementar en el servlet. Si por ejemplo no necesitasemos realizar ninguna inicialización, no haría falta el reescribir el método <a title="init()" href="http://www.w3api.com/wiki/Java:Servlet.init()">init</a>.

Así un primer servlet que mostrase la frase, como no, de "Hola Mundo" quedaría de la siguiente forma:
<pre lang="java" lineno="1">import javax.servlet.*;
import javax.servlet.http.*;

public class MiPrimerServlet extends HttpServlet {
  public void doGet (HttpServletRequest req, HttpServletResponse res) throws ServletException, IOException {
    PrintWriter out; out = res.getWriter();
    res.setContentType("text/html");
    out.println("<html>");
    out.println("<head><title>Mi Primer Servlet</title></head>");
    out.println("<body>);
    out.println("Este es mi Primer Servlet");
    out.println("</body></html>");
  }
}</pre>
Como se puede apreciar, la salida que se está generando es una página web (sus etiquetas). Es decir, recalcamos la idea de que generamos el contenido de una página web dinamicamente.