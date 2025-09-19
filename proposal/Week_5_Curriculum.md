# Plan de Estudios Detallado: Semana 5

## Objetivo de la Semana

Al finalizar esta semana, el desarrollador estará preparado para **desplegar, operar y optimizar microservicios en un entorno de producción**. Habrá dominado:

1.  **Patrones de Consistencia y Despliegue:** Implementar el patrón Saga para consistencia de datos y empaquetar servicios en contenedores.
2.  **Configuración y Operación Avanzada:** Gestionar la configuración para producción, depurar problemas full-stack y entender el ciclo de vida del despliegue.
3.  **Diseño de APIs y Tópicos Avanzados de Backend:** Diseñar APIs con OpenAPI, entender la representación de datos a bajo nivel y depurar memory leaks.
4.  **Experiencia de Usuario Avanzada (PWA):** Construir Progressive Web Apps con capacidades offline (Service Workers) y procesamiento en segundo plano (Web Workers).
5.  **Rendimiento, Seguridad y Mensajería Avanzada:** Aplicar técnicas de optimización y seguridad en bases de datos e implementar clientes de mensajería MQTT.
6.  **Servicios Cloud, Monitoreo y Automatización:** Utilizar servicios clave de GCP, monitorear aplicaciones y automatizar tareas con scripts.

Esta semana final consolida todo el aprendizaje, enfocándose en las habilidades necesarias para llevar una aplicación del desarrollo a un entorno productivo, robusto y escalable.

## Modalidad de Acompañamiento y Soporte

*   **Foro de Dudas en Classroom:** Para preguntas asíncronas y discusiones técnicas detalladas.
*   **Sesiones de Q&A en Vivo:** 
    *   **lunes:** 3:00 PM - 4:00 PM
    *   **miercoles:** 9:00 AM - 10:00 AM y 3:00 PM - 4:00 PM
    *   **viernes:** 3:00 PM - 4:00 PM
*   **Google NotebookLM:** Herramienta recomendada para estudiar bajo las fuentes del currículo y acelerar la comprensión de conceptos complejos. Utiliza los documentos de cada path como fuentes de conocimiento.
*   **Asistentes de IA:** Se incentiva el uso de ChatGPT, GitHub Copilot, Gemini CLI y Gemini Code Assist para facilitar el entendimiento del código, depuración y exploración de conceptos.

### Resumen de Habilidades por Día y Path

| Día | Path 1: Arquitectura | Path 2: Framework | Path 3: Backend (RxJS) | Path 4: Frontend | Path 5: Persistencia | Path 6: DevOps/Herramientas |
|:--- |:--- |:--- |:--- |:--- |:--- |:--- |
| **1** | Patrón Saga | - | Diseño de APIs con OpenAPI | Introducción a PWAs | Rendimiento en BD | Servicios de GCP: Pub/Sub y Cloud Storage |
| **2** | Patrón Servicio por Contenedor | - | Representación Numérica | Service Workers | Seguridad en BD | Logging y Monitoring en GCP |
| **3** | Patrón Composición de UI | Técnicas de Debugging Full-Stack | Debugging y Memory Leaks en RxJS | Web Workers | Replicación en BD | Creación de Dashboards en GCP |
| **4** | - | Configuración Externalizada | - | Almacenamiento Local | Implementación de Cliente MQTT | Automatización con Bash |
| **5** | - | Entendiendo el Despliegue | - | Introducción a WebAssembly | - | - |

---

## Día 1: Consistencia, Producción y Servicios en la Nube

### Introducción del Día

¡Bienvenido a la última semana! Hoy nos enfocamos en preparar nuestras aplicaciones para el mundo real. Aprenderás a gestionar la consistencia de datos en sistemas distribuidos con el patrón Saga, a diseñar APIs robustas con OpenAPI y a dar el primer paso hacia las Progressive Web Apps. Finalmente, profundizaremos en el rendimiento de bases de datos y en el uso de servicios clave de Google Cloud.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrón Saga (Path 1)
*   **Módulo 2:** Diseño de APIs con OpenAPI (Path 3)
*   **Módulo 3:** Introducción a Progressive Web Apps (PWA) (Path 4)
*   **Módulo 4:** Rendimiento en Bases de Datos (Path 5)
*   **Módulo 5:** Servicios de GCP: Pub/Sub y Cloud Storage (Path 6)

