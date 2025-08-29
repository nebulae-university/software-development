# Plan de Estudios Detallado: Semana 3

## Objetivo de la Semana

Al finalizar esta semana, el desarrollador será capaz de **implementar la comunicación entre microservicios y conectar el frontend con el backend de forma avanzada**. Habrá dominado:

1.  **CQRS y Event Sourcing:** Entender la implementación de estos patrones para la comunicación y persistencia.
2.  **Conexión Frontend-Backend:** Profundizar en la implementación de los patrones de NebulaE en ambas capas.
3.  **Filtrado y Transformación con RxJS:** Dominar los operadores de RxJS para manipular flujos de datos.
4.  **Fetching de Datos con GraphQL:** Conectar el frontend con el backend utilizando GraphQL para queries y mutations.
5.  **Optimización de Consultas y Mensajería:** Aprender a optimizar consultas con índices y entender los fundamentos de MQTT.
6.  **Operación en la Nube:** Conectarse y operar en un entorno de GCP y GKE pre-existente.

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
| **1** | Patrón CQRS | - | Operadores de filtrado (`filter`, `debounceTime`, `throttleTime`) | Queries con Apollo Client | Índices en MongoDB | Conexión al Entorno GCP y GKE |
| **2** | Patrón Event Sourcing | Componentes base de UI | Operadores de filtrado (`first`, `last`, `take`, `takeUntil`) | Mutations con Apollo Client | Agregaciones en MongoDB | Inspección y Depuración en Kubernetes |
| **3** | Patrón Consumidor Idempotente | Implementación de RxJS en Backend | Operadores de transformación (`mergeMap`, `concatMap`) | Context API y `useContext` | Agregaciones con Node.js | Acceso a Servicios Internos del Clúster |
| **4** | Eventos vs Comandos | Escenarios de uso de GraphQL con MongoDB | Operadores de transformación (`groupBy`, `map`, `reduce`) | - | Introducción a MQTT | Interacción con Google Cloud Pub/Sub desde CLI |
| **5** | **Práctica Integral:** Diseño de un flujo de eventos | **Práctica Integral:** Conexión avanzada | **Práctica Integral:** Transformación de datos | **Práctica Integral:** Fetching y estado local | **Práctica Integral:** Optimización y mensajería | **Práctica Integral:** Operación en la nube |

---

## Día 1: Segregación de Responsabilidades y Conexión a la Nube

### Introducción del Día

¡Comenzamos la tercera semana! Hoy nos enfocaremos en la segregación de responsabilidades con CQRS y en cómo conectar nuestro frontend a la API de GraphQL. También aprenderemos a optimizar nuestras consultas en MongoDB y a conectarnos a un entorno de nube real. Al final del día, habrás separado la lógica de lectura y escritura, y podrás obtener datos del backend de forma eficiente.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrón CQRS (Path 1)
*   **Módulo 2:** Operadores de Filtrado en RxJS (Path 3)
*   **Módulo 3:** Queries con Apollo Client (Path 4)
*   **Módulo 4:** Índices en MongoDB (Path 5)
*   **Módulo 5:** Conexión al Entorno GCP y GKE (Path 6)

