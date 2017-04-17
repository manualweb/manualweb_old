
# JDBC (Java DataBase Connectivity)

## Índice

1. Primeros pasos con JDBC
2. Componentes JDBC
3. Tipos de Drivers JDBC
4. Crear una conexión JDBC -> ¿Esto no es parecido al Primeros Pasos? Ver si unificar.
5. Conexiones JDBC


## Primeros pasos con JDBC
JDBC es el API de Java que nos permite acceder a las bases de datos relacionales para realizar operaciones con ellas: consultas, inserciones, borrados,...

Los pasos que se suelen seguir mediante el uso de JDBC son:

1. Conectarse a la base de datos
2. Ejecutar una consulta
3. Recuperar los resultados

Estos tres simples pasos podríamos resumirlos de la siguiente manera:

1. Para conectarnos a la base de datos necesitamos tener los drivers de acceso a la base de datos. Cada base de dato tiene sus propios drivers. Mediante la clase DriverManager conseguiremos una conexión sobre la base de datos.

~~~java
Class.forName("com.mysql.jdbc.Driver").newInstance();
con = DriverManager.getConnection("jdbc:mysql://localhost:3306/lineadecodigo");
~~~

2. Lo siguiente es preparar la consulta en SQL y ejecutarla. Las sentencias son descritas utilizando PreparedStatements.

~~~java
stmt = con.prepareStatement("SELECT titulo FROM libros");
rs = stmt.executeQuery();
~~~

3.- Lo último será el recorrer los resultados para mostrarlos por pantalla. Los resultados de las consultas se dejaran en estructuras con filas y columnas llamadas ResultSet.

~~~java
while (rs.next())
  System.out.println (rs.getString("titulo"));
~~~

### Componentes JDBC
Dentro de JDBC encontramos 4 tipos de componentes:

* JDBC API
* JDBC Driver Manager
* JDBC Test Suite
* JDBC-ODBC Bridge

JDBC API
Es el que nos permite realizar una acceso programático a los datos de una base de datos relacional. El API JDBC puede interactuar con múltiples orígenes de datos en entornos distribuidos. EL JDBC API 4.0 está distribuido en dos paquetes que podemos encontrar dentro de Java SE.

* java.sql
* javax.sql

JDBC Driver Manager
Es un objeto que permite conectar las clases Java con los Drivers de las bases de datos. Este objeto es el DriverManager.

JDBC Test Suite
Permite comprobar qué Drivers vana funcionar con tu aplicación Java. Aunque no son test muy exhaustivos, permiten el comprobar las funcionalidades básicas de JDBC contra una base de datos.

JDBC-ODBC Bridge
Permite realizar un acceso JDBC utilizando drivers ODBC. La máquina que ejecute el programa Java deberá de contener los drivers ODBC binarios


NOTA: Se podría hablar de conceptos básicos del SQL: select, where, joins, comandos, cursores,...
https://docs.oracle.com/javase/tutorial/jdbc/overview/index.html


3. Introducción a JDBC

Drivers
Los primero que deberemos de hacer en nuestro código fuente JDBC será el instanciar los Drivers de la base de datos. Existen 4 tipos de drivers:

* Tipo 1, implementan el API JDBC realizando un mapeo directo sobre un API ya existente, por ejemplo con ODBC. Son drivers que dependen de una librería nativa y que por lo tanto suelen venir con complejidades en su portabilidad.
* Tipo 2, drivers que están construidos parcialmente en lenguaje Java y parcialmente en lenguaje nativo. En este caso suele existir un cliente nativo que es el que accede al origen de datos. Al tener parte nativa suelen existir complejidades de portabilidad. Oracle CLI es un driver de tipo 2.
* Tipo 3, drivers cuyo cliente es puro Java y que se comunican con el servidor middleware utilizando un protocolo independiente. El middleware es el que conecta con el origen de datos y devuelve el contenido al cliente.
* Tipo 4, son drivers puros Java que implementan el protocolo de red que se conecta al origen de datos. El cliente se conecta directamente con el origen de datos.

