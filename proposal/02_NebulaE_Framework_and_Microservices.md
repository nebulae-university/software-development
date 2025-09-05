# Path 2: Framework NebulaE y Microservicios

## Objetivo del Path

Este es el path más importante y práctico. Se centra en el "cómo" materializamos nuestros principios arquitectónicos en código funcional. El desarrollador aprenderá a usar nuestras herramientas internas para ser productivo desde el primer día, dominando el uso del framework de NebulaE para crear, desarrollar, probar y desplegar microservicios full-stack siguiendo nuestras convenciones y patrones.

### Descripción General del Path

Si el Path 1 fue el "qué" y el "porqué" de nuestra arquitectura, este Path es el **"cómo"**. Aquí es donde la teoría se encuentra con la realidad del código. El propósito de este camino es darte un dominio completo y práctico del **Framework NebulaE**, un conjunto de herramientas y convenciones diseñadas para acelerar el desarrollo de microservicios sin sacrificar los principios arquitectónicos que aprendiste. Dejarás de ser un espectador de la arquitectura para convertirte en su constructor.

**¿Qué se espera de ti?**
Se espera que te ensucies las manos. Este es un path de construcción, no de contemplación. Deberás seguir los tutoriales, ejecutar los comandos del CLI, escribir código tanto en el backend como en el frontend, y depurar los problemas que surjan. La meta es que al final de este recorrido, el framework no sea una "caja negra", sino un conjunto de herramientas que entiendes y puedes usar con confianza para materializar ideas de negocio en software funcional.

**¿Qué vas a aprender?**
Este Path te llevará en un viaje práctico a través del ciclo de vida completo de un microservicio full-stack:

1.  **Dominio del CLI (`@nebulae/cli`):** Aprenderás a usar nuestra herramienta de línea de comandos como tu principal aliado para generar nuevos servicios, crear esqueletos de entidades de negocio (CRUDs) y automatizar tareas repetitivas.

2.  **Construcción del Backend (Lado de Escritura):** Implementarás la lógica de negocio de tu servicio. Definirás `Comandos`, los procesarás en el backend, y publicarás `Eventos de Dominio` usando nuestro paquete `@nebulae/event-store`, el corazón de nuestro sistema de Event Sourcing.

3.  **Desarrollo de APIs y Frontend (Lado de Lectura):** Expondrás tu lógica a través de una API de GraphQL y construirás una interfaz de usuario en React para interactuar con ella. Conectarás formularios para ejecutar `mutations` (comandos) y crearás vistas para mostrar datos a través de `queries`.

4.  **Comunicación Asíncrona:** Irás más allá de un solo servicio y aprenderás a publicar y consumir eventos de dominio, permitiendo que tus microservicios colaboren de forma desacoplada y resiliente.

5.  **Ciclo de Vida y Operaciones:** Finalmente, aprenderás a gestionar la configuración de tu servicio para diferentes entornos, a empaquetarlo con Docker y a entender los fundamentos del despliegue continuo y la depuración en un entorno distribuido.

Al finalizar, habrás construido, desde cero, un microservicio completo, funcional y alineado con todos los patrones de NebulaE.

## Herramientas del Framework NebulaE

Para facilitar el desarrollo y la adopción de nuestros patrones, el framework NebulaE proporciona las siguientes herramientas clave:

