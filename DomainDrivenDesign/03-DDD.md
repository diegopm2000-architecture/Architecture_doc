# Domain Driven Design

## 1. Fuentes de referencia

Libros interesantes

![Libros interesantes de DDD](./LibrosDDD.png)

Video resumen de codely:

https://www.youtube.com/watch?v=dH5aSQLXtKg

## 2. DDD en términos generales

Es un enfoque de desarrollo propuesto por Eric Evans.

## 3. Ventajas

- Flexible
- Perspectiva desde la parte del cliente
- Ofrece una vía para solucionar problemas muy complejos
- Permite tener el código bien organizado y fácilmente testable
- Permite tener la lógica de negocio en un único sitio
- Soporta multiples patrones de diseño

## 4. Inconvenientes

- Tiempo y esfuerzo:

    * Require discutir el modelo del problema con los expertos del dominio
    * Aisla la lógica de dominio de otras partes de la aplicación

- Curva de aprendizaje

    * Supone nuevos principios
    * Supone nuevos patrones
    * Supone nuevos procesos

- Sólo tiene sentido cuando realmente el problema tiene complejidad

    * No aconsejado para aplicaciones CRUD o Data-driven
    * No aconsejado cuando sólo hay realmente dificultad técnica no del dominio del problema.

- La compañia o el eqipo han de creer realmente en el DDD

## 5. Tactical Design

__Model-Driven Design__:

Modelar el diseño en base al contexto del problema genérico. Este modelado estará basado en __Services__, __Entities__, __Value Objects__ (no tienen identificadores, por ejemplo los colores)

Los __Entities__ se pueden agrupar en __Aggregates__ para mantener su integridad.
Los __Value Objects__ se encapsulan en __Aggregates__

Los __Aggregates__ y __Entities__ se pueden guardar en __Repositories__

Cada vez que las __Entities__ cambian de estado, se produce un __Domain Event__
También puede haber eventos de dominio (desde el __Model-Driven Design)

Tanto __Entities__, como __Value Objects__ o __Aggregates__ se pueden encapsular por medio de __Factories__

Todo se combina con la __Layered-Architecture__, (no confundir con la arquitectura por capas, que acopla la base de datos al dominio). Eric Evans que lo quiere decir es que una solución DDD no se acopla a los detalles de implementación. Se usaría Arquitectura Hexagonal o bien Clean Architecture también parece aplicar.


![Tactical Design](./DDD-TacticalDesign.png)

## 6. Strategic Design

Todo esto da estructura al __Ubiquous Language__, que viene a ser que todo lo que se hable mediante el lenguaje de alto nivel de negocio, quede reflejado en el código.

Finalmente, todo queda reflejado en el __Bounded Context__, que consiste en que un dominio puede dividirse en subdominios, de tal forma que pueden existir dominios relacionados los cuales se agrupan en un contexto. Las fronteras de estos contextos __Context Boundaries__ son los puntos por los cuales se pueden comunicar los subdominios de un contexto con otro. Esta comunicación se hace mediante servicios o adapters.

El modelo se mantiene unificado gracias a la __Continuos Integration__

Las relaciones se mantieen mediante el __Context Map__

Una aplicación anterior se conocería como __Big Ball of Mud__

Se define un mecanismo para comunicarnos con otro sistema llamado __Anticorruption Layer__

Los equipos son libres de trabajar de forma separada (__Separate Ways__)

Podemos ofrecer al resto de la empresa una forma de comunicarse con nuestra nueva aplicación, via __Open Host Service__, por ejemplo un API.

Se conoce como __Published Language__ al código publicado

__Shared Kernel__ se conoce como una base de datos compartida entre varios contextos, lo más pequeña posible. Por ejemplo sólo los identificadores a nivel de infraestructura.

Si tenemos un tercero que nos desarrolla una parte del sistema se conoce como __Customer/Supplier Teams__

__Conformist__ se refiere a que entre dos equipos se tienen que conformar con un api o algo similar para compartir datos.


![Strategic Design](./DDD-StrategicDesign.png)