Instalación de los Drivers
La instalación de los drivers, sobre todo si son drivers tipo 4, suele consistir en copiar el driver en un path que esté contenido dentro del classpath.

Instalar Drivers MySQL
a

Instalar Drivers Oracle
a

Instalar Drivers SQL Server
a


Crear una conexión a la base de datos con JDBC
Lo primero que haremos para conectarnos a una base de datos mediante JDBC será el establecer una conexión. Las conexiones se realizan mediante el objeto Connection.


Class.forName("com.mysql.jdbc.Driver").newInstance();
Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/lineadecodigo");

Crear una sentencia
Una sentencia SQL es representada en JDBC mediante la clase Statement. Las sentencias son ejecutadas y su resultado suele devolver un conjunto de datos o ResultSet.

Statement stmt = con.createStatement()
stmt = con.createStatement("SELECT titulo FROM libros");

Dependiendo del tipo de sentencia podremos manejarlo con diferentes clases de Statements.

* Statement, para sentencias SQL que no tienen ningún tipo de parámetros
* PreparedStatement, para sentencias SQL que contienen parámetros. Extiende de Statement.
* CallableStatement, sirve para ejecutar procedimientos almacenados, los cuales pueden contener parámetros de entrada y de salida.

Nunca deberás de componer una sentencia con parámetros mediante concatenación de texto, ya que esa forma es susceptible de recibir una SQL Inyection.

Ejecutar una sentencia
Una vez que hemos construido nuestra sentencia SQL lo que haremos será ejecutarla para obtener un resultado. Las sentencias se pueden ejecutar de tres formas diferentes:

* execute, devuelve true si el objeto que se devuelve al ejecutar la query es un ResultSet. Este método se utiliza cuando la querré devuelve 1 o más objetos ResultSet. En este caso deberemos acudir al método Statement.getResultSet() para recuperar el contenido del ResultSet.
* executeQuery, devuelve un objeto ResultSet con el resultado de la ejecución de la query.
* executeUpdate, se utiliza para las actualizaciones o borrados, ya que devuelve un número entero con el número de registros afectados por la ejecución de la query, es decir número de filas insertadas, actualizadas o borradas.

ResultSet rs = stmt.executeQuery();

Recorrer un ResultSet
Una vez que hemos ejecutado la sentencia, para las consultas tendremos un ResultSet con los elementos recuperados de la base de datos. En este caso vamos a ver cómo podemos recorrer un ResultSet para acceder al resultado.

El ResultSet es un cursor que va apuntando a los datos del resultado. Para recorrer un ResultSet deberemos de ir moviendo el cursor por los resultados hasta que no haya más resultados. El método .next() nos ayuda a movernos por el ResultSet. Cada vez que ejecutamos el método .next() vamos moviendo el cursor y nos devuelve un registro con los datos que contiene la fila. En el caso de que queramos mover el cursor y no haya más registros nos devolverá el valor false.

Es por ello que el ResultSet se suele recorrer mediante un bucle while.

