# Oracle vs MongoDB

- La creciente cantidad y variedad de datos generados y utilizados por las aplicaciones empresariales actuales han originado conjuntos masivos de éstos.

- Los sistemas de gestión de bases de datos relacionales tradicionales presentan limitaciones a la hora de gestionar y explotar eficientemente estos conjuntos de datos.

- Los sistemas de gestión de bases de datos NoSQL han surgido como alternativa a los SGBD relacionales para la gestión de estos conjuntos de datos. Entre los principales SGBD NoSQL se encuentra MongoDB.

## MongoDB

- MongoDB es una base de datos de propósito general que puede ser utilizada en una **gran variedad de casos de uso**.

- MongoDB **simplifica el desarrollo** y permite **crear aplicaciones más rápidamente**, ya que los documentos MongoDB (en formato JSON) se asignan de forma natural a los lenguajes de programación modernos orientados a objetos.

- Al ser _schemaless_ (el esquema o estructura de datos no tiene que estar necesariamente predefinido), MongoDB **elimina la compleja capa de mapeo relacional** de objetos (ORM, que traduce los objetos en código a celdas en tablas relacionales) y permite manejar **tipos de datos muy diversos**, incluso que el valor de un **atributo sea multivaluado** (lista de valores) o que pueda presentar **formatos diferentes**.

- En MongoDB se pueden realizar consultas distribuidas mediante técnicas de _mapreduce_ (paradigma de programación paralela en arquitecturas distribuidas) lo que permite **reducir aún más los tiempos de respuesta**.

- MongoDB puede escalar dentro o a través de múltiples centros de datos distribuidos, lo que proporciona niveles de **disponibilidad y escalabilidad** que anteriormente no se podían alcanzar con bases de datos relacionales como Oracle.

- Frente a nuevos requerimientos en términos de volumen de datos y rendimiento, MongoDB **escala fácilmente sin tiempo de inactividad y sin necesidad de cambiar las aplicaciones**. Por el contrario, para lograr una escala con Oracle se requiere a menudo un trabajo de ingeniería significativo y personalizado o una inversión en hardware caro y personalizado.

- Las organizaciones (de cualquier tamaño) que cambian de Oracle a MongoDB consiguen un **ahorro de más del 70%** como resultado de las ganancias en productividad del desarrollador, la reducción de costes en hardware y el modelo de licencia.

## Oracle

- Aunque la mayoría de las aplicaciones modernas requieren un sistema flexible y escalable como MongoDB, existen casos de uso en los que es más adecuado utilizar una base de datos relacional como Oracle. Por ejemplo, aquellas aplicaciones que requieren transacciones complejas.

- Además, MongoDB tampoco es un reemplazo inmediato para aplicaciones heredadas basadas en el modelo de datos relacionales y SQL.

## Implementaciones híbridas

- Existen también numerosos casos de implementaciones híbridas de MongoDB y Oracle. Por ejemplo:

    - Sistemas de reserva de viajes, en los que el motor de reserva principal, que es el que realiza transacciones complejas, podría ejecutarse en Oracle mientras que las partes de la aplicación que interactúen con los usuarios (sirviendo contenido, integrándose con redes sociales, administrando sesiones) estarían mejor ubicadas en MongoDB.
    
    - Aplicaciones de comercio electrónico, donde el catálogo de productos, que incluye múltiples productos con diferentes atributos, es una buena opción para el modelo de datos flexible de MongoDB, mientras que el sistema de pago, que requiere transacciones complejas, puede implementarse sobre Oracle u otra tecnología relacional.

    - En otros casos, los nuevos requisitos comerciales impulsan a las organizaciones a adoptar MongoDB para los componentes de próxima generación de sus aplicaciones.

## Ejemplos de gráficas comparativas

- Existen numerosos estudios comparativos de rendimiento entre las principales bases de datos relacionales y NoSql, por ejemplo entre Oracle y MongoDB.

- Aunque se pueden realizar estudios profundos con experimentos muy exhaustivos y otros muchos tipos de pruebas, los estudios basados en operaciones de inserción, consulta, actualización y borrado (CRUD) ofrecen un buen punto de partida para el análisis de rendimiento de estos SGBD.

- A continuación se muestran algunas gráficas que dan una idea comparativa del rendimiento de algunas operaciones en MongoDB y Oracle. Estas gráficas están explicadas en en el informe [Una comparación de rendimiento entre Oracle y MongoDB](http://www.scielo.org.co/pdf/cein/v26n1/v26n1a07.pdf), citado en el apartado de referencias de este documento.

> NOTA: Para entender correctamente las gráficas es necesario ver (en el documento citado) las configuraciones y condiciones específicas en las que se han realizado.

![Inserción](mongodb_vs_oracle_insercion.png)
![Modificación](mongodb_vs_oracle_actualizacion.png)

![Consulta](mongodb_vs_oracle_consulta.png)
![Borrado](mongodb_vs_oracle_borrado.png)

## ¿Cuál utilizar?

- En multitud de casos de uso MongoDB es mejor opción que Oracle, debido a su modelo de datos flexible, arquitectura escalable, etc.

- Un caso de uso especialmente interesante son los procesos ETL/ELT, en los que se obtienen datos de orígenes y formatos muy diversos que pueden ser fácilmente persistidos y transformados en una base de datos MongoDB.

## Referencias

- [MongoDB and Oracle Compared](https://www.mongodb.com/compare/mongodb-oracle)
- [Una comparación de rendimiento entre Oracle y MongoDB](http://www.scielo.org.co/pdf/cein/v26n1/v26n1a07.pdf)