*   **`@nebulae/cli`**: Una herramienta de línea de comandos (CLI) diseñada para asistir en la construcción y despliegue de microservicios cloud-native. Provee generadores de código y utilidades para automatizar tareas como la actualización de almacenes de datos, subida de archivos, configuración de entornos y generación de código para backend, frontend y middleware.
    *   [npm: @nebulae/cli](https://www.npmjs.com/package/@nebulae/cli)
    *   [Architecture Overview](https://www.npmjs.com/package/@nebulae/cli#architecture-overview)

*   **`@nebulae/event-store`**: Un paquete que proporciona una solución de Event Store, fundamental para arquitecturas de Event Sourcing y Microservicios. Desarrollado y mantenido por Nebula Engineering SAS.
    *   [npm: @nebulae/event-store](https://www.npmjs.com/package/@nebulae/event-store)

*   **`@nebulae/backend-node-tools`**: Una librería cliente que ofrece varias herramientas transversales para el desarrollo de micro-backends dentro del Framework de Microservicios NebulaE. Incluye un logger de consola, manejo de errores personalizado, herramientas de autenticación para verificación de roles de usuario, una factoría de brokers para MQTT o Google Cloud PubSub, herramientas CQRS para manejo de respuestas, y un motor de reglas de negocio capaz de ejecutar scripts Lua y JavaScript en tiempo de ejecución.
    *   [npm: @nebulae/backend-node-tools](https://www.npmjs.com/package/@nebulae/backend-node-tools)

## Plan de Estudios

El plan se divide en 5 semanas, enfocándose en la aplicación práctica de los patrones de NebulaE, desde la creación de un servicio hasta su despliegue y comunicación.

---

### Semana 1: Inmersión en el Ecosistema NebulaE: Arquitectura y Primer Microservicio

*   **Objetivo:** El desarrollador se sumergirá en la arquitectura y filosofía del framework NebulaE, estudiando sus herramientas clave como `@nebulae/cli` y `@nebulae/event-store`. Comprenderá la anatomía de un microservicio, los patrones de diseño subyacentes como CQRS y Event Sourcing, y la composición de micro-frontends. La semana culmina con la instalación completa del entorno de desarrollo y la generación de un microservicio funcional, estableciendo una base sólida para el desarrollo práctico.
*   **Recursos y Prácticas:**
    *   [npm: @nebulae/cli](https://www.npmjs.com/package/@nebulae/cli)
    *   [Architecture Overview](https://www.npmjs.com/package/@nebulae/cli#architecture-overview)
    *   [npm: @nebulae/event-store](https://www.npmjs.com/package/@nebulae/event-store)
    *   [npm: @nebulae/backend-node-tools](https://www.npmjs.com/package/@nebulae/backend-node-tools)
    *   [GitHub: nebulae-university/repositories](https://github.com/orgs/nebulae-university/repositories)
    *   [Nebulae Microservice Anatomy Overview](https://github.com/nebulae-university/software-development/blob/main/documents/nebulae_microservice_anatomy_overview.md)
    *   [Architecture Benchmark Analysis: Gemini](https://github.com/nebulae-university/software-development/blob/main/documents/architecture_benchmark_analysis_gemini.md)
    *   [Architecture Benchmark Analysis: Sonnet](https://github.com/nebulae-university/software-development/blob/main/documents/architecture_benchmark_analysis_sonnet.md)
    *   [Micro-frontends Pattern: Server-side page fragment composition](https://microservices.io/patterns/ui/server-side-page-fragment-composition.html)
    *   [Micro-frontends in Action: Chapter 4](https://livebook.manning.com/book/micro-frontends-in-action/chapter-4)
    *   [API Gateway Pattern](https://microservices.io/patterns/apigateway.html)
    *   [Video: Vista General de Arquitectura](https://www.youtube.com/watch?v=CxbGZhWJDkM) (1h)
    *   [Video: Estructura y Arquitectura de un Microservicio NebulaE](https://www.youtube.com/watch?v=8XgWmuzcAkE) (1h)
    *   [Video: Instalación del Entorno y Generación de Primer Microservicio](https://youtu.be/MdLlDh7y9kI)

### Semana 2: Construcción Full-Stack de una Entidad de Negocio

*   **Objetivo:** El desarrollador aplicará los patrones de NebulaE para construir una funcionalidad de negocio completa. Aprenderá a modificar el esqueleto de una entidad, implementar la lógica de negocio de los Comandos en el backend con NodeJS y RxJS, conectar las mutaciones y queries de la API de GraphQL con la lógica del backend, y generar las vistas de frontend en React para interactuar con la nueva entidad. Esta semana se enfoca en el flujo de desarrollo completo, desde la lógica de negocio hasta la interfaz de usuario.
*   **Recursos y Prácticas:**
    *   [Video: Modificación básica FullStack de un µServicio NebulaE](https://youtu.be/GC8qjgkX3F8)
    *   [Video: Implementación de Lógica de Comandos en el Backend](https://youtu.be/5HiQB8uWhfM)
    *   [Video: Conexión API GraphQL con FrontEnd y Backend](https://youtu.be/PIptkzY6TFk)
    *   [Video: Generación de Nueva Vista FrontEnd](https://youtu.be/9M1GhET8kC0)

### Semana 3: Conectando Frontend y Backend

*   **Objetivo:** Profundizar en la implementación de los patrones de NebulaE tanto en el frontend como en el backend. El desarrollador comprenderá la arquitectura de componentes de la UI, incluyendo la gestión de estado con `Redux` y `useState`. Simultáneamente, implementará la lógica de negocio principal en el backend, utilizando RxJS para orquestar los flujos de CQRS y Event Sourcing, y conectando la capa de GraphQL con MongoDB para el procesamiento avanzado de datos.
*   **Recursos y Prácticas:**
    *   [Entender los componentes base, el uso de Material UI, Formik, Redux y useState en el frontend de NebulaE.](https://www.youtube.com/watch?v=dummy_video)
    *   [Implementación de RxJS para procesar CQRS y EventSourcing en el backend de NebulaE.](https://www.youtube.com/watch?v=dummy_video)
    *   [Escenarios de uso de queries y mutaciones con MongoDB para procesamiento de datos en el backend de NebulaE.](https://www.youtube.com/watch?v=dummy_video)

### Semana 4: Comunicación Asíncrona con Eventos

*   **Objetivo:** Implementar la comunicación entre microservicios mediante la publicación y consumo de eventos de dominio, aplicando los patrones correspondientes.
*   **Recursos y Prácticas:**
    *   [Flujo Completo de Eventos: Publicación, Consumo e Idempotencia](https://www.youtube.com/watch?v=dummy_video) (2h) - Comprender cómo publicar eventos de dominio a través del broker de mensajería, cómo implementar un consumidor en otro microservicio que reaccione a los eventos publicados teniendo en cuenta el consumidor idempotente.

### Semana 5: Configuración, Despliegue y Operación

*   **Objetivo:** Aprender a configurar, desplegar y depurar un microservicio en diferentes entornos, entendiendo los fundamentos de su ciclo de vida.
*   **Recursos y Prácticas:**
    *   [Configuración Externalizada en NebulaE](https://www.youtube.com/watch?v=dummy_video) (1.5h) - Aprende a gestionar la configuración de un servicio para diferentes entornos (local, staging, prod).
    *   [Entendiendo el Despliegue con Docker y GitLab CI]https://www.youtube.com/watch?v=dummy_video) (1.5h) - Analiza el `docker-compose.yml` local y los pasos de un pipeline de CI/CD de ejemplo.
    *   [Técnicas de Debugging Full-Stack](https://www.youtube.com/watch?v=dummy_video) (1.5h) - Aprender a trazar y depurar un problema desde el frontend hasta el backend.
