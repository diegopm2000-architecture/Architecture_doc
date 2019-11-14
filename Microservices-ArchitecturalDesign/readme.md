# Microservices Architectural Design

## 1. Resumen

![Resumen](Resumen.jpg)

## 2. How to Scope microservices using bounded contexts

### 2.1 Ideas principales

La idea de los microservicios es que permitan desarrollar software que miminice el coste de modificación y tiempo de entrega.

Design vs Scrumm. Aquí la idea es que la arquitectura interna de los microservicios ha de ser emergente, y que realmente se haga durante el proceso de desarrollo. Inicialmente nos quedamos con que se necesita una especificación funcional de lo que queramos que haga el microservicio.

Es responsabilidad de arquitectos del equipo comunicar al equipo para que se van a usar estos microservicios, usando un punto de vista estrátegico de la función que realizan.

Usaremos los contextos delimitados para definir la arquitectura de microservicios de la aplicación. Estos contextos vienen de usar DDD (Domain Driven Design) de Eric Evans.

### 2.2 Domain Driven Design

![DDD](DDD.jpg)

Nos centraremos en el concepto de bounded contexts.

### 2.3. Bounded Context

![Bounded Context](BoundedContext.jpg)

### 2.4 Ubiquituous Language

El lenguaje ubiquo pertenece a una funcionalidad específica (bounded context). Se usa por todos los miembros del equipo para conectar todas las actividades que se realicen con el software.

![Bounded Context and Ubiquitous Langauge](BCANDUL.jpg)

### 2.5 Aproximación a los microservicios sin bounded contexts

Se recogen los aspectos core de nuestro dominio:

![Core Aspects](CoreAspects.jpg)

Se desarrollan los conceptos core del negocio con otros conceptos asociados.

![Core Concepts and Associated Concepts](CCAndSC.jpg)

Si no tenemos cuidado, acabamos solapando los conceptos y se queda todo muy liado.

![Core Concepts and Associated Concepts 2](CCAndSC2.jpg)

Al no haber delimitaciones entre los diferentes contextos, la aplicación se volverá muy complicada de mantener a lo largo del tiempo, e incluso en la fase de desarrollo y evolutivos.

### 2.6 Uso de bounded contexts

![BCTEchnique](BCTEchnique.jpg)

Lo primero, es identificar el core.

![Identifying the core](CoreIdentify.jpg)

El Core define el lenguaje Ubicuo

![Identifying the core 2](CoreIdentify2.jpg)

Renombramos los conceptos

![Rename concepts](RenameConcepts.jpg)

Podemos sacar algunos conceptos complejos de los contextos

![Out Concepts](OutConcepts.jpg)

De esta forma, nos quedamos con conceptos más simples, lo que implica mejor integración

![Single Concepts](SingleConcepts.jpg)

De esta forma, el pasar del bounded context a los microservicios, se hace de forma rápida y clara

![Bounded Context to Microservice](BC2Microservice.jpg)

Microservicios que finalmente resultan

![Microservicios resultantes](Selección_019.jpg)

### 2.7 Agregación

![Agregación](Selección_020.jpg)

Cuando interesa descomponer o agregar? Hay que verlo en función de las necesidades

## 3. Como concebir la arquitectura de microservicios asíncronos

Event based:

 - Competing Workers Pattern
 - Fanout pattern

Async API Calls

  - Request/Acknowledge with Callback

### 3.1 Asynchronous Microservices

Introducción

![Introducción](Selección_021.jpg)

Opciones que tenemos

- Event based
- Async API Calls
- Hangfire

![Opciones que tenemos](Selección_022.jpg)

### 3.2 Event Based

Event as a message

![Event as a Message](Selección_023.jpg)

Uno de los más populares es Rabbit.

### 3.3 Competing Workers Pattern

![Competing Workers Pattern](Selección_024.jpg)

Lo proporcionan los message brokers y permite escalar horizontalmente nuestra arquitectura en caso de que aumenten nuestras necesidades.

Además proporiona redundancia en caso de fallo.

Aquí tenemos un ejemplo de immplemetanción con rabbit mq

![Ejemplo de implementación](Selección_025.jpg)

### 3.3 Fanout Pattern

Con este patrón, el mensjae es consumido por todos los servicios.

![Fanout Pattern](Selección_026.jpg)

Ejemplo de implementación con rabbit mq

![Fanout Pattern Ejemplo de implementación](Selección_027.jpg)

### 3.4 Api Async Pattern

Se comunican directamente de forma asíncrona, sin usar un broker de mensajería.

![Api Async Pattern](Selección_028.jpg)

Ejemplo completo de Request/Acknowledge con Callback

![Request Acknowledge with Callback](Selección_028.jpg)

Detalle

![Detalle](Selección_029.jpg)

## 4. Api Microservices

- Functional Requirements
- Architecture Options
- REST Architectural Style
- API Architectural Patterns
    * Facade Design Pattern
    * Proxy Design Pattern
    * Stateless Service Pattern


