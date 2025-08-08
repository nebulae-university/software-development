# Path 5: Persistencia de Datos y Mensajería

## Objetivo del Path

Este path está diseñado para que el desarrollador domine las tecnologías y patrones de persistencia de datos y mensajería asíncrona que son fundamentales en la arquitectura de NebulaE. Al finalizar, el desarrollador será capaz de modelar datos de forma eficiente para alto rendimiento, interactuar con bases de datos MongoDB a nivel experto, administrar un clúster, optimizar consultas complejas, **implementar la comunicación asíncrona con MQTT y comprender los fundamentos de NATS y Google Pub/Sub.**

## Plan de Estudios

El plan se divide en 5 semanas, combinando dos learning paths principales de MongoDB University, un skill path enfocado en **Performance** y **recursos clave sobre sistemas de mensajería asíncrona**. Esta estructura asegura una progresión lógica desde los fundamentos del desarrollo hasta la administración avanzada, la optimización y la comunicación entre servicios.

---

### Semana 1: Fundamentos de MongoDB para Desarrolladores

*   **Objetivo:** Establecer una base sólida en el ecosistema de MongoDB, comprendiendo su arquitectura, el modelo de documentos y cómo interactuar con la base de datos desde el `mongo shell` y una aplicación Node.js.
*   **Cursos (Node.js Developer Path):**
    *   [Intro to MongoDB](https://learn.mongodb.com/courses/start-here-introduction-to-mongodb) (1.25h)
    *   [Getting Started with MongoDB Atlas](https://learn.mongodb.com/courses/getting-started-with-mongodb-atlas) (1.25h)
    *   [MongoDB and the Document Model](https://learn.mongodb.com/courses/overview-of-mongodb-and-the-document-model) (1.25h)
    *   [Connecting to a MongoDB Database Using the MongoDB Shell](https://learn.mongodb.com/courses/connecting-to-a-mongodb-database-using-the-mongodb-shell) (1.75h)
    *   [Connecting to MongoDB in Node.js](https://learn.mongodb.com/courses/connecting-to-mongodb-in-nodejs) (1h)

### Semana 2: Operaciones CRUD y Modelado de Datos

*   **Objetivo:** Dominar las operaciones de Crear, Leer, Actualizar y Eliminar (CRUD) y aprender los principios del modelado de datos en MongoDB para diseñar schemas eficientes.
*   **Cursos (Node.js Developer Path & Admin Path):**
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
