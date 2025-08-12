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

### Semana 1: "Hola Mundo" con NebulaE

*   **Objetivo:** Instalar el entorno de desarrollo de NebulaE, generar un microservicio desde cero y comprender su estructura de carpetas fundamental.
*   **Recursos y Prácticas:**
    *   [Creación de tu Primer Microservicio con NebulaE CLI](https://www.youtube.com/watch?v=dummy_video) (1h) - Comprender cómo generar un nuevo servicio y levantarlo con el `integrated-local-environment`.
    *   [Estructura y Arquitectura de un Microservicio NebulaE](https://www.youtube.com/watch?v=dummy_video) (1h) - Entender el propósito de las carpetas `frontend`, `api`, `backend`, `deployment` y `playground`.

### Semana 2: Desarrollando una Entidad de Negocio (Backend)

*   **Objetivo:** Implementar la lógica de negocio y la capa de API para una entidad de negocio completa, siguiendo los patrones de DDD y CQRS dentro del framework.
*   **Recursos y Prácticas:**
    *   [Generación de un CRUD con NebulaE CLI](https://www.youtube.com/watch?v=dummy_video) (1h) - Aprender a generar el esqueleto de una nueva entidad (schema GraphQL, resolvers, etc.).
    *   [Implementación de Lógica de Comandos en el Backend](https://www.youtube.com/watch?v=dummy_video) (2.5h) - Comprender la lógica de negocio para los comandos (Crear, Actualizar, Eliminar) en la capa `backend` usando NodeJS y RxJS.
    *   [Conexión de Resolvers de GraphQL en la API](https://www.youtube.com/watch?v=dummy_video) (1.5h) - Entender cómo conectar las operaciones de GraphQL con el backend.

### Semana 3: Conectando el Frontend

*   **Objetivo:** Construir una interfaz de usuario funcional en React para interactuar con la nueva entidad de negocio, consumiendo la API de GraphQL.
*   **Recursos y Prácticas:**
    *   [Guía de Frontend en NebulaE](https://www.youtube.com/watch?v=dummy_video) (1h) - Entender los componentes base, el uso de Material UI y Formik en el frontend de NebulaE.
    *   [Creación de un Formulario de Alta](https://www.youtube.com/watch?v=dummy_video) (2h) - Aprender a construir un formulario en React para ejecutar mutaciones de GraphQL de creación.
    *   [Mostrando Datos con Queries de GraphQL](https://www.youtube.com/watch?v=dummy_video) (2h) - Comprender cómo crear vistas que consulten y muestren datos de la entidad.

### Semana 4: Comunicación Asíncrona con Eventos

*   **Objetivo:** Implementar la comunicación entre microservicios mediante la publicación y consumo de eventos de dominio, aplicando los patrones correspondientes.
*   **Recursos y Prácticas:**
    *   [Publicación de Eventos de Dominio](https://www.youtube.com/watch?v=dummy_video) (2h) - Comprender cómo publicar eventos de dominio a través de Google Pub/Sub.
    *   [Consumo de Eventos de Dominio](https://www.youtube.com/watch?v=dummy_video) (2h) - Comprender cómo implementar un consumidor en otro microservicio que reaccione a los eventos.
    *   [Patrón: Consumidor Idempotente (microservices.io)](https://www.youtube.com/watch?v=dummy_videol) (1h) - Lectura teórica para entender por qué nuestros consumidores de eventos deben ser idempotentes.

### Semana 5: Configuración, Despliegue y Operación

*   **Objetivo:** Aprender a configurar, desplegar y depurar un microservicio en diferentes entornos, entendiendo los fundamentos de su ciclo de vida.
*   **Recursos y Prácticas:**
    *   [Configuración Externalizada en NebulaE](https://www.youtube.com/watch?v=dummy_video) (1.5h) - Aprende a gestionar la configuración de un servicio para diferentes entornos (local, staging, prod).
    *   [Entendiendo el Despliegue con Docker y GitLab CI]https://www.youtube.com/watch?v=dummy_video) (1.5h) - Analiza el `docker-compose.yml` local y los pasos de un pipeline de CI/CD de ejemplo.
    *   [Técnicas de Debugging Full-Stack](https://www.youtube.com/watch?v=dummy_video) (1.5h) - Aprender a trazar y depurar un problema desde el frontend hasta el backend.
