# RESTful vs GraphQL

Las APIs REST han sido determinantes en el auge del desarrollo de apps y de servicios distribuidos. Las más utilizadas hoy día son las **APIs RESTfull**. 

REST es, por tanto, un **claro caso de éxito**, pero su concepción CRUD basada en resources, verbos y códigos de respuesta HTTP hacen **cada vez más patente sus limitaciones y falta de flexibilidad**.

La necesidad de avanzar más rápidamente en productos cada vez más complejos, más allá de un simple CRUD, ha empujado un cambio en la forma de interactuar con las APIs. En este nuevo escenario surge **GraphQL**, un **fuerte candidato para sustituir a REST**.

## GraphQL APIs

GraphQL **no es una librería o framework, sino una especificación** de cómo implementar un lenguaje de queries en cualquier lenguaje de programación. Ya existen **implementaciones realizadas en lenguajes** como JavaScript, Python, Scala, Java, Ruby, Clojure, Go, PHP, .NET, etc. También existen clientes para consumir un API GraphQL desde JS, iOS, Android, React, Angular, etc.

Lo más interesante de GraphQL es que **el cliente (el Frontend) es quién decide qué datos pedir al servidor y de qué forma**, por lo que si mañana se necesita un dato adicional o se deja de necesitar otro, no hay que modificar el Backend, simplemente se modifica la query de del cliente y ya está.

GraphQL es **Open Source**. El primer borrador de su especificación (aún en desarrollo) fue creado por **Facebook**, que lleva usándolo y perfeccionandolo desde 2012 en sus apps móviles. También Github, Pinterest o Shopify se han unido al carro.


## Interactuando con GraphQL

La forma de interactuar con un API Rest es mediante una petición HTTP a ciertas URL únicas por recurso del API usando alguno de los métodos GET, POST, PUT o DELETE.

En cambio con GraphQL sólo hay **un endpoint** con el que se interactúa mediante el método POST. Para indicar la operación a realizar se coloca en el cueropo de la petición alguna de estas tres opciones: **Query, Mutation o Subscription**.

## Ventajas de GraphQL sobre REST

Con REST no se pueden elegir los datos que se recesitan recibir como respuesta a una petición. Con GraphQL, en cambio, se puede **elegir exactamente lo que se encesita**.

Dónde REST requiere muchas request, a GraphQL tan sólo le hace falta **una única request para obtener los mismos datos**.

En REST, cuando se necesita añadir nuevos campos o modificar el tipo de alguno de ellos, para mantener compatibilidad con los clientes viejos hay que ampliar innecesariamente el tamaño y tiempo de carga de la respuesta, o gestionar “vistas distintas” en el lado del servidor según la versión del cliente que consume el recurso. Con GraphQL **no hay que modificar el backend, sólo hay que cambiar la query en el cliente**.

REST tiene una asignatura pendiente con la **documentación**, casi siempre pobre en muchos casos. GraphQL aprovecha su naturaleza fuertemente tipada para ser autodocumentada, por ejemplo con GraphiQL.

## Referencias y más información

- [GraphQL](http://graphql.org/)
- [Primer borrador del RFC (aún en desarrollo)](http://facebook.github.io/graphql/October2016/)
- [Introducción a GraphQL](https://platzi.com/blog/introduccion-a-graphql/)
- [¿Por qué deberíamos abandonar REST y empezar a usar GraphQL en nuestras APIs?](https://www.genbetadev.com/desarrollo-aplicaciones-moviles/por-que-deberiamos-abandonar-rest-y-empezar-a-usar-graphql-en-nuestras-apis)

