# Currículo de la Universidad para Desarrolladores NebulaE

## Introducción y Filosofía del Programa

Bienvenido a la **Universidad NebulaE**, el programa intensivo que transforma a desarrolladores con talento en **profesionales productivos, autónomos y alineados con la cultura y estándares de NebulaE**.

Durante **5 semanas**, vivirás una experiencia inmersiva que combina **fundamentos arquitectónicos, prácticas de desarrollo reales y despliegues en entornos productivos**, siempre con un enfoque práctico y conectado a nuestras soluciones más complejas como **FLEET** y proyectos de AFC/ABT.

Nuestra filosofía pedagógica se apoya en tres pilares:

1. **Base sólida desde el primer día**: ensamblar y operar un entorno de desarrollo completo y funcional.
2. **Conocimiento “Just in Time”**: cada concepto se introduce justo cuando es necesario para resolver un reto real.
3. **Aprendizaje progresivo y acumulativo**: revisitar las capas de la aplicación cada semana con mayor complejidad.

---

## Los 6 Paths de Conocimiento

### Path 1: Fundamentos de Arquitectura de Microservicios y DDD

**Objetivo:** Internalizar los principios de diseño y los patrones arquitectónicos que guían la creación de software robusto, escalable y alineado con las necesidades del negocio en NebulaE.

**¿Qué aprenderás?**
- **Domain-Driven Design (DDD):** Filosofía de desarrollo que pone el dominio del negocio en el centro del diseño de software, usando conceptos como Lenguaje Ubicuo y Contextos Delimitados para crear una arquitectura coherente y mantenible.
- **Patrones Tácticos:** Entidades, Objetos de Valor y Agregados para modelar la lógica de negocio de forma efectiva.
- **Arquitecturas Avanzadas:** CQRS (Command Query Responsibility Segregation) y Event Sourcing para sistemas altamente escalables y auditables.
- **Patrones de Comunicación:** API Gateways, tokens de acceso, y composición de interfaces distribuidas.
- **Consistencia de Datos:** Patrón Saga para mantener la consistencia sin transacciones distribuidas.

**Valor para NebulaE:** Este path te capacita para descomponer sistemas complejos en microservicios bien diseñados, siguiendo los principios que hacen que FLEET y otros productos sean escalables y mantenibles.

---

### Path 2: Framework NebulaE y Microservicios

**Objetivo:** Dominar el uso del framework propietario de NebulaE para materializar principios arquitectónicos en código funcional, siendo productivo desde el primer día.

**¿Qué aprenderás?**
- **@nebulae/cli:** Herramienta de línea de comandos para generar, construir y desplegar microservicios cloud-native con generadores de código automatizados.
- **@nebulae/event-store:** Solución de Event Store fundamental para arquitecturas de Event Sourcing y comunicación entre microservicios.
- **@nebulae/backend-node-tools:** Librería con herramientas transversales incluyendo logging, manejo de errores, autenticación, brokers MQTT/Pub-Sub, herramientas CQRS y motor de reglas de negocio.
- **Estructura de Microservicios:** Comprensión profunda de las carpetas `frontend`, `api`, `backend`, `deployment` y `playground`.
- **Ciclo de Vida Completo:** Desde la generación inicial hasta el despliegue en producción, incluyendo configuración externalizada y debugging full-stack.

**Valor para NebulaE:** Este es el path más práctico e importante. Te convierte en un desarrollador productivo que puede crear, extender y mantener microservicios siguiendo las convenciones y patrones específicos de NebulaE.

---

### Path 3: Desarrollo Backend y APIs con NodeJS y RxJS

**Objetivo:** Dominar el desarrollo del lado del servidor con NodeJS, haciendo uso intensivo de programación asíncrona y reactiva para implementar lógicas de negocio complejas y eficientes.

**¿Qué aprenderás?**
- **Fundamentos NodeJS:** Asincronismo con Callbacks, Promises y Async/Await, paradigmas de programación declarativa vs imperativa.
- **Programación Reactiva con RxJS:** Observables, operadores de creación, transformación, filtrado, combinación y manejo de errores para crear flujos de datos robustos.
- **Operadores Esenciales:** `map`, `filter`, `mergeMap`, `forkJoin`, `debounceTime`, `catchError` y muchos más para manipular streams de datos.
- **APIs Robustas:** Diseño e implementación con especificaciones OpenAPI y Express.
- **Optimización Avanzada:** Debugging, memory leaks en RxJS, y representación numérica a bajo nivel.

