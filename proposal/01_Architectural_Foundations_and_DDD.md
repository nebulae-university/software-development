# Path 1: Fundamentos de Arquitectura de Microservicios y DDD

## Objetivo del Path

Este path está diseñado para que el desarrollador internalice los principios de diseño y los patrones arquitectónicos que guían la creación de software robusto, escalable y alineado con las necesidades del negocio en NebulaE. Al finalizar, el desarrollador podrá descomponer un sistema en microservicios, diseñarlos siguiendo los principios de DDD y aplicar los patrones de comunicación, datos y despliegue más importantes.

### Descripción General del Path

Este Path es el pilar fundamental de la filosofía de desarrollo de NebulaE. Su propósito no es solo enseñar un conjunto de tecnologías, sino forjar una mentalidad de **Arquitecto de Software Moderno**. Aquí, aprenderás a pensar en el software no como una colección de funcionalidades, sino como un modelo vivo del negocio al que sirve.

**¿Qué se espera de ti?**
Se espera que te sumerjas en los conceptos con una mente crítica. No se trata de memorizar patrones, sino de entender profundamente el *porqué* de cada uno. Deberás cuestionar las soluciones monolíticas tradicionales y abrazar un enfoque donde el software se diseña para ser flexible, resiliente y, sobre todo, alineado con un dominio de negocio en constante evolución. Al final de este camino, no solo construirás software, sino que lo diseñarás con intención y propósito.

**¿Qué vas a aprender?**
A lo largo de este recorrido, dominarás las dos disciplinas que definen la arquitectura de NebulaE:

1.  **Domain-Driven Design (DDD):**
    *   **Estratégico:** Aprenderás a colaborar con expertos del negocio para descubrir y definir el **Lenguaje Ubicuo**. Descompondrás problemas complejos en **Contextos Delimitados** manejables, que se convertirán en la semilla de tus microservicios.
    *   **Táctico:** Modelarás la lógica de negocio interna de cada servicio usando bloques de construcción como **Agregados**, **Entidades** y **Objetos de Valor**, garantizando que la lógica de dominio esté encapsulada y protegida.

2.  **Arquitectura de Microservicios:**
    *   **Patrones Fundamentales:** Implementarás patrones esenciales como **CQRS** y **Event Sourcing**, separando la lógica de escritura de la de lectura y construyendo sistemas basados en un flujo inmutable de eventos.
    *   **Comunicación y Datos:** Resolverás los desafíos de la comunicación entre servicios y la consistencia de datos distribuidos, aprendiendo sobre **API Gateways**, **Bases de Datos por Servicio** y el patrón **Saga**.
    *   **Despliegue y Operación:** Entenderás cómo empaquetar tus servicios en **contenedores** y cómo estandarizar el desarrollo con **plantillas de servicio** para acelerar la entrega de valor.

Este Path te transformará de un programador que implementa requisitos a un arquitecto que modela soluciones de negocio.

## Plan de Estudios

El plan se divide en 5 semanas, siguiendo una progresión lógica desde los fundamentos de DDD hasta los patrones de comunicación y consistencia en arquitecturas de microservicios.

### Playlist Recomendada: Software Architecture by Drawing Boxes

Como complemento fundamental a las lecturas, se recomienda seguir la siguiente lista de reproducción que cubre de forma visual y progresiva los conceptos clave de la arquitectura de software moderna.

