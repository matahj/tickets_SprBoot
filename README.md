# Tickets Spring Boot

Se desarrolla un Backend para venta de boletos de autobus utilizando Spring Boot Y las dependencias Spring Web, Spring JPA, MySQL Driver, Lombok, Mapstruct y Slf4j.

## Especificaciones

Se tienen terminales en diferentes estados de la República, las cuales son origen y destino de los viajes. Cada terminal tiene adscritos un conjunto de autobuses y uno de conductores, los cuales son asignados a cada viaje según su disponibilidad y de manera independiente unos de otros. Los viajes son programados con origen, destino, fecha y hora de salida. El precio del boleto se establece al programar el viaje (dependiendo de diferentes factores). Todos los autobuses tienen cuarenta asientos y se clasifican en las clases primera, segunda y tercera; otras características importantes que se deben tomar en cuenta son la matrícula del autobús y su estado mecánico (operativo o en mantenimiento). Los clientes deben registrarse con: nombre completo, domicilio, correo electrónico y telefono. Cuando el cliente compra un vije selecciona un asiento. Para cada viaje de ida, hay uno de regreso con el mismo autobús y el mismo conductor. El usuario "administrador" tiene acceso y puede modificar todas las tablas (operaciones CRUD), los usuario "cliente" pueden leer "viajes", crear-leer-actualizar su propia información en "clientes" y crear-leer "boletos" (no puede hacer cancelaciones ni cambios).

## Setup

1. Clonar el repositorio
2. Configurar el acceso a la base de datos MySQL en ./src/main/resources/application.properties (base de datos, usuario y contraseña).
3. Crear la base de datos.
4. Ejecutar

## Compilación-Construcción-Ejecución
Para compilar y ejecutar en desarrollo:
~~~
mvn clean   //opcional
mvn spring-boot:run
~~~

Para compilar y construir un archivo jar:
~~~
mvn clean   //recomendado
mvn package
~~~

Para ejecutar el jar
~~~
java -jar ./target/tripsSpringBoot-0.0.1-SNAPSHOT.jar
~~~