**Valor para NebulaE:** Te capacita para implementar la lógica de negocio del corazón de los microservicios, usando los mismos patrones reactivos que potencian la escalabilidad de FLEET y otros productos complejos.

---

### Path 4: Desarrollo Frontend con React

**Objetivo:** Construir interfaces de usuario modernas, eficientes y responsivas que se integran perfectamente con la arquitectura de microservicios de NebulaE.

**¿Qué aprenderás?**
- **React Moderno:** Componentes funcionales, hooks (`useState`, `useEffect`, `useCallback`, `useRef`), JSX y renderizado eficiente.
- **Gestión de Estado:** Redux para estado global complejo, Context API para estado compartido, y React Redux con `useSelector` y `useDispatch`.
- **UI/UX Profesional:** Material UI (MUI) para componentes consistentes, Tailwind CSS para estilizado utility-first.
- **Formularios Robustos:** Formik para manejo de estado de formularios y Yup para validación de esquemas.
- **Integración con Backend:** Apollo Client para GraphQL, queries y mutations eficientes.
- **Optimización de Rendimiento:** `React.memo`, virtualización de listas, lazy loading.
- **Tecnologías Avanzadas:** Progressive Web Apps (PWA), Service Workers, Web Workers, WebAssembly.

**Valor para NebulaE:** Te permite crear interfaces de usuario que cumplan con los estándares de calidad y usabilidad de productos como FLEET, integrándose de forma nativa con la arquitectura de microservicios.

---

### Path 5: Persistencia de Datos y Mensajería

**Objetivo:** Dominar las tecnologías de persistencia y mensajería asíncrona fundamentales en la arquitectura de NebulaE para crear sistemas de alto rendimiento y comunicación eficiente entre servicios.

**¿Qué aprenderás?**
- **MongoDB Experto:** Desde fundamentos del modelo de documentos hasta administración avanzada de clústeres, optimización de consultas complejas, índices, agregaciones y replicación.
- **MongoDB Atlas:** Configuración, monitoreo, backup/recovery y seguridad en entornos cloud.
- **Agregaciones Avanzadas:** Pipelines complejos para análisis de datos y reporting.
- **Mensajería Asíncrona:** 
  - **MQTT:** Protocolo ligero para comunicación en tiempo real
  - **NATS y JetStream:** Sistemas de mensajería distribuida de alto rendimiento
  - **Google Pub/Sub:** Mensajería cloud-native para comunicación entre microservicios
- **Implementación Práctica:** Clientes MQTT en Node.js, patrones de publicación/suscripción.

**Valor para NebulaE:** Te capacita para diseñar y optimizar la capa de datos que soporta productos de alta demanda como FLEET, implementando comunicación asíncrona eficiente entre microservicios.

---

### Path 6: DevOps, Cloud y Herramientas

**Objetivo:** Familiarizarte con el ecosistema completo de DevOps y cloud de NebulaE para maximizar productividad, asegurar despliegues fiables e interactuar eficientemente con entornos de producción.

**¿Qué aprenderás?**
- **Línea de Comandos Maestría:** Navegación, manipulación de archivos, búsqueda de texto (`grep`, `find`), pipes, redirección y encadenamiento de comandos.
- **Containerización:** Docker para desarrollo local, Docker Compose para orquestación multi-servicio, creación de imágenes y Dockerfiles.
- **Google Cloud Platform (GCP):**
  - **CLI `gcloud`:** Gestión de proyectos y recursos
  - **Google Kubernetes Engine (GKE):** Creación y gestión de clústeres
  - **kubectl:** Despliegue y gestión de aplicaciones en Kubernetes
  - **Cloud Services:** Pub/Sub, Cloud Storage, Logging y Monitoring
- **CI/CD con GitLab:** Pipelines automatizados, Container Registry, despliegue continuo.
- **Monitoreo y Observabilidad:** Dashboards en Google Monitoring, análisis de logs, métricas de rendimiento.
- **Automatización:** Scripts Bash y uso de herramientas de IA para acelerar tareas operativas.

**Valor para NebulaE:** Te convierte en un desarrollador completamente autónomo que puede manejar el ciclo de vida completo de aplicaciones, desde desarrollo local hasta producción en GCP, usando las mismas herramientas que mantienen FLEET y otros productos críticos funcionando 24/7.

---

## Plan de Estudio Detallado (Semana vs. Path)