*   **Playlist:** [Software Architecture - Drawing Boxes](https://www.youtube.com/playlist?list=PLsrRMpHuSOU1_AaGbbuJSxhYZmhsWYirn)
*   **Descripción:** Abarca conceptos de arquitectura de software, desde microservicios, Clean Architecture, Domain-Driven Design, CQRS y Event Sourcing.

---

### Semana 1: Fundamentos de Domain-Driven Design (DDD)

*   **Objetivo:** Comprender la filosofía de Domain-Driven Design (DDD) y su importancia para el negocio. El desarrollador dominará los conceptos del diseño estratégico, incluyendo el Lenguaje Ubicuo, el Análisis de Dominio y la identificación de Contextos Delimitados (Bounded Contexts) como pilar para el diseño de microservicios. Se introducirán los principios de arquitecturas limpias y la influencia de la estructura organizacional (Ley de Conway) en el software.
*   **Recursos y Prácticas:**
    *   [Análisis de dominio en una arquitectura de microservicios (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/microservices/model/domain-analysis) (1.5h)
    *   [Patrón: Servicio por Equipo (microservices.io)](https://microservices.io/patterns/decomposition/service-per-team.html) (1h)
    *   [Bounded Context - Martin Fowler](https://martinfowler.com/bliki/BoundedContext.html) (1h)
    *   [Video: The Art of Discovering Bounded Contexts (Nick Tune)](https://www.youtube.com/watch?v=ez9GWESKG4I) (1h)
    *   [Video: Hexagonal, Onion & Clean Architecture](https://www.youtube.com/watch?v=JubdZIdLQ4M) (15min)
    *   [Video: Microservices vs Monolithic Architecture](https://www.youtube.com/watch?v=6-Wu178sOEE) (10min)
    *   [Video: DDD Bounded Contexts & Subdomains](https://www.youtube.com/watch?v=NvBsEnDgA4o) (12min)
    *   [Video: Conway’s Law](https://www.youtube.com/watch?v=TqhkWaeUN_8) (8min)
    *   [Video: Boundaries & Encapsulation](https://www.youtube.com/watch?v=EBO0ysJr2BA) (10min)
    *   [Video: DDD and Microservices: At Last, Some Boundaries! - Eric Evans](https://www.youtube.com/watch?v=yPvef9R3k-M) (50min)

### Semana 2: Patrones Tácticos de DDD y Aislamiento de Datos

*   **Objetivo:** Diseñar el interior de un microservicio modelando su lógica de negocio con los patrones tácticos de DDD. El desarrollador aprenderá a identificar y definir Entidades, Objetos de Valor y, fundamentalmente, Agregados (Aggregates) como barreras transaccionales. Se reforzará el principio de autonomía de los servicios a través del patrón de Base de Datos por Servicio para garantizar un bajo acoplamiento.
*   **Recursos y Prácticas:**
    *   [Identificando los bloques de construcción de DDD (Microsoft Docs)](https://docs.microsoft.com/es-es/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/microservice-domain-model) (2h)
    *   [Patrón: Base de Datos por Servicio (microservices.io)](https://microservices.io/patterns/data/database-per-service.html) (1h)
    *   [Video: Dissecting Bounded Contexts (Nick Tune)](https://www.youtube.com/watch?v=zkRfDw0N4W8) (1h)
    *   [Video: DDD Building Blocks](https://www.youtube.com/watch?v=xFl-QQZJFTA) (18min)

### Semana 3: Implementando DDD con CQRS y Event Sourcing

*   **Objetivo:** Entender cómo los patrones CQRS y Event Sourcing sirven como mecanismos para implementar una arquitectura DDD, permitiendo la comunicación y la persistencia basada en eventos.
*   **Lecturas y Videos:**
    *   [Patrón CQRS (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/patterns/cqrs) (1h) - Describe en detalle el patrón de segregación de comandos y consultas.
    *   [Patrón Event Sourcing (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/patterns/event-sourcing) (1.5h) - Introduce el concepto de persistir el estado de una aplicación como una secuencia inmutable de eventos.
    *   [Patrón: Consumidor Idempotente (microservices.io)](https://microservices.io/patterns/communication-style/idempotent-consumer.html) (1h) - Un patrón crucial para evitar el procesamiento duplicado de mensajes en sistemas de comunicación asíncrona.
    *   [Video: DDD, Event Sourcing & CQRS - Teoría y Práctica (YouTube)](https://www.youtube.com/watch?v=rolfJR9ERxo) (1h) - Un recurso visual que conecta la teoría de los tres patrones y muestra su aplicación práctica.
    *   [Video: CQS and CQRS](https://www.youtube.com/watch?v=cqNGAo-9pUE) (10min) - Aclarando la diferencia entre CQS y CQRS.
    *   [Video: Events vs Commands](https://www.youtube.com/watch?v=vS7sCJ1uezY) (8min) - Diferencias clave para arquitecturas basadas en eventos.
    *   [Video: Event Sourcing Explained](https://www.youtube.com/watch?v=yFjzGRb8NOk) (15min) - Una explicación clara del patrón Event Sourcing.
    *   [Video: Outbox Pattern](https://www.youtube.com/watch?v=tQw99alEVHo) (12min) - Solucionando fallos en la entrega de eventos.

### Semana 4: Exposición de APIs y Aceleración del Desarrollo

*   **Objetivo:** Aprender a exponer los servicios al mundo exterior de forma segura y a utilizar patrones que aceleran y estandarizan el desarrollo.
*   **Lecturas:**
    *   [Patrón: API Gateway (microservices.io)](https://microservices.io/patterns/apigateway.html) (1.5h) - Explica cómo un API Gateway puede actuar como punto de entrada único, simplificando la comunicación y la seguridad.
    *   [Patrón: Token de Acceso (microservices.io)](https://microservices.io/patterns/security/access-token.html) (1h) - Describe cómo propagar la identidad del usuario de forma segura a través de las llamadas a los servicios.
    *   [Patrón: Microservice Chassis (microservices.io)](https://microservices.io/patterns/microservice-chassis.html) (1h) - Describe cómo crear un framework base con funcionalidades transversales como logging, métricas y configuración.
    *   [Patrón: Plantilla de Servicio (microservices.io)](https://microservices.io/patterns/service-template.html) (1h) - Presenta una forma de estandarizar y acelerar la creación de nuevos servicios a partir de una base predefinida.

### Semana 5: Despliegue, Consistencia y Composición de UI

*   **Objetivo:** Aprender a empaquetar y desplegar servicios, gestionar la consistencia de datos a través de ellos con Sagas y componer interfaces de usuario a partir de múltiples servicios.
*   **Lecturas:**
    *   [Patrón: Servicio por Contenedor (microservices.io)](https://microservices.io/patterns/deployment/service-per-container.html) (1.5h) - Explica los beneficios de desplegar cada instancia de servicio en su propio contenedor.
    *   [Patrón Saga (microservices.io)](https://microservices.io/patterns/data/saga.html) (1.5h) - Una guía completa sobre cómo gestionar la consistencia de datos a través de servicios sin transacciones distribuidas.
    *   [Patrón Saga (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/patterns/saga) (1h) - Documentación oficial de Microsoft sobre el patrón Saga.
    *   [Patrón: Composición de Fragmentos de UI en el Servidor (microservices.io)](https://microservices.io/patterns/ui/server-side-page-fragment-composition.html) (1h) - Muestra una técnica para construir interfaces de usuario complejas a partir de fragmentos generados por diferentes microservicios.