### Módulo 1: Patrón CQRS (Path 1)
*   **Objetivo:** Entender el patrón de Segregación de Responsabilidad de Comandos y Consultas (CQRS).
*   **Descripción:** CQRS es un patrón arquitectónico que separa los modelos para leer y escribir datos. En lugar de usar el mismo modelo para consultas y actualizaciones, CQRS utiliza modelos distintos para cada uno. Esto permite optimizar cada modelo de forma independiente: el modelo de escritura se enfoca en la consistencia y la validación, mientras que el modelo de lectura se optimiza para el rendimiento de las consultas.
*   **Recursos Web:**
    *   [Patrón CQRS (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/patterns/cqrs) (1h)
*   **Videos:**
    *   [CQS and CQRS](https://www.youtube.com/watch?v=cqNGAo-9pUE) (10min)

### Módulo 2: Operadores de Filtrado en RxJS (Path 3)
*   **Objetivo:** Dominar los operadores de RxJS para filtrar flujos de datos.
*   **Descripción:** Hoy comenzarás a explorar los operadores de filtrado de RxJS. Estos operadores te permiten controlar qué valores de un flujo de datos se emiten, basándose en ciertas condiciones.
*   **Recursos Web:**
    *   [Operador `filter` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/filter) (1h)
    *   [Operador `debounceTime` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/debouncetime) (0.5h)
    *   [Operador `throttleTime` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/throttletime) (0.5h)
*   **Videos:**
    *   [filter](https://www.youtube.com/watch?v=w44c1VXtRKc)
    *   [debounceTime](https://www.youtube.com/watch?v=VmBKiLqeSPo)
    *   [throttleTime](https://www.youtube.com/watch?v=lDPcJxSsYZY)

### Módulo 3: Queries con Apollo Client (Path 4)
*   **Objetivo:** Aprender a obtener datos de una API de GraphQL utilizando Apollo Client.
*   **Descripción:** Apollo Client es una librería de gestión de estado para GraphQL que simplifica la comunicación con el backend. En este módulo, aprenderás a realizar queries para obtener los datos que necesitas para tus componentes de React.
*   **Recursos Web:**
    *   [Queries con Apollo Client (Apollo GraphQL Docs)](https://www.apollographql.com/docs/react/data/queries/) (1.5h)
*   **Videos:**
    *   [Crash Course React con GraphQL y Apollo Client](https://www.youtube.com/watch?v=gAbIQx26wSI)

### Módulo 4: Índices en MongoDB (Path 5)
*   **Objetivo:** Aprender a crear y utilizar índices para optimizar el rendimiento de las consultas en MongoDB.
*   **Descripción:** Los índices son estructuras de datos especiales que almacenan una pequeña porción de los datos de la colección de una forma fácil de recorrer. La creación de índices adecuados puede mejorar drásticamente el rendimiento de las consultas.
*   **Recursos Web:**
    *   [MongoDB Indexes](https://learn.mongodb.com/courses/mongodb-indexes) (1.75h)

### Módulo 5: Conexión al Entorno GCP y GKE (Path 6)
*   **Objetivo:** Aprender a conectarse a un entorno de Google Cloud Platform (GCP) y Kubernetes (GKE) pre-existente.
*   **Descripción:** En este módulo, darás tus primeros pasos en la operación de un entorno de nube real. Aprenderás a configurar las herramientas de línea de comandos para interactuar con GCP y GKE.
*   **Recursos Web:**
    *   [Instalación y Configuración de Google Cloud CLI](https://cloud.google.com/sdk/docs/install)

---

## Día 2: Persistencia Basada en Eventos y Mutaciones

### Introducción del Día

Hoy profundizaremos en la persistencia basada en eventos con Event Sourcing y cómo realizar mutaciones desde nuestro frontend. Continuaremos con los operadores de filtrado en RxJS y las agregaciones en MongoDB, y aprenderemos a inspeccionar y depurar aplicaciones en Kubernetes.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrón Event Sourcing (Path 1)
*   **Módulo 2:** Componentes Base de UI (Path 2)
*   **Módulo 3:** Operadores de Filtrado en RxJS (Path 3)
*   **Módulo 4:** Mutations con Apollo Client (Path 4)
*   **Módulo 5:** Agregaciones en MongoDB (Path 5)
*   **Módulo 6:** Inspección y Depuración en Kubernetes (Path 6)

### Módulo 1: Patrón Event Sourcing (Path 1)
*   **Objetivo:** Entender el concepto de persistir el estado de una aplicación como una secuencia inmutable de eventos.
*   **Descripción:** Event Sourcing es un patrón en el que todos los cambios en el estado de una aplicación se almacenan como una secuencia de eventos. Esto no solo proporciona un registro de auditoría completo, sino que también permite reconstruir el estado de la aplicación en cualquier momento.
*   **Recursos Web:**
    *   [Patrón Event Sourcing (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/patterns/event-sourcing) (1.5h)
*   **Videos:**
    *   [Event Sourcing Explained](https://www.youtube.com/watch?v=yFjzGRb8NOk) (15min)

### Módulo 2: Componentes Base de UI (Path 2)
*   **Objetivo:** Entender los componentes base, el uso de Material UI, Formik, Redux useContext y useState en el frontend de NebulaE.
*   **Descripción:** Este módulo se enfoca en comprender la arquitectura de componentes de la UI de NebulaE. Analizarás cómo se utilizan las librerías clave para construir interfaces de usuario robustas y mantenibles.
*   **Recursos Web:**
    *   [Entender los componentes base, el uso de Material UI, Formik, Redux y useState en el frontend de NebulaE.](https://youtu.be/wjHnL6w6GNw)

### Módulo 3: Operadores de Filtrado en RxJS (Path 3)
*   **Objetivo:** Continuar dominando los operadores de filtrado de RxJS.
*   **Descripción:** Hoy explorarás más operadores de filtrado que te darán un control aún más fino sobre tus flujos de datos.
*   **Recursos Web:**
    *   [Operador `first` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/first) (0.5h)
    *   [Operador `last` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/last) (0.5h)
    *   [Operador `take` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/take) (0.5h)
    *   [Operador `takeUntil` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/takeuntil) (0.5h)
*   **Videos:**
    *   [first](https://www.youtube.com/watch?v=d8RQs9ZXieE)
    *   [last](https://www.youtube.com/watch?v=XNWdxPK9zZs)
    *   [take](https://www.youtube.com/watch?v=FAZRFXg80k0)
    *   [takeUntil](https://www.youtube.com/watch?v=KkgE3Ct3Djc)

### Módulo 4: Mutations con Apollo Client (Path 4)
*   **Objetivo:** Aprender a enviar datos y modificar el estado en el backend utilizando mutaciones de GraphQL con Apollo Client.
*   **Descripción:** Las mutaciones son la forma en que se realizan cambios en los datos en una API de GraphQL. En este módulo, aprenderás a ejecutar mutaciones desde tu aplicación de React para crear, actualizar o eliminar datos.
*   **Recursos Web:**
    *   [Mutations con Apollo Client (Apollo GraphQL Docs)](https://www.apollographql.com/docs/react/data/mutations/) (1.5h)
*   **Videos:**
    *   [Usando GraphQL, React y Apollo Client](https://www.youtube.com/watch?v=vy9x1Rn0arY)

### Módulo 5: Agregaciones en MongoDB (Path 5)
*   **Objetivo:** Aprender a utilizar el Aggregation Framework de MongoDB para realizar consultas complejas.
*   **Descripción:** El Aggregation Framework es una de las características más potentes de MongoDB. Permite procesar datos a través de un pipeline de etapas, realizando transformaciones, agrupaciones y cálculos complejos.
*   **Recursos Web:**
    *   [MongoDB Aggregation](https://learn.mongodb.com/courses/mongodb-aggregation) (1.75h)

### Módulo 6: Inspección y Depuración en Kubernetes (Path 6)
*   **Objetivo:** Aprender a inspeccionar y depurar cargas de trabajo en Kubernetes.
*   **Descripción:** En este módulo, aprenderás a utilizar `kubectl` para ver los logs de tus pods, obtener una shell interactiva dentro de un contenedor y diagnosticar problemas comunes.
*   **Recursos Web:**
    *   [Hoja de Referencia (Cheat Sheet) de `kubectl`](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

---

## Día 3: Garantizando la Entrega y el Estado Local

### Introducción del Día

Hoy nos enfocaremos en garantizar la entrega de mensajes con el patrón de consumidor idempotente y en cómo manejar el estado local en nuestras aplicaciones de React. También veremos operadores de transformación en RxJS y cómo acceder a los servicios internos de un clúster de Kubernetes.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrón Consumidor Idempotente (Path 1)
*   **Módulo 2:** Implementación de RxJS en Backend (Path 2)
*   **Módulo 3:** Operadores de Transformación en RxJS (Path 3)
*   **Módulo 4:** Context API y `useContext` (Path 4)
*   **Módulo 5:** Agregaciones con Node.js (Path 5)
*   **Módulo 6:** Acceso a Servicios Internos del Clúster (Path 6)

### Módulo 1: Patrón Consumidor Idempotente (Path 1)
*   **Objetivo:** Entender cómo evitar el procesamiento duplicado de mensajes en sistemas de comunicación asíncrona.
*   **Descripción:** En un sistema distribuido, es posible que un mensaje se entregue más de una vez. Un consumidor idempotente es aquel que puede procesar el mismo mensaje varias veces sin causar efectos secundarios no deseados.
*   **Recursos Web:**
    *   [Patrón: Consumidor Idempotente (microservices.io)](https://microservices.io/patterns/communication-style/idempotent-consumer.html) (1h)

### Módulo 2: Implementación de RxJS en Backend (Path 2)
*   **Objetivo:** Implementar RxJS para procesar CQRS y EventSourcing en el backend de NebulaE.
*   **Descripción:** Este módulo se centra en la aplicación práctica de RxJS para orquestar los flujos de CQRS y Event Sourcing en el backend. Aprenderás a utilizar los operadores de RxJS para manejar la lógica de negocio de una manera reactiva y declarativa.
*   **Recursos Web:**
    *   [Implementación de RxJS para procesar CQRS y EventSourcing en el backend de NebulaE.](https://www.youtube.com/watch?v=dummy_video)

### Módulo 3: Operadores de Transformación en RxJS (Path 3)
*   **Objetivo:** Dominar los operadores de RxJS para transformar los datos que viajan a través de los flujos.
*   **Descripción:** Los operadores de transformación te permiten cambiar la forma de los datos emitidos por un observable.
*   **Recursos Web:**
    *   [Operador `mergeMap` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/mergemap) (1h)
    *   [Operador `concatMap` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/concatmap) (1h)
*   **Videos:**
    *   [mergeMap](https://www.youtube.com/watch?v=Ar_hCJBEG2E)
    *   [concatMap](https://www.youtube.com/watch?v=lM16-E-uCWc)

### Módulo 4: Context API y `useContext` (Path 4)
*   **Objetivo:** Aprender a compartir estado entre componentes sin "prop drilling" utilizando la Context API de React.
*   **Descripción:** La Context API proporciona una forma de pasar datos a través del árbol de componentes sin tener que pasar props manualmente en cada nivel.
*   **Recursos Web:**
    *   [Context API y `useContext` (React.dev)](https://react.dev/reference/react/useContext) (1.5h)
*   **Videos:**
    *   [React Context API y useContext](https://www.youtube.com/watch?v=NT8_dQ954lE)

### Módulo 5: Agregaciones con Node.js (Path 5)
*   **Objetivo:** Implementar el Aggregation Framework de MongoDB en una aplicación Node.js.
*   **Descripción:** En este módulo, aplicarás tus conocimientos sobre el Aggregation Framework para construir consultas complejas en tu aplicación de Node.js.
*   **Recursos Web:**
    *   [MongoDB Aggregation with Node.js](https://learn.mongodb.com/courses/mongodb-aggregation-with-nodejs) (1.25h)

### Módulo 6: Acceso a Servicios Internos del Clúster (Path 6)
*   **Objetivo:** Aprender a acceder a servicios internos de un clúster de Kubernetes desde tu máquina local.
*   **Descripción:** A menudo, necesitarás conectarte a una base de datos u otro servicio que se ejecuta dentro de tu clúster de Kubernetes. En este módulo, aprenderás a utilizar `kubectl port-forward` para lograrlo.
*   **Recursos Web:**
    *   [Documentación Oficial de `kubectl port-forward`](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#port-forward)

---

## Día 4: Eventos vs. Comandos y Mensajería Asíncrona

### Introducción del Día

Hoy aclararemos la diferencia entre eventos y comandos, y nos introduciremos en la mensajería asíncrona con MQTT. Continuaremos con los operadores de transformación en RxJS y aprenderemos a interactuar con Google Cloud Pub/Sub desde la línea de comandos.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Eventos vs Comandos (Path 1)
*   **Módulo 2:** Escenarios de Uso de GraphQL con MongoDB (Path 2)
*   **Módulo 3:** Operadores de Transformación en RxJS (Path 3)
*   **Módulo 4:** -
*   **Módulo 5:** Introducción a MQTT (Path 5)
*   **Módulo 6:** Interacción con Google Cloud Pub/Sub desde CLI (Path 6)

### Módulo 1: Eventos vs Comandos (Path 1)
*   **Objetivo:** Entender las diferencias clave entre eventos y comandos en arquitecturas basadas en eventos.
*   **Descripción:** Los comandos son solicitudes para realizar una acción, mientras que los eventos son notificaciones de que algo ha sucedido. Entender esta diferencia es crucial para diseñar sistemas distribuidos robustos.
*   **Recursos Web:**
    *   [Video: Events vs Commands](https://www.youtube.com/watch?v=vS7sCJ1uezY) (8min)

### Módulo 2: Escenarios de Uso de GraphQL con MongoDB (Path 2)
*   **Objetivo:** Escenarios de uso de queries y mutaciones con MongoDB para procesamiento de datos en el backend de NebulaE.
*   **Descripción:** Este módulo explora cómo se utilizan las queries y mutaciones de GraphQL en combinación con MongoDB para el procesamiento avanzado de datos en el backend.
*   **Recursos Web:**
    *   [Escenarios de uso de queries y mutaciones con MongoDB para procesamiento de datos en el backend de NebulaE.](https://www.youtube.com/watch?v=dummy_video)

### Módulo 3: Operadores de Transformación en RxJS (Path 3)
*   **Objetivo:** Continuar dominando los operadores de transformación de RxJS.
*   **Descripción:** Hoy explorarás más operadores de transformación que te permitirán manipular tus flujos de datos de formas aún más potentes.
*   **Recursos Web:**
    *   [Operador `groupBy` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/groupby) (1h)
    *   [Operador `map` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/map) (0.5h)
    *   [Operador `reduce` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/reduce) (0.5h)
*   **Videos:**
    *   [groupBy](https://www.youtube.com/watch?v=JLYznawrX-8)
    *   [map](https://www.youtube.com/watch?v=-nYQJkMpOHU)
    *   [reduce](https://www.youtube.com/watch?v=96KUjeiNfX8)

### Módulo 5: Introducción a MQTT (Path 5)
*   **Objetivo:** Comprender los conceptos fundamentales del protocolo MQTT.
*   **Descripción:** MQTT es un protocolo de mensajería ligero ideal para la comunicación en sistemas distribuidos y el Internet de las Cosas (IoT). En este módulo, aprenderás los conceptos clave de MQTT, como broker, publisher, subscriber, topics y QoS.
*   **Recursos Web:**
    *   [The Easiest Guide to Getting Started with MQTT](https://www.emqx.com/en/blog/the-easiest-guide-to-getting-started-with-mqtt) (1.5h)

### Módulo 6: Interacción con Google Cloud Pub/Sub desde CLI (Path 6)
*   **Objetivo:** Aprender a publicar y consumir mensajes de Google Cloud Pub/Sub desde la línea de comandos.
*   **Descripción:** Google Cloud Pub/Sub es un servicio de mensajería totalmente gestionado que te permite enviar y recibir mensajes entre aplicaciones. En este módulo, aprenderás a utilizar `gcloud pubsub` para interactuar con el servicio.
*   **Recursos Web:**
    *   [Guía de Inicio Rápido de `gcloud pubsub`](https://cloud.google.com/pubsub/docs/quickstart-cli)

---

## Día 5: Práctica Integral y Consolidación

Esta práctica integral tomará lo aprendido en los 6 paths durante las tres semanas.

### Actividad Final Evaluativa: Evolución del Microservicio `ms-facts-mng`

#### Parte 1: Refactorización a un Modelo Orientado a Eventos

1.  **Comando `importSharkAttacks`:**
    *   Modificar el comando para que, en lugar de escribir directamente en la base de datos, emita un evento `SharkAttackReported` por cada registro.
    *   El evento debe contener toda la información del ataque de tiburón.
2.  **Consumidor de Eventos:**
    *   Crear un consumidor de eventos que escuche los eventos `SharkAttackReported`.
    *   El consumidor será responsable de guardar la información en la colección de MongoDB.
    *   Implementar el patrón de consumidor idempotente para evitar duplicados.

#### Parte 2: Notificación de Eventos con Google Cloud Pub/Sub

1.  **Procesamiento en Paralelo y Publicación de Eventos:**
    *   Modificar el consumidor de eventos (creado en la Parte 1) para que la persistencia en MongoDB y la publicación del nuevo evento en Google Cloud Pub/Sub se realicen en paralelo.
    *   El evento debe ser publicado en el proyecto `nebulae-lab`.
    *   El tópico de Pub/Sub debe seguir el formato `neb-university-[nombre_estudiante]`, donde `[nombre_estudiante]` debe ser reemplazado por el nombre del estudiante.
    *   El mensaje del evento debe contener la información del ataque de tiburón que fue procesado.

2.  **Verificación con gcloud CLI:**
    *   Para verificar la correcta publicación del evento, el estudiante deberá utilizar el comando `gcloud pubsub subscriptions pull` para escuchar y recibir el mensaje desde la suscripción correspondiente al tópico.

#### Parte 3: Dashboard de Estadísticas

1.  **Nueva Vista en el Frontend:**
    *   Crear una nueva vista de "Dashboard".
2.  **Componentes del Dashboard:**
    *   **Total de Ataques:** Mostrar el número total de ataques de tiburones importados.
    *   **Ataques por País:** Mostrar un gráfico de barras con el número de ataques por país (top 5).
    *   **Ataques por Año:** Mostrar un gráfico de líneas con el número de ataques por año.
3.  **Lógica de Backend:**
    *   Crear los endpoints en la API de GraphQL necesarios para obtener los datos para el dashboard.
    *   Utilizar el Aggregation Framework de MongoDB para calcular las estadísticas.

---

### Forma de Entrega

El desarrollador deberá proporcionar la URL de su repositorio público en Github/Gitlab/Bitbucket que contiene el microservicio `ms-facts-mng` refactorizado. El proceso de evaluación seguirá los siguientes pasos:

1.  **Descarga y Configuración:** Se clonará el repositorio y se configurará el entorno local.
2.  **Levantamiento del Entorno:** Se utilizará `docker-compose up` para iniciar toda la infraestructura.
3.  **Prueba de Refactorización (Parte 1):** Se ejecutará la importación y se verificará que los datos se persisten en MongoDB a través del consumidor de eventos. Se probará la idempotencia ejecutando la importación múltiples veces.
4.  **Prueba de Notificación (Parte 2):** Se ejecutará la importación y se utilizará `gcloud pubsub` para verificar que el evento se publica correctamente en el tópico especificado.
5.  **Prueba del Dashboard (Parte 3):** Se accederá a la nueva vista "Dashboard" y se validará que las estadísticas se muestran correctamente, verificando las llamadas a los nuevos endpoints de GraphQL.

### Criterios de Evaluación

La evaluación se basará en una puntuación máxima de 100 puntos, distribuidos de la siguiente manera:

| Criterio | Puntos | Descripción de la Evaluación |
| :--- | :--- | :--- |
| **Parte 1: Modelo Orientado a Eventos** | **(40 Puntos)** | |
| Refactorización del Comando | 15 | El comando `importSharkAttacks` ya no escribe en la base de datos, sino que emite correctamente eventos `SharkAttackReported`. |
| Consumidor de Eventos | 15 | Se ha creado un consumidor que escucha los eventos y persiste la información correctamente en MongoDB. |
| Idempotencia | 10 | El consumidor es idempotente, lo que significa que procesar el mismo evento varias veces no produce registros duplicados. |
| **Parte 2: Notificación con Pub/Sub** | **(30 Puntos)** | |
| Publicación en Paralelo | 15 | El consumidor publica un evento en Google Cloud Pub/Sub en paralelo a la escritura en la base de datos. |
| Configuración de Pub/Sub | 10 | El evento se publica en el proyecto (`nebulae-lab`) y tópico (`neb-university-[nombre_estudiante]`) correctos. |
| Verificación con gcloud | 5 | El estudiante puede demostrar cómo verificar la recepción del mensaje utilizando la CLI de `gcloud`. |
| **Parte 3: Dashboard de Estadísticas** | **(30 Puntos)** | |
| Creación de Endpoints GraphQL | 10 | Se han creado los nuevos endpoints de GraphQL necesarios para las estadísticas del dashboard. |
| Lógica de Agregación | 15 | Los endpoints utilizan el Aggregation Framework de MongoDB de manera eficiente para calcular las estadísticas solicitadas. |
| Visualización en Frontend | 5 | La nueva vista "Dashboard" muestra correctamente el total de ataques, el gráfico de ataques por país y el gráfico de ataques por año. |
| **TOTAL** | **100 Puntos** | |