| Semana | Path 1: Arquitectura | Path 2: Framework | Path 3: Backend (RxJS) | Path 4: Frontend | Path 5: Persistencia | Path 6: DevOps/Herramientas |
|:------ |:-------------------- |:----------------- |:--------------- |:---------------- |:------------------- |:--------------------------- |
| **1** | Fundamentos de DDD, Contextos Delimitados, Lenguaje Ubicuo | Entender el framework y generar un microservicio | Fundamentos de NodeJS, asincronismo y paradigmas | Fundamentos de React, componentes y hooks | Fundamentos de MongoDB, modelo de documentos y Atlas | Configuración de entorno, CLI, Git y nvm |
| **2** | Patrones tácticos DDD (Entidades, Agregados), Aislamiento de Datos | Implementar lógica de negocio (comandos) y vistas (queries) | Fundamentos de RxJS, creación de streams, Hot/Cold Observables | Estilizado con MUI/Tailwind, formularios con Formik/Yup | Operaciones CRUD, modelado de datos en MongoDB | Docker, Dockerfiles y Docker Compose |
| **3** | CQRS, Event Sourcing, Consumidor Idempotente | Conexión de componentes, implementación de RxJS en backend | Operadores de filtrado y transformación en RxJS | Conexión a APIs con Apollo Client (queries/mutations) | Índices, agregaciones en MongoDB, introducción a MQTT | Conexión a GCP/GKE, `kubectl`, `gcloud pubsub` |
| **4** | API Gateway, Token de Acceso, Plantillas de Servicio | Publicación y consumo de eventos de dominio | Operadores de combinación y manejo de errores en RxJS | Gestión de estado global con Redux, optimización de UI | Administración de BD, NATS y Google Pub/Sub | Despliegue en Kubernetes (YAML) y CI/CD con GitLab |
| **5** | Patrón Saga, Composición de UI | Configuración para producción, debugging full-stack | Diseño de APIs con OpenAPI, debugging avanzado | PWAs, Service Workers, Web Workers, WebAssembly | Rendimiento y seguridad en BD, implementación de cliente MQTT | Monitoreo en GCP, automatización con Bash y IA |

---

## Hoja de Ruta Semanal (Progresión de Conocimiento)

| Semana | Objetivo de la Semana | Conocimientos y Competencias Adquiridas |
| ------ | -------------------- | ---------------------------------------- |
| **1** | **Iniciación en el ecosistema NebulaE y fundamentos base** | Configuración completa del entorno de desarrollo, comprensión del modelo arquitectónico de microservicios, primeros pasos en Domain-Driven Design (Lenguaje Ubicuo, Contextos Delimitados), uso del CLI NebulaE para generar un servicio, exploración inicial del frontend (React + hooks) y backend (NodeJS + asincronismo), conexión y configuración de MongoDB Atlas. |
| **2** | **Construcción y modelado de la lógica de negocio de un microservicio funcional** | Aplicación de patrones tácticos de DDD (Agregados), implementación de lógica de negocio en backend (comandos), creación de formularios complejos en frontend con Formik/Yup y validaciones, ejecución de operaciones CRUD en MongoDB desde NodeJS, empaquetado y ejecución del entorno local con Docker y Docker Compose. |
| **3** | **Aplicación de Patrones de Arquitectura (CQRS/ES) y Conexión de Capas (GraphQL/GKE)** | Comprensión y aplicación de CQRS y Event Sourcing, implementación de consumidores idempotentes, conexión del frontend al backend con GraphQL (queries y mutations), dominio de operadores de filtrado y transformación en RxJS, optimización de consultas con índices y agregaciones en MongoDB, operación de servicios en un entorno de nube (GCP/GKE) con `kubectl`. |
| **4** | **Optimización, consistencia y despliegue automatizado** | Uso avanzado de operadores RxJS para combinación y manejo de errores, gestión de estado global en frontend con Redux, comprensión de patrones de comunicación y consistencia (Sagas, API Gateway), administración de bases de datos, despliegue de aplicaciones en Kubernetes mediante manifiestos y CI/CD con GitLab. |
| **5** | **Preparación para producción, seguridad y tecnologías avanzadas** | Aplicación de patrones de despliegue y composición de UI, depuración avanzada y optimización de rendimiento, implementación de Progressive Web Apps (PWA), configuración de replicación y seguridad en MongoDB, monitoreo de aplicaciones en GCP, automatización de tareas con scripts de Bash y asistentes de IA. |