### Módulo 1: Patrón Saga (Path 1)
*   **Objetivo:** Aprender a gestionar la consistencia de datos a través de servicios sin transacciones distribuidas.
*   **Descripción:** En una arquitectura de microservicios, no puedes usar transacciones distribuidas tradicionales. El patrón Saga resuelve este problema gestionando la consistencia a través de una secuencia de transacciones locales. Si una transacción falla, la saga ejecuta una serie de transacciones compensatorias para deshacer los cambios.
*   **Recursos Web:**
    *   [Patrón Saga (microservices.io)](https://microservices.io/patterns/data/saga.html) (1.5h)
    *   [Patrón Saga (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/patterns/saga) (1h)

### Módulo 2: Diseño de APIs con OpenAPI (Path 3)
*   **Objetivo:** Diseñar APIs robustas y bien documentadas utilizando la especificación OpenAPI.
*   **Descripción:** OpenAPI (anteriormente Swagger) es un estándar para describir APIs RESTful. Aprender a definir tus APIs con esta especificación te permite generar documentación interactiva, SDKs de cliente y realizar pruebas de forma automática. Es un pilar del diseño "API-first".
*   **Recursos Web:**
    *   [Referencia de la Especificación OpenAPI 3.1 (Swagger.io)](https://spec.openapis.org/oas/v3.1.0) (2.5h)
*   **Videos:**
    *   [OpenAPI Specification Explained](https://www.youtube.com/watch?v=Sflpzh_cAcA)
    *   [Swagger / OpenAPI Tutorial](https://www.youtube.com/watch?v=vcS9WdFLCbw)

### Módulo 3: Introducción a Progressive Web Apps (PWA) (Path 4)
*   **Objetivo:** Entender los beneficios y fundamentos de las Progressive Web Apps.
*   **Descripción:** Las PWAs son aplicaciones web que utilizan tecnologías modernas para ofrecer una experiencia similar a la de una aplicación nativa. Pueden instalarse en el dispositivo del usuario, funcionar offline y enviar notificaciones push. Este módulo introduce los conceptos básicos y el manifiesto de la aplicación web.
*   **Recursos Web:**
    *   [Introducción a Progressive Web Apps (web.dev)](https://web.dev/learn/pwa/) (1.5h)

### Módulo 4: Rendimiento en Bases de Datos (Path 5)
*   **Objetivo:** Profundizar en técnicas avanzadas de optimización de rendimiento en MongoDB.
*   **Descripción:** Este módulo cubre herramientas y técnicas para diagnosticar y solucionar cuellos de botella en el rendimiento de la base de datos. Aprenderás a analizar planes de consulta, a identificar consultas lentas y a aplicar estrategias de optimización más allá de la simple creación de índices.
*   **Recursos Web:**
    *   [Performance Tools and Techniques](https://learn.mongodb.com/courses/performance-tools-and-techniques) (1h)

### Módulo 5: Servicios de GCP: Pub/Sub y Cloud Storage (Path 6)
*   **Objetivo:** Utilizar servicios clave de Google Cloud Platform para mensajería y almacenamiento.
*   **Descripción:** Aprenderás a interactuar con dos de los servicios más fundamentales de GCP: Pub/Sub, un servicio de mensajería asíncrona global, y Cloud Storage, un sistema de almacenamiento de objetos escalable y duradero. Entenderás sus casos de uso y cómo operarlos desde la CLI.
*   **Recursos Web:**
    *   [Introducción a Pub/Sub (Google Cloud)](https://cloud.google.com/pubsub/docs/overview?hl=es) (1.5h)
    *   [Introducción a Cloud Storage (Google Cloud)](https://cloud.google.com/storage/docs/introduction?hl=es) (1.5h)

---

## Día 2: Despliegue, Seguridad y Monitoreo

### Introducción del Día

Hoy nos enfocamos en el despliegue y la operación. Aprenderás a empaquetar tus servicios en contenedores de manera eficiente. En el frontend, habilitaremos capacidades offline con Service Workers. En la capa de datos, nos centraremos en la seguridad y el monitoreo de nuestras aplicaciones en la nube.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrón Servicio por Contenedor (Path 1)
*   **Módulo 2:** Representación Numérica (Path 3)
*   **Módulo 3:** Service Workers (Path 4)
*   **Módulo 4:** Seguridad en Bases de Datos (Path 5)
*   **Módulo 5:** Logging y Monitoring en GCP (Path 6)

### Módulo 1: Patrón Servicio por Contenedor (Path 1)
*   **Objetivo:** Entender los beneficios de desplegar cada instancia de servicio en su propio contenedor.
*   **Descripción:** Este patrón establece que cada microservicio debe ser empaquetado como una imagen de contenedor y desplegado como un contenedor. Esto proporciona aislamiento, portabilidad y escalabilidad, ya que cada servicio puede ser gestionado y escalado de forma independiente.
*   **Recursos Web:**
    *   [Patrón: Servicio por Contenedor (microservices.io)](https://microservices.io/patterns/deployment/service-per-container.html) (1.5h)

### Módulo 2: Representación Numérica (Path 3)
*   **Objetivo:** Comprender conceptos avanzados de representación de datos como bits, bytes, y endianness.
*   **Descripción:** Para ser un desarrollador backend completo, es útil entender cómo se representan los datos a bajo nivel. Este módulo cubre los fundamentos de los sistemas numéricos binarios y hexadecimales, y cómo se ordenan los bytes en la memoria (endianness), conceptos importantes para la serialización de datos y la interoperabilidad.
*   **Recursos Web:**
    *   [Guías de Representación Numérica](https://www.tutorialspoint.com/digital-electronics/digital-electronics-number-systems.htm) (1h)
*   **Videos:**
    *   [Sistemas numéricos: Binario, Decimal y Hexadecimal](https://www.youtube.com/watch?v=g9-MRBBcvdg)
    *   [LITTLE-ENDIAN VS BIG-ENDIAN ](https://www.youtube.com/watch?v=urFopex6SE0)

### Módulo 3: Service Workers (Path 4)
*   **Objetivo:** Aprender a cachear recursos y habilitar funcionalidades offline en una PWA.
*   **Descripción:** El Service Worker es un script que tu navegador ejecuta en segundo plano, separado de la página web. Es la tecnología clave que permite a las PWAs interceptar peticiones de red, gestionar el caché y ofrecer una experiencia offline.
*   **Recursos Web:**
    *   [Service Workers: Habilitando Offline (MDN)](https://developer.mozilla.org/es/docs/Web/API/Service_Worker_API) (1.5h)

### Módulo 4: Seguridad en Bases de Datos (Path 5)
*   **Objetivo:** Aprender a configurar la seguridad en una base de datos MongoDB auto-gestionada.
*   **Descripción:** Este módulo cubre los aspectos fundamentales de la seguridad en MongoDB, incluyendo la autenticación (quién puede conectarse), la autorización (qué pueden hacer los usuarios), el cifrado de datos en tránsito (TLS/SSL) y en reposo.
*   **Recursos Web:**
    *   [Self-Managed Database Security](https://learn.mongodb.com/courses/mongodb-self-managed-database-security) (2h)

### Módulo 5: Logging y Monitoring en GCP (Path 6)
*   **Objetivo:** Aprender a utilizar los servicios de Logging y Monitoring de Google Cloud.
*   **Descripción:** La observabilidad es crucial en producción. Aprenderás a usar Google Cloud Logging para centralizar y analizar los logs de tus aplicaciones, y Google Cloud Monitoring para recolectar métricas, crear alertas y visualizar el rendimiento de tus servicios.
*   **Recursos Web:**
    *   [Logging (Google Cloud)](https://cloud.google.com/logging/docs/overview?hl=es) (2h)
    *   [Monitoring (Google Cloud)](https://cloud.google.com/monitoring/docs/monitoring-overview?hl=es)

---

## Día 3: Debugging, Composición y Tareas en Segundo Plano

### Introducción del Día

Hoy nos enfocamos en la depuración y la composición. Aprenderás técnicas para depurar problemas que abarcan todo el stack, desde el frontend hasta el backend. Compondremos interfaces de usuario a partir de múltiples microservicios y delegaremos tareas pesadas en el frontend a Web Workers. En la capa de datos, exploraremos la replicación para alta disponibilidad.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrón Composición de UI (Path 1)
*   **Módulo 2:** Técnicas de Debugging Full-Stack (Path 2)
*   **Módulo 3:** Debugging y Memory Leaks en RxJS (Path 3)
*   **Módulo 4:** Web Workers (Path 4)
*   **Módulo 5:** Replicación en MongoDB (Path 5)
*   **Módulo 6:** Creación de Dashboards en GCP (Path 6)

### Módulo 1: Patrón Composición de UI (Path 1)
*   **Objetivo:** Aprender a construir interfaces de usuario complejas a partir de fragmentos generados por diferentes microservicios.
*   **Descripción:** En una arquitectura de micro-frontends, la página que ve el usuario final es a menudo un ensamblaje de fragmentos de HTML, CSS y JavaScript, cada uno propiedad de un equipo y un microservicio diferente. Este patrón explora técnicas para realizar esta composición en el lado del servidor.
*   **Recursos Web:**
    *   [Patrón: Composición de Fragmentos de UI en el Servidor (microservices.io)](https://microservices.io/patterns/ui/server-side-page-fragment-composition.html) (1h)

### Módulo 2: Técnicas de Debugging Full-Stack (Path 2)
*   **Objetivo:** Aprender a trazar y depurar un problema desde el frontend hasta el backend.
*   **Descripción:** La depuración en un sistema distribuido puede ser un desafío. Este módulo te enseñará técnicas y herramientas para seguir una petición a través de las diferentes capas (frontend, API gateway, backend, base de datos), inspeccionar logs y encontrar la causa raíz de un problema.
*   **Recursos Web:**
    *   [Técnicas de Debugging Full-Stack](https://www.youtube.com/watch?v=dummy_video) (1.5h)

### Módulo 3: Debugging y Memory Leaks en RxJS (Path 3)
*   **Objetivo:** Aprender a depurar flujos de RxJS y a prevenir fugas de memoria.
*   **Descripción:** Las suscripciones a observables que no se cancelan son una fuente común de fugas de memoria. Aprenderás a usar operadores como `takeUntil` para gestionar el ciclo de vida de las suscripciones y a usar herramientas de depuración para inspeccionar flujos complejos.
*   **Recursos Web:**
    *   [Artículos sobre Memory Leaks en RxJS](https://medium.com/@benlesh/rxjs-dont-unsubscribe-6753ed4fda87) (1.5h)
*   **Videos:**
    *   [Debugging RxJS](https://www.youtube.com/watch?v=OhuRvfcw3Tw)
    *   [Avoiding Memory Leaks](https://www.youtube.com/watch?v=ZxVN4597RX8)

### Módulo 4: Web Workers (Path 4)
*   **Objetivo:** Aprender a delegar tareas pesadas a un hilo en segundo plano para mantener la UI fluida.
*   **Descripción:** Los Web Workers permiten ejecutar scripts en un hilo de fondo, separado del hilo principal de la UI. Esto es ideal para realizar cálculos intensivos, procesamiento de datos o cualquier tarea que pueda bloquear la interfaz y hacer que la aplicación no responda.
*   **Recursos Web:**
    *   [Web Workers: Ejecución en Segundo Plano (MDN)](https://developer.mozilla.org/es/docs/Web/API/Web_Workers_API) (1h)
*   **Videos:**
    *   [Hooks personalizados + Web Workers](https://www.youtube.com/watch?v=yPAp1h0vk-s) (1h)

### Módulo 5: Replicación en MongoDB (Path 5)
*   **Objetivo:** Entender cómo funciona la replicación en MongoDB para proporcionar redundancia y alta disponibilidad.
*   **Descripción:** La replicación permite mantener copias de tus datos en múltiples servidores. Aprenderás sobre los conjuntos de réplicas (replica sets), el proceso de elección de un primario y cómo la replicación automática garantiza que tu aplicación pueda sobrevivir a la falla de un servidor.
*   **Recursos Web:**
    *   [Replication in MongoDB](https://learn.mongodb.com/courses/replication-in-mongodb) (2h)

### Módulo 6: Creación de Dashboards en GCP (Path 6)
*   **Objetivo:** Aprender a crear dashboards personalizados en Google Cloud Monitoring.
*   **Descripción:** Los dashboards te permiten visualizar las métricas más importantes de tus aplicaciones en un solo lugar. Aprenderás a crear gráficos y tablas para monitorear el rendimiento, la latencia, las tasas de error y otros indicadores clave de la salud de tus servicios.
*   **Recursos Web:**
    *   [Creación de dashboards (Google Cloud)](https://cloud.google.com/monitoring/charts/dashboards?hl=es) (1h)

---

## Día 4: Automatización y Mensajería

### Introducción del Día

Hoy nos enfocamos en la automatización y la persistencia de datos en el cliente. Aprenderás a escribir scripts de Bash para automatizar tareas repetitivas, a gestionar la configuración de tus servicios para diferentes entornos y a implementar un cliente MQTT en Node.js para la comunicación asíncrona. En el frontend, exploraremos las diferentes opciones de almacenamiento en el navegador.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Configuración Externalizada en NebulaE (Path 2)
*   **Módulo 2:** Almacenamiento Local en el Navegador (Path 4)
*   **Módulo 3:** Implementación de Cliente MQTT en Node.js (Path 5)
*   **Módulo 4:** Automatización con Bash (Path 6)

### Módulo 1: Configuración Externalizada en NebulaE (Path 2)
*   **Objetivo:** Aprender a gestionar la configuración de un servicio para diferentes entornos (local, staging, prod).
*   **Descripción:** Nunca se deben codificar valores de configuración (como cadenas de conexión o claves de API) directamente en el código. Este módulo te enseñará cómo el framework NebulaE maneja la configuración externalizada, permitiendo que el mismo artefacto de despliegue se comporte de manera diferente según el entorno en el que se ejecuta.
*   **Recursos Web:**
    *   [Configuración Externalizada en NebulaE](https://www.youtube.com/watch?v=dummy_video) (1.5h)

### Módulo 2: Almacenamiento Local en el Navegador (Path 4)
*   **Objetivo:** Comprender cómo y cuándo usar `localStorage` y `sessionStorage` para persistir datos en el navegador.
*   **Descripción:** La API de Web Storage proporciona mecanismos para que las aplicaciones web almacenen datos clave-valor en el navegador del cliente. Aprenderás la diferencia entre `localStorage` (persiste incluso después de cerrar el navegador) y `sessionStorage` (se borra al cerrar la sesión).
*   **Recursos Web:**
    *   [Almacenamiento Local: `localStorage` vs `sessionStorage` (MDN)](https://developer.mozilla.org/es/docs/Web/API/Web_Storage_API) (0.5h)

### Módulo 3: Implementación de Cliente MQTT en Node.js (Path 5)
*   **Objetivo:** Aplicar los conocimientos de mensajería para implementar un cliente MQTT en Node.js.
*   **Descripción:** Este es un módulo práctico donde construirás una aplicación de Node.js que se conecta a un broker MQTT. Aprenderás a usar una librería de cliente MQTT para publicar mensajes en un tópico y para suscribirte a un tópico y recibir mensajes.
*   **Recursos Web:**
    *   [Getting Started with Node.js and MQTT](https://blog.risingstack.com/getting-started-with-nodejs-and-mqtt/) (2.5h)

### Módulo 4: Automatización con Bash (Path 6)
*   **Objetivo:** Aprender a escribir scripts de Bash para automatizar tareas operativas.
*   **Descripción:** La automatización es un pilar de DevOps. Aprenderás los fundamentos de la programación de scripts de Bash, incluyendo variables, bucles, condicionales y la ejecución de comandos, para automatizar tareas como despliegues, backups o limpieza de entornos.
*   **Recursos Web:**
    *   [Programación de Bash (freeCodeCamp)](https://www.freecodecamp.org/espanol/news/tutorial-de-programacion-de-bash-script-de-shell-de-linux-y-linea-de-comandos-para-principiantes/) (2h)
*   **Videos:**
    *   [Bash Scripting Crash Course](https://www.youtube.com/watch?v=tK9Oc6AEnR4) (2022)

---

## Día 5: Despliegue y Tecnologías de Alto Rendimiento

### Introducción del Día

Llegamos al último día del programa. Hoy conectaremos el desarrollo local con el despliegue automatizado, analizando cómo funciona un pipeline de CI/CD. Además, exploraremos WebAssembly como una opción para llevar el rendimiento del frontend al siguiente nivel. Es el cierre que une todo el ciclo de vida del software.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Entendiendo el Despliegue con Docker y GitLab CI (Path 2)
*   **Módulo 2:** Introducción a WebAssembly (Path 4)

### Módulo 1: Entendiendo el Despliegue con Docker y GitLab CI (Path 2)
*   **Objetivo:** Analizar el `docker-compose.yml` local y los pasos de un pipeline de CI/CD de ejemplo.
*   **Descripción:** Este módulo conecta el desarrollo local con el despliegue automatizado. Analizarás cómo la configuración de Docker Compose para el entorno local se traduce en los pasos que un sistema de CI/CD como GitLab CI ejecutaría para construir, probar y desplegar tu servicio en un entorno de producción.
*   **Recursos Web:**
    *   [Entendiendo el Despliegue con Docker y GitLab CI](https://www.youtube.com/watch?v=dummy_video) (1.5h)

### Módulo 2: Introducción a WebAssembly (Path 4)
*   **Objetivo:** Entender los conceptos clave de WebAssembly y su integración con JavaScript.
*   **Descripción:** WebAssembly (Wasm) es un formato de instrucción binaria para una máquina virtual basada en pila. Wasm está diseñado como un destino de compilación portátil para lenguajes de alto nivel como C/C++/Rust, lo que permite la implementación en la web de aplicaciones de cliente y servidor de alto rendimiento.
*   **Recursos Web:**
    *   [Introducción a WebAssembly (MDN)](https://developer.mozilla.org/es/docs/WebAssembly/Concepts) (1.5h)