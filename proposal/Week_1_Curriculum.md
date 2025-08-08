# Plan de Estudios Detallado: Semana 1

## Objetivo de la Semana

Al finalizar esta semana, el desarrollador habrá establecido una **base sólida y operativa** en el ecosistema NebulaE. Será capaz de:

1. **Comprender los fundamentos de DDD:** Lenguaje Ubicuo, Contextos Delimitados y su aplicación en microservicios
2. **Instalar y operar** el entorno de desarrollo de NebulaE con el CLI y estructura de carpetas
3. **Dominar los fundamentos de NodeJS:** Asincronismo, programación declarativa vs imperativa
4. **Crear componentes React básicos:** JSX, hooks (useState, useEffect) y conceptos de Redux
5. **Interactuar con MongoDB:** Modelo de documentos, MongoDB Atlas y conexiones desde Node.js
6. **Configurar herramientas CLI:** Terminal, Docker, nvm y herramientas de desarrollo

Esta semana establece los **fundamentos conceptuales y técnicos** necesarios para ser productivo en NebulaE, proporcionando una base sólida en cada una de las tecnologías core de nuestra arquitectura.

## Modalidad de Acompañamiento y Soporte

*   **Foro de Dudas en Classroom:** Para preguntas asíncronas y discusiones técnicas detalladas.
*   **Sesiones de Q&A en Vivo:** 
    *   **Martes:** 9:00 AM - 10:00 AM y 3:00 PM - 4:00 PM
    *   **Jueves:** 9:00 AM - 10:00 AM y 3:00 PM - 4:00 PM
*   **Google NotebookLM:** Herramienta recomendada para estudiar bajo las fuentes del currículo y acelerar la comprensión de conceptos complejos. Utiliza los documentos de cada path como fuentes de conocimiento.
*   **Asistentes de IA:** Se incentiva el uso de ChatGPT, GitHub Copilot, Gemini CLI y Gemini Code Assist para facilitar el entendimiento del código, depuración y exploración de conceptos.

### Resumen de Habilidades por Día y Path

| Día | Path 1: Arquitectura | Path 2: Framework | Path 3: Backend | Path 4: Frontend | Path 5: Persistencia | Path 6: DevOps/Herramientas |
|:--- |:--- |:--- |:--- |:--- |:--- |:--- |
| **1** | Fundamentos de DDD: Filosofía y Lenguaje Ubicuo | Lectura y entendimiento del framework NebulaE | Fundamentos de NodeJS y paradigmas de programación | Conceptos básicos de React: componentes y JSX | Introducción a MongoDB y modelo de documentos | Configuración del entorno CLI y herramientas básicas |
| **2** | Contextos Delimitados y análisis de dominio | Comprensión de estructura de carpetas de microservicio NebulaE | Asincronismo en JS: Callbacks, Promises, Async/Await | Hooks de React: useState y useEffect | MongoDB Atlas: configuración y primeros pasos | Comandos esenciales de terminal y navegación |
| **3** | - | **Instalación del entorno y generación de primer microservicio** | Programación declarativa vs imperativa | Introducción a Redux: conceptos fundamentales | Conexión a MongoDB usando MongoDB Shell | Manipulación y búsqueda de texto con grep y find |
| **4** | - | - | Métodos de Array y programación funcional | React Redux: Provider, useSelector, useDispatch | Conexión a MongoDB desde Node.js | Encadenamiento de comandos y redirección |
| **5** | - | - | Igualdad y Falsy Values en JavaScript | **Práctica Integral:** Creación de componente completo con hooks | **Práctica Integral:** Operaciones básicas con MongoDB | **Práctica Integral:** Configuración completa del entorno |

---

## Día 1: Fundamentos Conceptuales y Configuración Inicial

