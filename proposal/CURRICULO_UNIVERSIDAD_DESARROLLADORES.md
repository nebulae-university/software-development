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

| Semana | Path 1: Arquitectura | Path 2: Framework | Path 3: Backend | Path 4: Frontend | Path 5: Persistencia | Path 6: DevOps/Herramientas |
|:------ |:-------------------- |:----------------- |:--------------- |:---------------- |:------------------- |:--------------------------- |
| **1** | Fundamentos de DDD, Contextos Delimitados, Lenguaje Ubicuo | Generar microservicio con CRUD y entender su estructura | Introducción a la lógica de backend generada | Introducción a frontend generado con React y MUI | Fundamentos de MongoDB y modelo de documentos | Configuración de entorno multi-terminal, Docker, nvm |
| **2** | Patrones tácticos DDD (Entidades, Agregados) | Implementar lógica de negocio y API con CLI | Comandos y resolvers GraphQL con RxJS | Formularios con Formik/Yup y validación | Operaciones CRUD y modelado de datos en MongoDB | Uso de cliente GraphQL, observación de logs |
| **3** | CQRS y Event Sourcing aplicados | Publicar/consumir eventos en microservicios | Implementar consumidores idempotentes | Integración frontend con eventos y actualizaciones | Introducción a MQTT y mensajería | Gestión básica de eventos en terminales |
| **4** | Patrones de comunicación y consistencia (Sagas) | Patrones de aceleración de desarrollo y API Gateway | Uso avanzado de operadores RxJS | Estado global con Redux y optimización de UI | Índices y agregaciones en MongoDB | Introducción a CI/CD con GitLab y Kubernetes básico |
| **5** | Despliegue y composición de UI a nivel producción | Preparación de microservicios para producción | Depuración y optimización backend | PWA y mejoras UX | Replicación, seguridad y rendimiento en MongoDB | Despliegue en Kubernetes, monitoreo en GCP, automatización con IA |

---

## Hoja de Ruta Semanal (Progresión de Conocimiento)

| Semana | Objetivo de la Semana | Conocimientos y Competencias Adquiridas |
| ------ | -------------------- | ---------------------------------------- |
| **1** | **Iniciación en el ecosistema NebulaE y fundamentos base** | Configuración completa del entorno de desarrollo multi-terminal, comprensión del modelo arquitectónico de microservicios, primeros pasos en Domain-Driven Design (conceptos de Lenguaje Ubicuo y Contextos Delimitados), uso del CLI NebulaE para generar un servicio con CRUD, exploración inicial del frontend (React + MUI) y backend (NodeJS), conexión y exploración de MongoDB con el modelo de documentos. |
| **2** | **Profundización en modelado de negocio y desarrollo funcional** | Aplicación de patrones tácticos de DDD (Entidades, Objetos de Valor, Agregados), implementación de lógica de negocio en backend con RxJS y GraphQL, creación de formularios complejos en frontend con Formik/Yup, validaciones de datos, ejecución de operaciones CRUD en MongoDB desde NodeJS, optimización inicial de consultas mediante índices. |
| **3** | **Integración asincrónica y comunicación entre microservicios** | Comprensión y aplicación de CQRS y Event Sourcing, publicación y consumo de eventos de dominio, implementación de consumidores idempotentes, integración del frontend para reaccionar a eventos en tiempo real, fundamentos de mensajería asíncrona con MQTT y NATS, monitoreo básico de flujos de eventos desde consola. |
| **4** | **Optimización, consistencia y escalabilidad** | Uso avanzado de operadores RxJS para manipulación y combinación de flujos, gestión de estado global en frontend con Redux, optimización de listas y renderizado con técnicas como `react-window`, comprensión de patrones de comunicación y consistencia (Sagas), consultas avanzadas y agregaciones en MongoDB, introducción a CI/CD con GitLab, despliegues controlados en Kubernetes. |
| **5** | **Producción, orquestación y consolidación de conocimientos** | Preparación de microservicios para entornos de producción, aplicación de patrones de despliegue y composición de UI, depuración avanzada en backend y frontend, implementación de Progressive Web Apps (PWA), configuración de replicación y seguridad en MongoDB, despliegue de servicios en Kubernetes (GKE), monitoreo con herramientas de GCP, automatización de tareas de operación y desarrollo con IA. |