while (rs.next()) {
  System.out.println (rs.getString("titulo"));
  System.out.println (rs.getString(“isbn"));
  System.out.println (rs.getString(“autor"));
}

Por otro lado el ResultSet tiene una serie de métodos .getString(), getInt(), getFloat(),… los cuales nos permiten recuperar los campos del registro en el que estemos. Estos métodos recibirán como parámetro el nombre del campo que intentamos recuperar y que coincide con el nombre del campo de la tabla o alias que hayamos utilizado en la query.

Cerrar Conexiones
Lo último que deberemos de hacer a la hora de ejecutar una sentencia contra una base de datos con JDBC es el cerrar la conexión. De esta manera liberaremos los recursos que hacen a la base de datos y podrán ser utilizados por la ejecución de otra sentencia.

Lo primero que debemos de hacer para cerrar la conexión será el cerrar el objeto sentencia o Statement. Para ello deberemos de invocar a su método .close()

if (stmt != null) { stmt.close(); }

Al ejecutar el método .close() sobre el Statement, automáticamente se cierra el ResultSet. Ya solo nos quedará cerrar la conexión a la base de datos.

if (con != null) { con.close(); }

Una de las cosas que puede pasar a la hora de ejecutar sentencias SQL mediante JDBC es que se produzca un error, es por ello que la ejecución se suele hacer dentro de un bloque try-catch.

try {
  // Ejecución de la Sentencia
} catch (SQLException sqle) {
  sql.printStackTrace();
}

Es por ello que el cierre del Statement y del Connection se suele hacer en una estructura finally, la cual se ejecuta después de capturar la excepción. De esta forma nos aseguramos que se cierra de forma correcta el código.

try {
  // Ejecución de la Sentencia
} catch (SQLException sqle) {
  sql.printStackTrace();
} finally {
  if (stmt != null) { stmt.close(); }
  if (con != null) { con.close(); }
}

Desde la versión JDBC 4.1 que se encuentra disponible en Java SE 7 existe la posibilidad de manejar y cerrar las sentencias en un bucle try-catch. En este caso lo que hacemos es ejecutar la sentencia dentro del bucle

try (Statement stmt = con.createStatement("SELECT titulo FROM libros”)) {
  // Ejecución de la Sentencia
} catch (SQLException sqle) {
  sql.printStackTrace();
}

De esta forma la sentencia es cerrada automáticamente una vez que el bucle try-catch termina, independientemente de si lo hizo de forma correcta o no.


5. Conexiones JDBC

Lo primero que hacemos cuando queremos conectarnos a una base de datos es establecer una conexión.

Aunque las conexiones se suelen realizar a bases de datos entidad-relación, se podrían realizar conexiones a cualquier origen de datos que esté soportado por JDBC, por ejemplo a una hoja Excel.

Existen dos formas de conectarnos a una base de datos, por un lado podemos conectarnos mediante un DriverManager y por otro utilizando un DataSource.

Un DriverManager es un programa que conecta directamente contra la base de datos, en este caso necesitaremos una URL de conexión para poder acceder a la base de datos. Para poder utilizar un DriverManager deberemos de tener los drivers de acceso a la base de datos en el ClassPath de la aplicación.

En el caso del DataSource tenemos un interface diferente al DriverManager, en este caso los datos de conexión a la base de datos son transparentes para la aplicación. Se tiene un objeto DataSource que, directamente, representa a una fuente de datos.


5.1. Drivers de Base de Datos: DriverManager

5.1.1. Cargar los Drivers
Lo primero que deberemos de hacer para utilizar el DriverManager es cargar los drivers de la base de datos que vayamos a utilizar. Para ello deberemos de haber puesto los drivers de la base de datos dentro del classpath. Los drivers son representados mediante la clase Driver.

Utilizaremos el método Class.forName para poder cargar el driver antes de iniciar una conexión.

Class.forName("com.mysql.jdbc.Driver").newInstance(); // Para MySQL
Class.forName(“ org.apache.derby.jdbc.ClientDriver").newInstance(); // Para Apache Derby

A partir de JDBC 4.0 todos los drivers que estén dentro del ClassPath son cargados de forma automática, y por lo tanto no se necesita llamar a Class.forName().

5.1.2. Establecer una Conexión
La clase DriverManager es la que nos permite establecer una conexión contra la base de datos mediante el método .getConnection(). El método .getConnection() espera, principalmente, tres parámetros:

* Una URL de conexión a la base de datos.
* El usuario con el que nos conectados a la base de datos
* La contraseña del usuario.

.getConnection (URLConexión, usuario, password)

Hay otra fora de llamar al método .getConnection() en el cual pasaríamos:

* Una URL de conexión a la base de datos.
* Un fichero de propiedades de conexión a la base de datos. En estas propiedades debe de estar el usuario y password.

.getConnection(URLConexión, Propiedades)

5.2. URL de Conexión a la Base de Datos
La URL de conexión a la base de datos en JDBC es una cadena de texto en la que se suele encontrar: el protocolo de conexión a la base de datos, la máquina y puerto en el que está la base de datos, el nombre de la base de datos,… así como otros parámetros de configuración para el acceso.

Por ejemplo, algunas cadenas de conexión que podemos encontrar son las siguientes:

MySQL
La estructura de la cadena de conexión JDBC para MySQL es:
jdbc:mysql://[host1]:[port1],[host2]:[port2]/[databaseName]?[property1=value1]&[property2=value2]

* Máquina, máquina en la que está instalado MySQL. Para las máquinas y puertos se puede especificar una lista por si falla la primera busca en la segunda y así sucesivamente por la lista.
* Puerto, puerto de conexión a MySQL. Suele ser el 3306.
* Base de Datos, nombre de la base de datos a la que nos queremos conectar
* Propiedad/Valor, pares de atributo/valor para enviar configuraciones específicas de la base de datos,

Por ejemplo una cadena de conexión contra MySQL podría ser:
jdbc:mysql://localhost:3306/lineadecodigo

Puedes encontrar más información sobre el Driver de MySQL en la documentación oficial.

Oracle
La estructura de la cadena de conexión JDBC para Oracle es:
jdbc:oracle:[driverType]:[user]/[password]@[database]

* Tipo de Driver, el tipo de driver de Oracle que queremos utilizar. Los drivers que tiene son: “thin", “oci", “kprb",...
* Usuario/Password, usuario y contraseña para la conexión
* Database, es una cadena con el nombre de la máquina, el puerto y el sistema al que nos queremos conectar.

Un ejemplo de cadena de conexión de Oracle sería:
jdbc:oracle:thin:scott/tiger@myhost:1521:orcl

Se puede encontrar más información sobre las cadenas de conexión JDBC de Oracle en su documentación de los Drivers.

Apache Derby
Para el caso de conectarnos a una base de datos Derby la estructura de la cadena de conexión es:
jdbc:derby:[subsubprotocol:][databaseName][;attribute=value]*

* SubProtocolo, indica dónde está la base de datos, si está en memoria “memory”, en un directorio “directory”, en el classpath “classpath” o dentro de un fichero jar “jar”.
* Nombre Base de Datos, el nombre de la base de datos a la que nos queramos conectar
* Atributo/Valor, para configurar atributos específicos de la base de datos.

Un ejemplo de conexión a Apache Derby sería:
jdbc:derby:memory:sample

Puedes consultar más información sobre cómo conectarse a Apache Derby en su documentación.

5.3. Ejemplo de conexión
De esta forma el código necesario para realizar una conexión a una base de datos MySQL sería:

Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/lineadecodigo",”usuario”,"password");


[ ] Hay que revisar los DataSources - https://docs.oracle.com/javase/tutorial/jdbc/basics/sqldatasources.html


6. SQLException
Cuando hay un problema utilizando JDBC se lanza la excepción SQLException, la cual contiene la información sobre el error que se ha producido accediendo a la base de datos.

6.1. Estructura del SQLException
Dentro de la información que podemos encontrar en una SQLException tenemos:

* Descripción del error, que nos lo devuelve el método .getMessage()
* Código SQLState, es un código estándar definido dentro de las diferentes bases de datos para representar un código en concreto. Siguen un estándar definido por ISO/ANSI y el Open Group (X/Open) Se puede recuperar mediante el método .getSQLState(). El código SQLState es una cadena de texto
* Código de Error, es un número entero que identifica el error que provocó el tener que lanzar la SQLException. El código es diferente por cada proveedor de la base de datos. Se puede recuperar mediante el método .getErrorCode()
* Causa, identifica el objeto que fue el que generó la excepción SQLException. El método .getCause() nos devolverá la lista de objeto que han provocado el error.
* Excepciones relacionadas, en el caso de que haya más excepciones relacionadas, podremos recuperar la cadena de excepciones mediante el método .getNextException()


6.2. Capturando una SQLException
Para poder capturar la excepción SLQException deberemos de utilizar un bucle try-catch en el que ejecutaremos las sentencias JDBC. A la hora de capturar la excepción podremos acceder a todos los métodos que nos devuelven la información.

try {
  stmt = con.prepareStatement("SELECT pais FROM paises");
  rs = stmt.executeQuery();

  while (rs.next())
    System.out.println (rs.getString("pais"));
} catch (SQLException sqle) {
  System.out.println("Error en la ejecución:"
    + sqle.getErrorCode() + " " + sqle.getMessage());
}

6.3. Otras excepciones JDBC
La excepción general de JDBC es la SQLException, pero también contamos con algunas subclases de esta excepción para situaciones en concreto. Entre ellas tenemos:

* BatchUpdateExcepction, se produce cuando estamos ejecutando una sentencia en batch. Una sentencia en batch consiste en ejecutar un conjunto de sentencias de forma consecutiva. En el caso de que falle esa ejecución se lanza la BatchUpdateException, indicando el número de sentencias que se habían ejecutado antes del error.
* SQLClientInfoException, se produce cuando se ha intentado aplicar alguna propiedad en la conexión sobre la base de datos y no ha sido posible. La SQLClientInfoException nos devuelve una lista con las propiedades de la base de datos.

6.4. Warnings
Una de las subclases de SQLException es SQLWarning, un warning o alerta es una alerta informativa que nos devuelve la base de datos, pero que no par la ejecución de la sentencia que hayamos lanzado contra la base de datos.

Por ejemplo podríamos recibir un aviso de que un privilegio que queremos revocar no ha podido ser revocado, cuando insertamos campos y estos son truncados pero insertados en el modelo,...

Los warnings pueden obtenerse de los objetos Connection, Statement o ResultSet. Será el método .getWarnings() el que os de la información relativa a la alerta. El método .getWarnings() devuelve una lista de warnings. Es por ello que deberemos de recorrer la lista mediante un bucle.


SQLWarning warning = stmt.getWarnings();
while (warning != null) {
  System.out.println("Warning");
  System.out.println("Message: " + warning.getMessage());
  System.out.println("SQLState: " + warning.getSQLState());
  System.out.print("Vendor error code: “ + warning.getErrorCode());
  System.out.println("");
  warning = warning.getNextWarning();
 }

Vemos que los campos que tiene el objeto SQLWarning son los heredados del SQLException.



7. Crear Tablas
Crear tablas en JDBC es tan sencillo como manejar la sentencia SQL “CREATE TABLE”. Lo que vamos a crear son sentencias PreparedStatement que serán las que contengan las sentencia de creación y directamente las ejecutamos, consiguiendo así crear la tabla.

La estructura de la sentencia CREATE TABLE, de forma general, es:

CREATE TABLE nombre_tabla
     (campo1 tipo_campo1 atributos,
      campo2,tipo_campo2, atributos,
     ...
     campoN,tipo_campoN,atributos)

Los campos serán los definidos por el estándar SQL o los que soporte la base de datos que estés utilizando. Alguno de estos campos son:

* Cadenas, char, varchar,...
* Números, tinyint, smallint, int, bigint,...
* Fechas, date, datetime,...
* ...

Con respecto a los atributos que podemos asignares encontramos algunos como:

* NOT NULL, si queremos que el campo no pueda albergar nulos.
* AUTO_INCREMENT, si queremos que el número se incremente automáticamente.
* CURRENT_TIMESTAMP, para asignarle la fecha de la creación del registro
* ...


Por ejemplo podríamos crear una tabla de la siguiente forma

CREATE TABLE usuarios (
     indentificador INT(4) AUTO_INCREMENT,
     nombre varchar(50) NOT NULL,
     edad TINYINT(2),
     alta DateTime CURRENT_TIMESTAMP)

Así, para poder crear la tabla crearemos una sentencia y le asignaremos la cade

Statement stmt = null;
String createtable =  "
CREATE TABLE usuarios (indentificador INT(4) AUTO_INCREMENT, nombre varchar(50) NOT NULL, edad TINYINT(2), alta DateTime CURRENT_TIMESTAMP)"
stmt = con.createStatement();
stmt.executeUpdate(createString)

8. Realizar una Consulta: ResultSet
Realizar una consulta sobre una base de datos JDBC viene a ser la ejecución de una sentencia SQL SELECT.

El resultado de ejecutar una consulta se deja almacenado en un objeto ResultSet.

Por ejemplo si recuperamos todos los países de la tabla de países, el resultado se queda en un ResultSet.

PreparedStatement stmt = con.prepareStatement("SELECT country FROM country")) {
ResultSet rs = stmt.executeQuery();

Para recorrer los resultado del ResultSet utilizamos un cursor que itera por cada una de las filas y las columnas devueltas como respuesta. El cursor inicialmente apunta a la primera fila y podremos irlo moviendo fila a fila hasta que devuelva “false” que significará que no hay más registros en el cursor y que estamos posicionados en la última fila.

Tipos de ResultSet
El tipo de ResultSet nos indica dos cosas:

* Cómo puede ser manipulado y recorrido el cursor.
* Si el cursor se ve afectado ante cambios en los datos de origen

Así tenemos tres tipos de ResultSet:
* TYPE_FORWARD_ONLY, el cursor solo se puede recorrer hacía delante, desde la primera fila hasta la última. La información contenida en las filas representa al contenido que hay en la base de datos que se consultó.
* TYPE_SCROLL_INSENSITIVE, se puede hacer scroll por los datos, es decir, podemos mover el cursor hacía delante o hacía detrás. Incluso podemos moverlo a una posición en concreto. El ResultSet no es sensible a los posibles cambios de los datos que se puedan hacer por debajo. Tiene los datos tal cual estaban en la base de datos en el momento en que se recuperaron.
* TYPE_SCROLL_SENSITIVE, al igual que el anterior se puede realizar scroll por los datos del cursor. Hacía delante, hacía detrás o a una posición absoluta. Si bien es sensible a los cambios que se produzcan en el origen de datos siempre y cuando el cursor siga abierto.

Por defecto el ResultSet es TYPE_FORWARD_ONLY. No todos los drivers y bases de datos soportan todos los tipos de cursores. Así tenemos el método DatabaseMetaData.supportsResultSetType para saber si el tipo de ResultSet es soportado.

Concurrencia en el ResultSet
La concurrencia de un ResultSet indica la capacidad de actualización que tiene el cursor. De esta forma tenemos dos tipos de concurrencia.

* CONCUR_READ_ONLY, el ResultSet no puede ser actualizado, solo podemos leer.
* CONCUR_UPDATABLE, el ResultSet puede ser actualizado.

Por defecto los ResultSet son de solo lectura. Mediante el método DatabaseMetaData.supportsResultSetConcurrency sabremos si el nivel de concurrencia está soportado por la base de datos.

Mantenibilidad del ResultSet

Cuando se ejecuta un “commit” sobre una Conexión los ResultSet son automáticamente cerrados. Puede ser que en algún caso este no sea el comportamiento que deseamos y queremos que se mantenga abierto el cursor. Así la propiedad “holdability” nos permite cambiar este comportamiento. De esta manera podemos tener dos tipos de ResultSet:

* HOLD_CURSORS_OVER_COMMIT, no se cierra el ResultSet ante un commit. Esto es recomendable solo para ResultSet que sean de solo lectura.
* CLOSE_CURSORS_AT_COMMIT, el cursor se cierra en cuanto se realiza un commit. Este es el mejor caso desde un punto de vista de rendimiento.

El método JDBCTutorialUtilities.cursorHoldabilitySupport, nos indicará que nivel de mantenibilidad está soportado por nuestro gestor de base de datos. Dependiendo de la base de datos que utilicemos vendrá uno u otro por defecto.

8.1. Obtener Columnas

Cuando estamos recorriendo el ResultSet, este nos ofrece una serie de métodos para recuperar las columnas, atendiendo al tipo de dato que se almacene en la columna. Así tenemos .getBoolean(), getLong(), getString(),… estos métodos recibirán como parámetro el nombre o alias de la columna o bien el índice de la columna dentro de la consulta.

Si trabajamos con índices la primera columna se numera con el 1, la segunda con el 2 y así consecutivamente hasta el número de columnas que existan. El acceso por índices es la forma en la que mejor rendimiento se tiene en el acceso a datos.  Las lecturas por índices deben de ser realizadas de izquierda a derecha.

En el caso de trabajar con nombres o alias deberemos de saber que estos no son sensibles a mayúsculas.

// Acceso por indice
(EJEMPLO)

// Acceso por columna
(EJEMPLO)

8.1. Recorrer un cursor
Los datos del ResultSet son recorridos utilizando un cursor, cursor que iremos moviendo a través de las diferentes filas que contenga el ResultSet. Para poder movernos por el ResultSet tenemos una serie de métodos:

* next(), mueve el cursor a la siguiente fila. Devuelve true si el cursor apunta a una fila y false si apunta después de la última fila.
* previous(), mueve el cursor a la fila anterior. Devuelve true si el cursor está apuntando a una fila y false si apunta antes de la primera fila.
* first(), mueve el cursor a la primera fila del ResultSet.
* last(), mueve el cursor a la última fila del ResultSet.
* beforeFirst(), posiciona el cursor al principio del ResultSet.
* afterLast(), posiciona el cursor después de la última fila del ResultSet.
* relative(int rows), posiciona el cursor tantas filas relativas a la posición actual.
* absolute(int row), posiciona el cursor en el número de fila pasado como parámetro.

[ ] Recorrer un cursor al revés
[ ] Obtener una fila en concreto del cursor

8.2. Actualizar filas en un ResultSet


8.4. Batch Updates???

8.5. Insertar filas en Resultset






Ejemplos en Línea de Código

[ ] Habría que revisar los ejemplos de https://docs.oracle.com/javase/tutorial/jdbc/basics/examples/zipfiles/JDBCTutorial.zip

1-Introducción
* Conectarnos a una base de datos con JDBC

5-Conexión a la BD
* Listar los drivers con JDBC
* [x] Conectarse a Apache Derby
* Conectarse a MySLQ
* [ ] Conectar a Oracle Express
* [x] Conexión utilizando Properties
* JDBC: Conectarse a una base de datos MS Access
* Configurar para que acepte truncado de campos

X-Consultas
* Consultas SQL con parametros en Java JDBC
* Consulta JDBC sin conocer los campos
* Insertar datos con JDBC
* Actualizar datos con JDBC
* Borrado de Datos con JDBC
* [x] Crear un tabla con JDBC
* [x] Borrar una tabla con JDBC
* [x] Borrar contenido de una tabla - TRUNCATE o DELETE FROM
* [x] Insert con campos truncados
* Cargar por batch (executeBatch)
* [ ] Cargar desde un fichero
* [ ] Crear un índice sobre una tabla
* [ ] Realizar un alter a una tabla
* [ ] Recuperar el último identificador de un campo Autoincremental

     [ ] Revisar operaciones que se pueden hacer a una base de datos y ponerlas. Privilegios, alter,..
     [ ] Carga de una base de datos
     [ ] Gestionado de versiones (descarga, alter y carga) o esto en shell?

ResultSet
[ ] Recuperar un campo de un Resultset, por nombre e índice
[ ] Saber que tipos de ResultSet soporta tu BD (tipo, actualización y mantenibilidad) -> 3 artículos
[ ] Hacer un tipo de Resultset que afecte datos y otro con scroll.
[ ] Como pagina? Da algo JDBC? Mediante el patrón de índice??


Excepciones

* [x] Controlar SQLException
* [x] Warnings - http://dev.mysql.com/doc/refman/5.7/en/show-warnings.html
* [x] Controlar un error en un BatchUpdate
* [ ] Controlar un SQLClientInfoException