### Módulo 1: Fundamentos de Domain-Driven Design (Path 1)
*   **Objetivo:** Comprender la filosofía de DDD, su importancia para el negocio y los conceptos del diseño estratégico.
*   **Descripción:** Introducción a los fundamentos de Domain-Driven Design, enfocándose en cómo DDD guía la creación de software alineado con las necesidades del negocio. Se explorarán los conceptos de Lenguaje Ubicuo y su importancia en la comunicación entre equipos técnicos y de negocio.
*   **Recursos Web:**
    *   [Análisis de dominio en una arquitectura de microservicios (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/microservices/model/domain-analysis) (1.5h)
    *   [Patrón: Servicio por Equipo (microservices.io)](https://microservices.io/patterns/decomposition/service-per-team.html) (1h)
*   **Videos:** [The Art of Discovering Bounded Contexts (Nick Tune)](https://www.youtube.com/watch?v=ez9GWESKG4I) (1h)

### Módulo 2: Lectura y Entendimiento del Framework NebulaE (Path 2)
*   **Objetivo:** Comprender la arquitectura y filosofía del framework NebulaE mediante lectura de documentación.
*   **Descripción:** Estudio teórico del framework NebulaE, sus herramientas principales (@nebulae/cli, @nebulae/event-store, @nebulae/backend-node-tools) y comprensión de la arquitectura general. Se analizará la documentación y se entenderán los principios que guían el desarrollo en NebulaE.
*   **Recursos Web:**
    *   [npm: @nebulae/cli](https://www.npmjs.com/package/@nebulae/cli)
    *   [Architecture Overview](https://www.npmjs.com/package/@nebulae/cli#architecture-overview)
    *   [npm: @nebulae/event-store](https://www.npmjs.com/package/@nebulae/event-store)
    *   [npm: @nebulae/backend-node-tools](https://www.npmjs.com/package/@nebulae/backend-node-tools)
*   **Videos:** [Introducción al Framework NebulaE y sus Componentes]() , [Vista General de Arquitectura](https://www.youtube.com/watch?v=CxbGZhWJDkM) (1h)

### Módulo 3: Fundamentos de NodeJS (Path 3)
*   **Objetivo:** Establecer una base sólida en los paradigmas de programación que guían el estilo de código en NebulaE.
*   **Descripción:** Introducción a los fundamentos de NodeJS y los paradigmas de programación declarativa vs imperativa. Se establecerán las bases conceptuales para el desarrollo backend eficiente.
*   **Recursos Web:**
    *   [Programación Imperativa vs Declarativa](https://dev.to/siddharthshyniben/explained-imperative-vs-declarative-programming-577g) (1h)
*   **Videos:** [Programación Imperativa vs Declarativa](https://www.youtube.com/watch?v=E7Fbf7R3x6I)

### Módulo 4: Conceptos Básicos de React (Path 4)
*   **Objetivo:** Comprender los conceptos fundamentales de React para construir interfaces de usuario.
*   **Descripción:** Introducción a React, componentes funcionales, JSX y los conceptos básicos del renderizado. Se establecerán los fundamentos para construir interfaces de usuario modernas y responsivas.
*   **Recursos Web:**
    *   [Introducción a React (React.dev)](https://react.dev/learn) (2h)
*   **Videos:** [Introducción a React (componentes, props, estado, fetching)](https://www.youtube.com/watch?v=LDB4uaJ87e0) (1h)

### Módulo 5: Introducción a MongoDB y Modelo de Documentos (Path 5)
*   **Objetivo:** Establecer una base sólida en el ecosistema de MongoDB y su arquitectura.
*   **Descripción:** Introducción a MongoDB, su arquitectura y el modelo de documentos. Se explorarán los conceptos fundamentales de las bases de datos NoSQL y las ventajas del modelo de documentos para el desarrollo de aplicaciones modernas.
*   **Recursos Web:**
    *   [Intro to MongoDB](https://learn.mongodb.com/courses/start-here-introduction-to-mongodb) (1.25h)
    *   [MongoDB and the Document Model](https://learn.mongodb.com/courses/overview-of-mongodb-and-the-document-model) (1.25h)
*   **Videos:** Material de MongoDB University

### Módulo 6: Configuración del Entorno CLI y Herramientas Básicas (Path 6)
*   **Objetivo:** Configurar el entorno de desarrollo con las herramientas fundamentales.
*   **Descripción:** Instalación y configuración inicial de herramientas esenciales: Git, nvm y Node.js. Se establecerán las bases para un entorno de desarrollo eficiente con todos los prerrequisitos necesarios.
*   **Recursos Web:**
    *   **Git:**
        * [Instalación de Git (Español)](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)
        * [Installing Git (Inglés)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
    *   **nvm:** 
        * [nvm-sh/nvm – GitHub](https://github.com/nvm-sh/nvm#installing-and-updating)
    *   **Node.js:**
        * [Node.js en Español](https://nodejs.org/es)
        * [Node.js Official](https://nodejs.org/en)
*   **Videos:** [Configuración básica del entorno de desarrollo](https://www.youtube.com/watch?v=c2-032jBDL4)

---

## Día 2: Profundización en Conceptos Core

### Módulo 1: Contextos Delimitados (Path 1)
*   **Objetivo:** Dominar los conceptos del diseño estratégico como los Contextos Delimitados y la organización de equipos.
*   **Descripción:** Profundización en los Contextos Delimitados como herramienta fundamental para definir los límites de los microservicios y organizar equipos de desarrollo.
*   **Recursos Web:**
    *   **Bounded Contexts - Conceptos Fundamentales:**
        * [Bounded Context - Martin Fowler](https://martinfowler.com/bliki/BoundedContext.html) (1h)
*   **Videos:** 
    *   [DDD and Microservices: At Last, Some Boundaries! - Eric Evans](https://www.youtube.com/watch?v=yPvef9R3k-M) (50min)

### Módulo 2: Estructura de Microservicio NebulaE (Path 2)
*   **Objetivo:** Comprender la estructura de carpetas fundamental de un microservicio NebulaE.
*   **Descripción:** Análisis detallado de la estructura generada, entendiendo el propósito de las carpetas `frontend`, `api`, `backend`, `deployment` y `playground`. Se explorarán las convenciones y patrones utilizados.
*   **Recursos Web:** Documentación interna de estructura de proyectos
*   **Videos:** "Estructura y Arquitectura de un Microservicio NebulaE" (1h)

### Módulo 3: Asincronismo en JavaScript (Path 3)
*   **Objetivo:** Dominar los patrones de asincronismo de NodeJS.
*   **Descripción:** Estudio profundo de Callbacks, Promises y Async/Await como fundamentos del desarrollo asíncrono en NodeJS. Se practicarán ejemplos reales de cada patrón.
*   **Recursos Web:**
    *   [Guía de asincronismo en JS: Callbacks, Promises, Async/Await (MDN)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous) (2h)
*   **Videos:** 
    *   [Asincronismo en JavaScript](https://www.youtube.com/watch?v=PoRJizFvM7s)
    *   [Promises y Async/Await](https://www.youtube.com/watch?v=V_Kr9OSfDeU)

### Módulo 4: Hooks de React (Path 4)
*   **Objetivo:** Utilizar los hooks esenciales para manejar el estado y los efectos secundarios.
*   **Descripción:** Implementación práctica de useState y useEffect para manejar estado local y efectos secundarios en componentes funcionales. Se crearán ejemplos prácticos de uso.
*   **Recursos Web:**
    *   [Hooks: useState y useEffect (React.dev)](https://react.dev/reference/react/useState) (1.5h)
*   **Videos:** 
    *   [Introducción a Hooks – useState y useEffect](https://www.youtube.com/watch?v=P5p3vMeJ6LQ) (0.5h)
    *   [useState en 15 minutos](https://www.youtube.com/watch?v=O6P86uwfdR0) (0.25h)

### Módulo 5: MongoDB Atlas - Configuración y Primeros Pasos (Path 5)
*   **Objetivo:** Configurar MongoDB Atlas y realizar las primeras conexiones.
*   **Descripción:** Configuración de una instancia de MongoDB Atlas, comprensión de la interfaz y realización de las primeras operaciones básicas. Se establecerán las conexiones fundamentales para el desarrollo.
*   **Recursos Web:**
    *   [Getting Started with MongoDB Atlas](https://learn.mongodb.com/courses/getting-started-with-mongodb-atlas) (1.25h)
*   **Videos:** Tutorial de configuración de MongoDB Atlas

### Módulo 6: Comandos Esenciales de Terminal y Navegación (Path 6)
*   **Objetivo:** Dominar los comandos esenciales de la terminal para navegación y manipulación básica de archivos.
*   **Descripción:** Práctica con comandos fundamentales de navegación y gestión de archivos: `ls`, `cd`, `pwd`, `mkdir`, `rm`, `cp`, `mv`, `chmod`. Se establecerán las bases para el trabajo eficiente en línea de comandos.
*   **Recursos Web:**
    *   **Comandos Bash:**
        * [Comandos Bash – Wikipedia (Español)](https://es.wikipedia.org/wiki/Comandos_Bash)
        * [GNU Coreutils – ls, cd, etc. (Inglés)](https://www.gnu.org/software/coreutils/)
*   **Videos:** 
    *   [Comandos LINUX Básicos Desde Cero – DeciLearn (Español)](https://www.youtube.com/watch?v=_KCc-tvpPRM) (2022)
    *   [Linux Command Line for Beginners – freeCodeCamp (Inglés)](https://www.youtube.com/watch?v=sWbUDq4S6Y8) (2021)

---

## Día 3: Tecnologías de Datos y Herramientas

### Módulo 1: Instalación del Entorno y Generación de Primer Microservicio (Path 2)
*   **Objetivo:** Instalar el entorno de desarrollo de NebulaE y generar el primer microservicio desde cero.
*   **Descripción:** Configuración del CLI de NebulaE e instalación de herramientas necesarias. Generación de un microservicio completo para comprender la estructura fundamental de carpetas y archivos que siguen las convenciones de NebulaE. Aplicación práctica de todos los conceptos estudiados en los días anteriores.
*   **Recursos Web:**
    *   Instalación del CLI de NebulaE
    *   Comandos de generación de microservicios

### Módulo 2: Programación Declarativa vs Imperativa (Path 3)
*   **Objetivo:** Dominar el estilo de programación declarativa utilizado en NebulaE.
*   **Descripción:** Práctica intensiva con métodos de Array y programación funcional. Se enfocará en la diferencia entre programación imperativa y declarativa con ejemplos prácticos.
*   **Recursos Web:**
    *   [Práctica Declarativa: Métodos de Array (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) (1.5h)
*   **Videos:** [Métodos de Array en JavaScript](https://www.youtube.com/watch?v=8MoElay6dWU)

### Módulo 3: Introducción a Redux - Conceptos Fundamentales (Path 4)
*   **Objetivo:** Comprender los conceptos fundamentales de Redux para gestión de estado global.
*   **Descripción:** Introducción a los principios de Redux: Store, Actions, Reducers. Se establecerán las bases para la gestión de estado complejo en aplicaciones React.
*   **Recursos Web:**
    *   [Redux: Conceptos Fundamentales (Redux.js.org)](https://redux.js.org/introduction/getting-started) (1.5h)
*   **Videos:** Tutoriales de Redux básico
    * [Redux Tutorial](https://www.youtube.com/watch?v=poQXNp9ItL4) (1.75h)

### Módulo 4: Conexión a MongoDB usando MongoDB Shell (Path 5)
*   **Objetivo:** Aprender a interactuar con MongoDB usando la shell nativa.
*   **Descripción:** Práctica con MongoDB Shell para realizar operaciones básicas de conexión y consulta. Se establecerán las bases para la interacción directa con la base de datos.
*   **Recursos Web:**
    *   [Connecting to a MongoDB Database Using the MongoDB Shell](https://learn.mongodb.com/courses/connecting-to-a-mongodb-database-using-the-mongodb-shell) (1.75h)
*   **Videos:** Material práctico de MongoDB Shell

### Módulo 5: Manipulación y Búsqueda de Texto con grep y find (Path 6)
*   **Objetivo:** Dominar herramientas avanzadas de búsqueda y manipulación de texto en terminal.
*   **Descripción:** Uso de comandos de manipulación y búsqueda de texto: `cat`, `less`, `head`, `tail`, `grep`, `find`. Se practicarán técnicas de búsqueda eficiente y manipulación de archivos de texto.
*   **Recursos Web:**
    *   **Comandos de texto:**
        * [Comandos Bash – Wikipedia (Español)](https://es.wikipedia.org/wiki/Comandos_Bash)
        * [grep – man7.org (Inglés)](https://man7.org/linux/man-pages/man1/grep.1.html)
*   **Videos:** 
    *   [Comando find](https://www.youtube.com/watch?v=Au9OM5-RgIM) 
    *   [Comando GREP](https://www.youtube.com/watch?v=MfDVUemyQOo) 
    *   [Linux Text Search – grep & find (Inglés)](https://www.youtube.com/watch?v=VGgTmxXp7xQ) (2022)

---

## Día 4: Integración y Conexiones

### Módulo 1: Métodos Funcionales en JavaScript (Path 3)
*   **Objetivo:** Profundizar en programación funcional y métodos de Array.
*   **Descripción:** Práctica avanzada con métodos funcionales de Array como map, filter, reduce. Se crearán ejemplos complejos que demuestren el poder de la programación declarativa.
*   **Recursos Web:**
    *   **Métodos de Array (MDN):**
        * [Array.prototype.map() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) (1h)
        * [Array.prototype.filter() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) (1h)
        * [Array.prototype.reduce() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce) (1.5h)
    *   **Programación Funcional:**
        * [Functional Programming in JavaScript - freeCodeCamp](https://www.freecodecamp.org/news/functional-programming-in-javascript/) (2h)
        * [JavaScript Functional Programming Explained - GeeksforGeeks](https://www.geeksforgeeks.org/functional-programming-paradigm/) (1h)
*   **Videos:** 
    *   [Métodos de Array en JavaScript: map, filter, reduce](https://www.youtube.com/watch?v=8MoElay6dWU) (Español)
    *   [Programación Funcional en JavaScript](https://www.youtube.com/watch?v=e-5obm1G_FY) (Español)
    *   [Functional JavaScript: Array Methods](https://www.youtube.com/watch?v=rRgD1yVwIvE) (Inglés)

### Módulo 2: React Redux Integración (Path 4)
*   **Objetivo:** Integrar Redux con React usando las herramientas modernas.
*   **Descripción:** Implementación práctica de React Redux usando `Provider`, `useSelector` y `useDispatch`. Se creará una aplicación ejemplo que demuestre el flujo completo de datos.
*   **Recursos Web:**
    *   [React Redux: Conectando Redux con React (React-Redux.js.org)](https://react-redux.js.org/introduction/getting-started) (1h)
*   **Videos:** [Crash Course React completo](https://www.youtube.com/watch?v=CgkZ7MvWUAA) (2h)

### Módulo 3: Conexión MongoDB desde Node.js (Path 5)
*   **Objetivo:** Aprender a interactuar con MongoDB desde aplicaciones Node.js.
*   **Descripción:** Implementación de conexiones desde Node.js a MongoDB. Se realizarán operaciones básicas de conexión y se establecerán las bases para operaciones CRUD.
*   **Recursos Web:**
    *   [Connecting to a MongoDB Database Using the MongoDB Shell](https://learn.mongodb.com/courses/connecting-to-a-mongodb-database-using-the-mongodb-shell) (1.75h)
    *   [Connecting to MongoDB in Node.js](https://learn.mongodb.com/courses/connecting-to-mongodb-in-nodejs) (1h)
*   **Videos:** Material práctico de conexión con MongoDB

### Módulo 4: Encadenamiento de Comandos y Redirección (Path 6)
*   **Objetivo:** Dominar técnicas avanzadas de encadenamiento de comandos y redirección en terminal.
*   **Descripción:** Uso avanzado de pipes (`|`), redirección (`>`, `>>`), y operadores de control (`;`, `&&`). Se practicarán técnicas de encadenamiento eficiente para automatizar tareas complejas.
*   **Recursos Web:**
    *   **Pipes y Redirección:**
        * [Guía de Redirección y Pipes en Linux – Tecmint (Español)](https://www.tecmint.com/use-linux-pipes-to-connect-commands/)
        * [Bash Reference Manual – Pipelines (Inglés)](https://www.gnu.org/software/bash/manual/html_node/Pipelines.html)
*   **Videos:** 
    *   [Pipes y Redirecciones en Linux (Español)](https://www.youtube.com/watch?v=Hsno6279tik) 
    *   [Linux Pipes and Redirection (Inglés)](https://www.youtube.com/watch?v=mV_8GbzwZMM) (2022)

---

## Día 5: Consolidación y Práctica Integral

### Módulo 1: Conceptos Avanzados de JavaScript (Path 3)
*   **Objetivo:** Consolidar conocimientos de JavaScript con conceptos de igualdad y valores falsy.
*   **Descripción:** Estudio de igualdad y valores falsy en JavaScript como fundamento para evitar errores comunes en el desarrollo. Se practicarán casos edge que son frecuentes en desarrollo real.
*   **Recursos Web:**
    *   [Igualdad y Falsy Values en JS (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness) (0.5h)
*   **Videos:** 
    *   [Igualdad en JavaScript](https://www.youtube.com/watch?v=jD2BuBfxRn8)
    *   [Falsy Values](https://www.youtube.com/watch?v=5DVqAFhfSsE)

### Módulo 2: Práctica Integral React (Path 4)
*   **Objetivo:** Crear un componente React completo que integre todos los conceptos aprendidos.
*   **Descripción:** Desarrollo de un componente funcional completo que utilice hooks, gestión de estado local, efectos secundarios y conexión con Redux. Se implementará un ejemplo práctico del mundo real.
*   **Recursos Web:** Integración de todos los recursos de React de la semana
*   **Videos:** Proyecto práctico guiado

### Módulo 3: Práctica Integral MongoDB (Path 5)
*   **Objetivo:** Realizar operaciones completas con MongoDB desde diferentes interfaces.
*   **Descripción:** Práctica integral que incluye operaciones desde MongoDB Shell y desde Node.js. Se implementarán operaciones de lectura y escritura básicas que servirán como base para semanas posteriores.
*   **Recursos Web:** Integración de todos los recursos de MongoDB de la semana
*   **Videos:** Sesión práctica con MongoDB

### Módulo 4: Configuración Completa del Entorno (Path 6)
*   **Objetivo:** Completar la configuración del entorno de desarrollo con todas las herramientas necesarias.
*   **Descripción:** Instalación y configuración completa de Git, nvm, Node.js y paquetes globales necesarios. Se verificará que el entorno esté completamente listo para el desarrollo en NebulaE, incluyendo automatización básica con Bash.
*   **Recursos Web:**
    *   **Instalación de herramientas:**
        * [Instalación de Git (Español)](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)
        * [nvm-sh/nvm – GitHub](https://github.com/nvm-sh/nvm#installing-and-updating)
    *   **Automatización:**
        * [Programación de Bash (Español)](https://www.freecodecamp.org/espanol/news/tutorial-de-programacion-de-bash-script-de-shell-de-linux-y-linea-de-comandos-para-principiantes/)
*   **Videos:** [Bash Scripting Crash Course (Inglés)](https://www.youtube.com/watch?v=tK9Oc6AEnR4) (2022)

### Módulo 5: Integración de Conocimientos
*   **Objetivo:** Conectar todos los conceptos aprendidos durante la semana.
*   **Descripción:** Sesión de integración donde se conectan los conceptos de DDD, la estructura de NebulaE, los fundamentos de Node.js, React, MongoDB y herramientas CLI. Se prepara el terreno para la Semana 2.
*   **Recursos Web:** Síntesis de todos los materiales de la semana
*   **Videos:** Sesión de síntesis y preparación para Semana 2

---

## Evaluación de la Semana 1

### Prueba Práctica: "Configuración y Fundamentos Técnicos"

**Descripción del Proyecto:**
Implementar un proyecto que demuestre el dominio de todos los fundamentos técnicos aprendidos durante la semana, integrando conceptos de cada path.

**Requisitos Técnicos:**

1.  **Arquitectura (Path 1):** 
    *   Definir un dominio simple (ej: gestión de libros) usando Lenguaje Ubicuo
    *   Identificar un Contexto Delimitado claro
    *   Documentar las decisiones de diseño

2.  **Framework NebulaE (Path 2):** 
    *   Instalar correctamente el CLI de NebulaE
    *   Generar la estructura básica de un microservicio
    *   Documentar la estructura de carpetas y su propósito

3.  **Backend (Path 3):** 
    *   Crear funciones que demuestren programación declarativa vs imperativa
    *   Implementar ejemplos de asincronismo con Promises y Async/Await
    *   Resolver ejercicios de métodos de Array (map, filter, reduce)

4.  **Frontend (Path 4):** 
    *   Crear un componente React funcional con useState y useEffect
    *   Implementar un ejemplo básico de Redux con store, actions y reducers
    *   Demostrar comprensión de JSX y renderizado condicional

5.  **Persistencia (Path 5):**
    *   Configurar una instancia de MongoDB Atlas
    *   Realizar conexión exitosa desde MongoDB Shell
    *   Implementar conexión básica desde Node.js

6.  **DevOps/Herramientas (Path 6):**
    *   Demostrar dominio de comandos básicos de terminal
    *   Configurar correctamente nvm con múltiples versiones de Node
    *   Instalar y configurar todas las herramientas de desarrollo

**Criterios de Evaluación:**

*   **Comprensión Conceptual (30%):** Dominio de conceptos fundamentales de cada path
*   **Implementación Técnica (40%):** Correcta implementación de ejercicios prácticos
*   **Configuración de Entorno (20%):** Entorno completamente funcional y documentado
*   **Documentación (10%):** Capacidad de explicar decisiones y conceptos aprendidos

### Prueba Teórica: Fundamentos Multi-Path

**Sección 1: Domain-Driven Design (20%)**
*   Definir Lenguaje Ubicuo y proporcionar un ejemplo práctico
*   Explicar qué es un Contexto Delimitado y su importancia
*   Describir cómo DDD influye en el diseño de microservicios

**Sección 2: NodeJS y Programación (25%)**
*   Comparar programación imperativa vs declarativa con ejemplos
*   Explicar la diferencia entre Callbacks, Promises y Async/Await
*   Resolver problemas prácticos con métodos de Array

**Sección 3: React Fundamentals (25%)**
*   Explicar el concepto de componente funcional vs clase
*   Describir el propósito de useState y useEffect con ejemplos
*   Explicar los conceptos básicos de Redux (Store, Actions, Reducers)

**Sección 4: MongoDB y Herramientas (30%)**
*   Describir las ventajas del modelo de documentos vs relacional
*   Explicar cómo conectar MongoDB desde Node.js
*   Demostrar conocimiento de comandos básicos de terminal

**Modo de Entrega:**
*   **Proyecto Práctico:** Repositorio GitHub con implementaciones de cada path
*   **Prueba Teórica:** Cuestionario en Google Classroom con casos prácticos
*   **Configuración de Entorno:** Video demostrando el entorno funcionando
*   **Fecha Límite:** Final del viernes de la Semana 1
*   **Sesión de Feedback:** Lunes de la Semana 2 durante la sesión de Q&A

**Preparación para Semana 2:**
*   **Path 1:** Patrones tácticos de DDD (Entidades, Agregados)
*   **Path 2:** Implementación de lógica de negocio con NebulaE
*   **Path 3:** Fundamentos de RxJS y Observables
*   **Path 4:** Estilizado con Material UI y formularios con Formik
*   **Path 5:** Operaciones CRUD en MongoDB
*   **Path 6:** Docker y Docker Compose
