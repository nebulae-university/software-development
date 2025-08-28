# Path 5: Persistencia de Datos y Mensajería

## Objetivo del Path

Este path está diseñado para que el desarrollador domine las tecnologías y patrones de persistencia de datos y mensajería asíncrona que son fundamentales en la arquitectura de NebulaE. Al finalizar, el desarrollador será capaz de modelar datos de forma eficiente para alto rendimiento, interactuar con bases de datos MongoDB a nivel experto, administrar un clúster, optimizar consultas complejas, **implementar la comunicación asíncrona con MQTT y comprender los fundamentos de NATS y Google Pub/Sub.**

### Descripción General del Path

Este Path te lleva a las capas más profundas y críticas de cualquier sistema de software: los datos y la comunicación. Aquí aprenderás que los datos no son solo algo que se guarda y se recupera, sino que son el activo más valioso del negocio. El propósito de este camino es convertirte en un experto en la gestión de la persistencia y el flujo de información, dominando tanto las bases de datos NoSQL de alto rendimiento como los sistemas de mensajería que permiten a nuestros microservicios colaborar.

**¿Qué se espera de ti?**
Se espera que desarrolles una mentalidad orientada al rendimiento, la durabilidad y la resiliencia de los datos. Deberás pensar no solo en *qué* datos guardar, sino en *cómo* modelarlos para que las consultas sean ultrarrápidas. Te sumergirás en la administración de bases de datos y en la depuración de problemas de rendimiento. Además, adoptarás el paradigma asíncrono, no como una opción, sino como el pilar fundamental para la comunicación en sistemas distribuidos.

**¿Qué vas a aprender?**
Este es un viaje exhaustivo a través de MongoDB y los sistemas de mensajería, que te proporcionará un dominio completo sobre:

1.  **MongoDB de Cero a Experto:**
    *   **Desarrollo:** Dominarás todo el espectro de operaciones CRUD, el Aggregation Framework para consultas complejas y el uso del driver de Node.js.
    *   **Modelado de Datos:** Aprenderás el arte de diseñar esquemas en un modelo de documentos, sabiendo cuándo incrustar (embed) o referenciar datos para un rendimiento óptimo.
    *   **Optimización:** Te convertirás en un experto en rendimiento, aprendiendo a crear índices, analizar planes de consulta y optimizar operaciones lentas.
    *   **Administración:** Adquirirás habilidades de DBA (Administrador de Base de Datos), incluyendo el uso de herramientas, monitorización de métricas, configuración de replicación y estrategias de backup/recovery.

2.  **Maestría en Mensajería Asíncrona:**
    *   **Fundamentos:** Entenderás por qué la comunicación síncrona es frágil en los microservicios y cómo la mensajería asíncrona proporciona desacoplamiento y resiliencia.
    *   **Protocolo MQTT:** Dominarás los conceptos del protocolo MQTT (Broker, Publisher, Subscriber, Topics, QoS), que es nuestra principal elección para la comunicación IoT y de eventos.
    *   **Implementación Práctica:** Construirás clientes en Node.js capaces de conectarse a un broker MQTT para publicar y suscribirse a mensajes.
    *   **Visión del Ecosistema:** Obtendrás una visión general de otras tecnologías importantes como **NATS** y **Google Cloud Pub/Sub**, entendiendo sus casos de uso y diferencias.

Al finalizar este Path, serás el guardián de los datos y la comunicación de NebulaE, capaz de diseñar, construir y mantener la columna vertebral de nuestra arquitectura.

## Plan de Estudios

El plan se divide en 5 semanas, combinando dos learning paths principales de MongoDB University, un skill path enfocado en **Performance** y **recursos clave sobre sistemas de mensajería asíncrona**. Esta estructura asegura una progresión lógica desde los fundamentos del desarrollo hasta la administración avanzada, la optimización y la comunicación entre servicios.

---

### Semana 1: Fundamentos de MongoDB para Desarrolladores

*   **Objetivo:** Establecer una base sólida en el ecosistema de MongoDB. El desarrollador comprenderá la arquitectura de una base de datos orientada a documentos, aprenderá a modelar datos con estrategias de incrustación (embedding) y referencia, configurará un clúster en la nube con MongoDB Atlas y se conectará a él tanto desde la shell interactiva (`mongosh`) como desde una aplicación Node.js.
*   **Recursos y Prácticas:**
    *   [Intro to MongoDB](https://learn.mongodb.com/courses/start-here-introduction-to-mongodb) (1.25h)
    *   [MongoDB and the Document Model](https://learn.mongodb.com/courses/overview-of-mongodb-and-the-document-model) (1.25h)
    *   [Getting Started with MongoDB Atlas](https://learn.mongodb.com/courses/getting-started-with-mongodb-atlas) (1.25h)
    *   [Connecting to a MongoDB Database Using the MongoDB Shell](https://learn.mongodb.com/courses/connecting-to-a-mongodb-database-using-the-mongodb-shell) (1.75h)
    *   [Connecting to MongoDB in Node.js](https://learn.mongodb.com/courses/connecting-to-mongodb-in-nodejs) (1h)

### Semana 2: Operaciones CRUD y Modelado de Datos

*   **Objetivo:** Dominar las operaciones de manipulación de datos (CRUD) y los principios del modelado en MongoDB. El desarrollador implementará la creación, lectura, actualización y eliminación de documentos desde el driver de Node.js. Además, aprenderá los conceptos fundamentales del modelado de datos en un esquema de documentos para diseñar colecciones eficientes y optimizadas para los patrones de lectura de la aplicación.
*   **Recursos y Prácticas:**
    *   [MongoDB CRUD Operations: Insert and Find Documents](https://learn.mongodb.com/courses/mongodb-crud-operations-insert-and-find-documents) (1.75h)
    *   [MongoDB CRUD Operations: Replace and Delete Documents](https://learn.mongodb.com/courses/mongodb-crud-operations-replace-and-delete-documents) (1.75h)
    *   [MongoDB CRUD Operations in Node.js](https://learn.mongodb.com/courses/mongodb-crud-operations-in-nodejs) (2h)
    *   [MongoDB Data Modeling Intro](https://learn.mongodb.com/courses/introduction-to-mongodb-data-modeling) (45min)


### Semana 3: Optimización de Consultas e Introducción a Mensajería

*   **Objetivo:** Aprender a optimizar el rendimiento de las consultas con índices y agregaciones, y **comprender los conceptos fundamentales del protocolo MQTT** como introducción a la mensajería asíncrona.
*   **Cursos (Node.js Developer Path):**
    *   [MongoDB Indexes](https://learn.mongodb.com/courses/mongodb-indexes) (1.75h)
    *   [MongoDB Aggregation](https://learn.mongodb.com/courses/mongodb-aggregation) (1.75h)
    *   [MongoDB Aggregation with Node.js](https://learn.mongodb.com/courses/mongodb-aggregation-with-nodejs) (1.25h)
*   **Lecturas (MQTT):**
    *   **MQTT (Enfoque Principal):** [The Easiest Guide to Getting Started with MQTT](https://www.emqx.com/en/blog/the-easiest-guide-to-getting-started-with-mqtt) (1.5h) - Lectura obligatoria para entender qué es MQTT, cómo funciona y sus conceptos clave.

### Semana 4: Administración de BD y Sistemas de Mensajería

*   **Objetivo:** Adquirir habilidades de administración de bases de datos y **obtener una visión general de los sistemas de mensajería NATS y Google Pub/Sub**.
*   **Cursos (Database Admin Path):**
    *   [MongoDB Database Administrator Tools](https://learn.mongodb.com/courses/mongodb-database-administrator-tools) (2.5h)
    *   [MongoDB Database Metrics & Monitoring](https://learn.mongodb.com/courses/mongodb-database-metrics-monitoring) (1h)
    *   [Self-Managed Backup & Recovery](https://learn.mongodb.com/courses/self-managed-backup-recovery) (1h)
    *   [MongoDB Logging Basics](https://learn.mongodb.com/courses/mongodb-logging-basics) (1h)
*   **Lecturas (Sistemas de Mensajería):**
    *   **NATS (Conocimiento Base):** (1h)
        *   [NATS Concepts Overview](https://docs.nats.io/nats-concepts/overview)
        *   [JetStream Concepts](https://docs.nats.io/nats-concepts/jetstream)
    *   **Google Pub/Sub (Conocimiento Base):** (1h)
        *   [Pub/Sub Basics](https://cloud.google.com/pubsub/docs/pubsub-basics)
        *   [Publishing Messages](https://cloud.google.com/pubsub/docs/publish-message-overview)
        *   [Receiving Messages (Subscriptions)](https://cloud.google.com/pubsub/docs/subscription-overview)

### Semana 5: Rendimiento, Seguridad e Implementación de Mensajería

*   **Objetivo:** Profundizar en técnicas avanzadas de optimización y seguridad, y **aplicar los conocimientos de mensajería para implementar un cliente MQTT en Node.js** capaz de publicar y suscribirse a tópicos.
*   **Cursos (Performance & Admin Path):**
    *   [Performance Tools and Techniques](https://learn.mongodb.com/courses/performance-tools-and-techniques) (1h)
    *   [Self-Managed Database Security](https://learn.mongodb.com/courses/mongodb-self-managed-database-security) (2h)
    *   [Replication in MongoDB](https://learn.mongodb.com/courses/replication-in-mongodb) (2h)
*   **Lecturas (Implementación con MQTT & Node.js):**
    *   [Getting Started with Node.js and MQTT](https://blog.risingstack.com/getting-started-with-nodejs-and-mqtt/) (2.5h): Guía práctica para conectar una aplicación Node.js a un broker MQTT, publicar mensajes y suscribirse a tópicos.