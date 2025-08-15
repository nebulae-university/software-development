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
    *   **lunes:** 3:00 PM - 4:00 PM
    *   **miercoles:** 9:00 AM - 10:00 AM y 3:00 PM - 4:00 PM
    *   **viernes:** 3:00 PM - 4:00 PM
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

### Introducción del Día

¡Bienvenido al primer día! Hoy sentaremos las bases de todo el programa. El objetivo es que te sumerjas en los conceptos fundamentales que definen nuestra arquitectura y configures tu entorno de desarrollo para estar listo para la acción. Se espera que al final del día tengas una comprensión clara de la filosofía de Domain-Driven Design (DDD), la estructura de nuestro framework NebulaE, y los pilares de tecnologías como NodeJS, React y MongoDB.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Fundamentos de Domain-Driven Design (Path 1)
*   **Módulo 2:** Lectura y Entendimiento del Framework NebulaE (Path 2)
*   **Módulo 3:** Fundamentos de NodeJS (Path 3)
*   **Módulo 4:** Conceptos Básicos de React (Path 4)
*   **Módulo 5:** Introducción a MongoDB y Modelo de Documentos (Path 5)
*   **Módulo 6:** Configuración del Entorno CLI y Herramientas Básicas (Path 6)

### Módulo 1: Fundamentos de Domain-Driven Design (Path 1)
*   **Objetivo:** Comprender la filosofía de DDD, su importancia para el negocio y los conceptos del diseño estratégico.
*   **Descripción:** Este módulo introduce los fundamentos de Domain-Driven Design (DDD), una metodología crucial para construir software que está verdaderamente alineado con las metas del negocio. El objetivo es que dejes de pensar solo en tecnología y comiences a modelar el dominio del negocio.

    Para ello, empezarás leyendo el material de **Microsoft Docs sobre análisis de dominio**, que te enseñará a descomponer un sistema complejo en partes más manejables, identificando los "subdominios" del negocio. Este es el primer paso para definir microservicios. El concepto clave aquí es el **Bounded Context (Contexto Delimitado)**, que es la frontera que define dónde un modelo de software específico tiene sentido.

    Luego, el artículo de **microservices.io sobre "Servicio por Equipo"** te mostrará cómo la estructura de tus equipos de desarrollo (la Ley de Conway) impacta directamente la arquitectura de tu software. Aprenderás por qué es vital que equipos pequeños y autónomos sean dueños de servicios específicos para fomentar la agilidad y la responsabilidad.

    Los videos complementan esta base teórica. El video de **Nick Tune sobre Bounded Contexts** te dará una visión práctica de cómo "descubrir" estos límites en un negocio real. Los videos sobre **arquitecturas Limpia, Hexagonal y de Cebolla** te introducirán a patrones que promueven el desacoplamiento y la testeabilidad, principios clave en DDD. Finalmente, los videos cortos sobre **Microservicios vs. Monolitos**, la **Ley de Conway** y los **Límites y Encapsulamiento** reforzarán de manera visual y concisa por qué estamos adoptando esta filosofía en NebulaE.

    Al final de este módulo, deberás ser capaz de explicar qué es el **Lenguaje Ubicuo** (un lenguaje compartido entre desarrolladores y expertos del dominio) y cómo los **Contextos Delimitados** ayudan a organizar tanto el código como los equipos.
*   **Recursos Web:**
    *   [Análisis de dominio en una arquitectura de microservicios (Microsoft Docs)](https://learn.microsoft.com/es-es/azure/architecture/microservices/model/domain-analysis) (1.5h)
    *   [Patrón: Servicio por Equipo (microservices.io)](https://microservices.io/patterns/decomposition/service-per-team.html) (1h)
*   **Videos:**
    *   [The Art of Discovering Bounded Contexts (Nick Tune)](https://www.youtube.com/watch?v=ez9GWESKG4I) (1h)
    *   [Video: Hexagonal, Onion & Clean Architecture](https://www.youtube.com/watch?v=JubdZIdLQ4M) (15min) - Conceptos base de arquitecturas limpias.
    *   [Video: Microservices vs Monolithic Architecture](https://www.youtube.com/watch?v=6-Wu178sOEE) (10min) - Comparativa fundamental de estilos arquitectónicos.
    *   [Video: DDD Bounded Contexts & Subdomains](https://www.youtube.com/watch?v=NvBsEnDgA4o) (12min) - Visualización de los conceptos clave de DDD.
    *   [Video: Conway’s Law](https://www.youtube.com/watch?v=TqhkWaeUN_8) (8min) - Entendiendo cómo la estructura del equipo moldea la arquitectura.
    *   [Video: Boundaries & Encapsulation](https://www.youtube.com/watch?v=EBO0ysJr2BA) (10min) - Principios para el diseño de componentes y servicios.

### Módulo 2: Lectura y Entendimiento del Framework NebulaE (Path 2)
*   **Objetivo:** Comprender la arquitectura y filosofía del framework NebulaE mediante lectura de documentación.
*   **Descripción:** En este módulo, te sumergirás en el corazón de nuestro ecosistema: el framework NebulaE. El objetivo es que entiendas *por qué* construimos las cosas de la manera en que lo hacemos.

    Tu primera tarea es explorar la documentación en **npm** de las herramientas clave. Comienza con **`@nebulae/cli`**. No te enfoques en memorizar comandos, sino en entender su propósito: es la herramienta que te permitirá crear, registrar y componer microservicios de manera estandarizada. Presta especial atención a la sección de **"Architecture Overview"**, ya que es un resumen visual y conceptual de los patrones que usamos: **CQRS** (separar la escritura de la lectura de datos) y **Event Sourcing** (almacenar el estado como una secuencia de eventos).

    Luego, revisa **`@nebulae/event-store`**. Este paquete es la implementación técnica del Event Sourcing. Aquí, el concepto clave es el **"Evento de Dominio"** (ej: `USUARIO_CREADO`), que se convierte en la única fuente de verdad. Entenderás cómo usamos **RxJS** para manejar flujos de eventos de manera reactiva y cómo los microservicios se comunican de forma asíncrona a través de un **Message Broker** (como MQTT o Pub/Sub).

    Finalmente, explora **`@nebulae/backend-node-tools`**. Este es tu kit de herramientas para el día a día. Fíjate en cómo resolvemos problemas comunes: **manejo de errores estructurado** (con `CustomError`), **logging estandarizado**, y **autenticación y autorización**. Conceptos como la **abstracción del broker** (`brokerFactory`) te mostrarán cómo aplicamos patrones de diseño para hacer nuestro código más flexible.

    Los videos de **Introducción al Framework** y la **Vista General de Arquitectura** te darán un recorrido guiado por estos conceptos, conectando la teoría de DDD que viste en el módulo anterior con la implementación práctica en NebulaE. Al final, deberías poder dibujar un diagrama simple de cómo un comando fluye a través del sistema, genera un evento y actualiza una vista de lectura.
*   **Recursos Web:**
    *   [npm: @nebulae/cli](https://www.npmjs.com/package/@nebulae/cli)
    *   [Architecture Overview](https://www.npmjs.com/package/@nebulae/cli#architecture-overview)
    *   [npm: @nebulae/event-store](https://www.npmjs.com/package/@nebulae/event-store)
    *   [npm: @nebulae/backend-node-tools](https://www.npmjs.com/package/@nebulae/backend-node-tools)
*   **Videos:** [Vista General de Arquitectura](https://www.youtube.com/watch?v=CxbGZhWJDkM) (1h)

### Módulo 3: Fundamentos de NodeJS (Path 3)
*   **Objetivo:** Establecer una base sólida en los paradigmas de programación que guían el estilo de código en NebulaE.
*   **Descripción:** Este módulo establece las bases del estilo de programación que favorecemos en NebulaE para el backend con NodeJS. El objetivo no es solo aprender la sintaxis de JavaScript, sino adoptar un paradigma de programación específico que hace el código más legible, mantenible y menos propenso a errores.

    El recurso principal, tanto el artículo de **DEV.to** como el video, se centra en una dicotomía fundamental: **Programación Imperativa vs. Declarativa**.

    *   **Programación Imperativa:** Es la que probablemente ya conoces. Se enfoca en el **"cómo"**: le das a la computadora una secuencia de pasos explícitos para llegar al resultado. Piensa en un bucle `for` donde manualmente iteras, verificas una condición y modificas una variable.

    *   **Programación Declarativa:** Se enfoca en el **"qué"**: describes el resultado que deseas, y el lenguaje o framework se encarga de los pasos. En lugar de un bucle `for`, usarías métodos de array como `.filter()` o `.map()`. Le dices "quiero una lista con solo los números pares", no "itera sobre esta lista, revisa si cada número es par, y si lo es, agrégalo a una nueva lista".

    Tu tarea es internalizar esta diferencia. Lee el artículo para obtener la base conceptual y luego mira el video para reforzarlo con ejemplos visuales. Intenta reescribir un bucle `for` simple usando un enfoque declarativo. El concepto clave a extraer es que el código declarativo es más expresivo y se alinea mejor con el pensamiento funcional, que es un pilar en nuestro trabajo con flujos de datos y eventos. Al final de este módulo, deberías poder identificar si un bloque de código es imperativo o declarativo y explicar por qué uno es preferible sobre el otro en el contexto de NebulaE.
*   **Recursos Web:**
    *   [Programación Imperativa vs Declarativa](https://dev.to/siddharthshyniben/explained-imperative-vs-declarative-programming-577g) (1h)
*   **Videos:** [Programación Imperativa vs Declarativa](https://www.youtube.com/watch?v=E7Fbf7R3x6I)

### Módulo 4: Conceptos Básicos de React (Path 4)
*   **Objetivo:** Comprender los conceptos fundamentales de React para construir interfaces de usuario.
*   **Descripción:** Este módulo es tu punto de partida en el mundo del frontend moderno con React. El objetivo es que comprendas cómo React nos permite construir interfaces de usuario complejas a partir de piezas pequeñas, reutilizables y aisladas.

    La documentación oficial de **React.dev ("Introducción a React")** es tu recurso principal y debes seguirla de manera secuencial. Los conceptos clave que debes dominar son:

    1.  **Componentes:** Son los bloques de construcción de tu UI. Entiende la idea de que una interfaz es un árbol de componentes (ej: un componente `Button` dentro de un componente `LoginForm` dentro de una página `LoginPage`). Enfócate en los **componentes funcionales**, que es el estándar moderno.
    2.  **JSX:** Es una extensión de sintaxis para JavaScript que te permite escribir "HTML" dentro de tu código JS. La clave es entender que no es HTML real, sino una forma declarativa de describir la estructura de tu UI. Aprende a usar llaves `{}` para insertar lógica y variables de JavaScript directamente en tu marcado.
    3.  **Props (Propiedades):** Son la forma de pasar datos desde un componente padre a un componente hijo. Piensa en ellas como los argumentos de una función. Son inmutables (solo de lectura) para el componente que las recibe.
    4.  **Estado (State):** Este es uno de los conceptos más importantes. El estado es la memoria interna de un componente. A través del hook `useState`, un componente puede "recordar" información (como el valor de un input o si un menú está abierto) y React volverá a renderizar el componente automáticamente cuando ese estado cambie.
    5.  **Renderizado Condicional y Listas:** Aprende a usar operadores de JavaScript (como el ternario `? :` o el `&&`) para mostrar u ocultar componentes, y el método `.map()` para renderizar listas de datos de forma dinámica.

    El **video de introducción a React** te servirá como un excelente complemento visual, guiándote a través de la creación de un componente desde cero y mostrando cómo se conectan los conceptos de componentes, props, estado y fetching de datos. Al final de este módulo, deberías ser capaz de crear un componente simple que reciba datos a través de props y maneje su propio estado interno con `useState`.
*   **Recursos Web:**
    *   [Introducción a React (React.dev)](https://react.dev/learn) (2h)
*   **Videos:** [Introducción a React (componentes, props, estado, fetching)](https://www.youtube.com/watch?v=LDB4uaJ87e0) (1h)

### Módulo 5: Introducción a MongoDB y Modelo de Documentos (Path 5)
*   **Objetivo:** Establecer una base sólida en el ecosistema de MongoDB y su arquitectura.
*   **Descripción:** Este módulo te introduce al mundo de las bases de datos NoSQL a través de MongoDB, la tecnología de persistencia que utilizamos en NebulaE. El objetivo es que comprendas por qué elegimos un modelo de documentos flexible en lugar de las tradicionales bases de datos relacionales (SQL).

    Los dos cursos de **MongoDB University** son tu hoja de ruta. Comienza con **"Intro to MongoDB"**. Aquí, el concepto fundamental es entender qué es una **base de datos orientada a documentos**. En lugar de filas y tablas, pensarás en **documentos** (similares a objetos JSON) agrupados en **colecciones**. Presta atención a la introducción de **MongoDB Atlas**, que es la plataforma en la nube que usaremos para desplegar y gestionar nuestras bases de datos, abstrayéndonos de la complejidad de la infraestructura.

    El segundo curso, **"MongoDB and the Document Model"**, es donde profundizarás en el "cómo". La lección más importante aquí es el **modelado de datos**. A diferencia de SQL, donde normalizas y unes tablas, en MongoDB tienes dos estrategias principales:

    1.  **Embedding (Incrustar):** Guardar datos relacionados directamente dentro de un único documento. Es ideal para relaciones "uno-a-pocos" donde los datos se leen juntos (ej: los comentarios de un post).
    2.  **Referencing (Referenciar):** Guardar el ID de un documento en otro, de forma similar a una clave foránea. Se usa para relaciones "uno-a-muchos" o "muchos-a-muchos" para evitar la duplicación de datos.

    Tu objetivo es entender las ventajas y desventajas de cada enfoque. No hay una única respuesta correcta; la decisión depende del caso de uso y de los patrones de acceso a los datos. Los videos del material de MongoDB University te guiarán con ejemplos prácticos. Al final de este módulo, deberías poder explicar la diferencia entre un modelo relacional y un modelo de documentos, y cuándo usarías embedding vs. referencing.
*   **Recursos Web:**
    *   [Intro to MongoDB](https://learn.mongodb.com/courses/start-here-introduction-to-mongodb) (1.25h)
    *   [MongoDB and the Document Model](https://learn.mongodb.com/courses/overview-of-mongodb-and-the-document-model) (1.25h)
*   **Videos:** Material de MongoDB University

### Módulo 6: Configuración del Entorno CLI y Herramientas Básicas (Path 6)
*   **Objetivo:** Configurar el entorno de desarrollo con las herramientas fundamentales.
*   **Descripción:** Este módulo es puramente práctico y fundamental para que puedas empezar a trabajar. El objetivo es que dejes tu máquina local perfectamente configurada con las herramientas básicas que todo desarrollador en NebulaE necesita.

    Sigue los recursos en el orden sugerido. La meta no es solo instalar, sino entender *qué* estás instalando y *por qué*.

    1.  **Git:** Es el sistema de control de versiones que usamos para todo. Sigue la guía de **instalación de Git** para tu sistema operativo. No te detengas en la instalación; asegúrate de configurar tu nombre de usuario y correo electrónico (`git config --global user.name "Tu Nombre"` y `git config --global user.email "tu.email@example.com"`). Git es la base para colaborar y gestionar el historial de nuestro código.

    2.  **nvm (Node Version Manager):** Esta es una herramienta crucial. En lugar de instalar Node.js directamente, instalarás **nvm**. ¿Por qué? Porque nvm te permite instalar y cambiar entre **múltiples versiones de Node.js** fácilmente. Diferentes proyectos pueden requerir diferentes versiones de Node.js, y nvm evita conflictos y te da control total sobre tu entorno. Sigue las instrucciones en el repositorio de GitHub para instalarlo. Una vez instalado, úsalo para instalar la versión LTS (Long-Term Support) más reciente de Node.js con el comando `nvm install --lts`.

    3.  **Node.js:** Aunque nvm lo instala, es importante que visites la página oficial de **Node.js** para entender qué es: un entorno de ejecución de JavaScript del lado del servidor. Es la base sobre la que construiremos todo nuestro backend.

    En el **video de configuración del entorno**, aprenderás a ensamblar un entorno de desarrollo robusto y versátil. La guía visual te llevará a través de la instalación de `git` para el control de versiones y `nvm` (Node Version Manager) para gestionar múltiples versiones de Node.js. Siguiendo el video, usarás `nvm` para instalar varias versiones clave de Node.js: 10, 12, 14, 18 y 22. El video también cubre la instalación de paquetes `npm` globales esenciales: para la versión 10 de Node, instalarás `@nebulae/cli` y `nodemon`; para la versión 12, instalarás los mismos paquetes y además `yarn`. Al completar estos pasos, tendrás un entorno de desarrollo profesional, capaz de manejar los requisitos de diversos proyectos de NebulaE y listo para los siguientes módulos.
*   **Recursos Web:**
    *   **Git:**
        * [Instalación de Git (Español)](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)
        * [Installing Git (Inglés)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
    *   **nvm:** 
        * [nvm-sh/nvm – GitHub](https://github.com/nvm-sh/nvm#installing-and-updating)
    *   **Node.js:**
        * [Node.js en Español](https://nodejs.org/es)
        * [Node.js Official](https://nodejs.org/en)
*   **Videos:** [Configuración básica del entorno de desarrollo](https://youtu.be/RzYQwp_6UKs)

---

## Día 2: Profundización en Conceptos Core

### Introducción del Día

En nuestro segundo día, profundizaremos en los conceptos clave presentados ayer. El objetivo es pasar de la teoría a un entendimiento más práctico y aplicado. Hoy dominarás el concepto de Contextos Delimitados en DDD, diseccionarás la estructura de un microservicio NebulaE, y te enfrentarás al asincronismo en JavaScript. Además, darás tus primeros pasos prácticos con React Hooks y configurarás tu primer clúster de base de datos en la nube con MongoDB Atlas. Se espera que hoy consolides tu base teórica y la conectes con las herramientas que usarás a diario.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Contextos Delimitados (Path 1)
*   **Módulo 2:** Estructura de Microservicio NebulaE (Path 2)
*   **Módulo 3:** Asincronismo en JavaScript (Path 3)
*   **Módulo 4:** Hooks de React (Path 4)
*   **Módulo 5:** MongoDB Atlas - Configuración y Primeros Pasos (Path 5)
*   **Módulo 6:** Comandos Esenciales de Terminal y Navegación (Path 6)

### Módulo 1: Contextos Delimitados (Path 1)
*   **Objetivo:** Dominar los conceptos del diseño estratégico como los Contextos Delimitados y la organización de equipos.
*   **Descripción:** Este módulo profundiza en el concepto más importante del diseño estratégico de DDD: el Contexto Delimitado (Bounded Context). El objetivo es que dejes de ver los microservicios como simples contenedores de código y los entiendas como fronteras lingüísticas y de modelo.

    El artículo de **Martin Fowler sobre Bounded Context** es la lectura canónica. Léelo con atención. El concepto clave es que un término (como "Cliente") puede significar cosas diferentes en distintas partes del negocio (Ventas vs. Soporte). Un Contexto Delimitado es la frontera explícita donde un modelo de dominio y un lenguaje específico tienen validez. No hay un "Cliente" universal.

    El video de **Eric Evans**, el creador de DDD, te dará una perspectiva de primera mano sobre cómo estos "límites" son cruciales para evitar que los microservicios se conviertan en un "gran barro distribuido". Te ayudará a conectar la teoría con la práctica de definir los límites de tus servicios.

    Al final de este módulo, deberías ser capaz de tomar un dominio de negocio simple, identificar los diferentes contextos lingüísticos y proponer límites claros para los microservicios, explicando qué modelo pertenece a cada contexto.
*   **Recursos Web:**
    *   **Bounded Contexts - Conceptos Fundamentales:**
        * [Bounded Context - Martin Fowler](https://martinfowler.com/bliki/BoundedContext.html) (1h)
*   **Videos:** 
    *   [DDD and Microservices: At Last, Some Boundaries! - Eric Evans](https://www.youtube.com/watch?v=yPvef9R3k-M) (50min)

### Módulo 2: Estructura de Microservicio NebulaE (Path 2)
*   **Objetivo:** Comprender la estructura de carpetas fundamental de un microservicio NebulaE.
*   **Descripción:** En este módulo, diseccionarás la anatomía de un microservicio generado por NebulaE. El objetivo es que entiendas el propósito de cada carpeta y archivo, y cómo contribuyen a una arquitectura limpia y organizada.

    Usando la **documentación interna** y el **video explicativo**, analizarás la estructura de carpetas generada por el CLI. Los directorios clave que debes entender son:

    *   `frontend`: Contiene la aplicación de React, que es el micro-frontend de este servicio.
    *   `api`: Define la capa de API Gateway, responsable de exponer los endpoints al exterior y componer las vistas de lectura (queries).
    *   `backend`: Aquí reside la lógica de negocio principal (el "write-side" de CQRS). Contiene los agregados, eventos de dominio y la lógica de comandos.
    *   `deployment`: Incluye los archivos necesarios para desplegar el microservicio (ej: Dockerfiles, configuraciones de Kubernetes).
    *   `playground`: Un espacio aislado para que puedas experimentar con los componentes de tu microservicio sin afectar la aplicación principal.

    Tu tarea es navegar por esta estructura y entender el flujo de una petición. ¿Dónde se define una ruta de la API? ¿Cómo invoca un comando en el backend? ¿Dónde se guarda un evento? Al final, deberías poder explicar el rol de cada carpeta y cómo se relacionan entre sí para implementar los patrones de CQRS y Event Sourcing.
*   **Recursos Web:**
    *   [npm: @nebulae/cli](https://www.npmjs.com/package/@nebulae/cli)
    *   [GitHub: nebulae-university/repositories](https://github.com/orgs/nebulae-university/repositories)
    *   [Nebulae Microservice Anatomy Overview](https://github.com/nebulae-university/software-development/blob/main/documents/nebulae_microservice_anatomy_overview.md)
    *   [Architecture Benchmark Analysis: Gemini](https://github.com/nebulae-university/software-development/blob/main/documents/architecture_benchmark_analysis_gemini.md)
    *   [Architecture Benchmark Analysis: Sonnet](https://github.com/nebulae-university/software-development/blob/main/documents/architecture_benchmark_analysis_sonnet.md)
    *   [Micro-frontends Pattern: Server-side page fragment composition](https://microservices.io/patterns/ui/server-side-page-fragment-composition.html)
    *   [Micro-frontends in Action: Chapter 4](https://livebook.manning.com/book/micro-frontends-in-action/chapter-4)
    *   [API Gateway Pattern](https://microservices.io/patterns/apigateway.html)
*   **Videos:** ["Estructura y Arquitectura de un Microservicio NebulaE"](https://www.youtube.com/watch?v=8XgWmuzcAkE) (1h)

### Módulo 3: Asincronismo en JavaScript (Path 3)
*   **Objetivo:** Dominar los patrones de asincronismo de NodeJS.
*   **Descripción:** NodeJS es asíncrono por naturaleza, y dominar este concepto es absolutamente crítico para ser un desarrollador de backend eficaz. Este módulo te llevará desde los patrones más antiguos hasta la sintaxis moderna para manejar operaciones que no bloquean el hilo principal.

    La **guía de asincronismo de MDN** es tu recurso principal. Debes entender la evolución y el propósito de cada patrón:

    1.  **Callbacks:** El enfoque original. Entiende el problema que resuelven, pero también por qué conducen al "Callback Hell" (código anidado y difícil de leer).
    2.  **Promises (Promesas):** La solución al Callback Hell. Una promesa es un objeto que representa la eventual finalización (o fallo) de una operación asíncrona. Aprende a consumir promesas con `.then()` y a manejar errores con `.catch()`.
    3.  **Async/Await:** Azúcar sintáctico sobre las promesas. Te permite escribir código asíncrono que se ve y se comporta como código síncrono, haciéndolo mucho más legible y fácil de razonar. Esta es la forma en que escribimos la mayor parte de nuestro código asíncrono en NebulaE.

    Los **videos** te proporcionarán ejemplos prácticos y visuales de cada uno de estos patrones. Tu objetivo es no solo entenderlos, sino ser capaz de convertir un trozo de código basado en callbacks a uno que use promesas, y finalmente a uno que use async/await. Al final, deberías poder explicar qué es el "event loop" de NodeJS a un alto nivel y por qué async/await es la mejor herramienta para el trabajo.
*   **Recursos Web:**
    *   [Guía de asincronismo en JS: Callbacks, Promises, Async/Await (MDN)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous) (2h)
*   **Videos:** 
    *   [Asincronismo en JavaScript](https://www.youtube.com/watch?v=PoRJizFvM7s)
    *   [Promises y Async/Await](https://www.youtube.com/watch?v=V_Kr9OSfDeU)

### Módulo 4: Hooks de React (Path 4)
*   **Objetivo:** Utilizar los hooks esenciales para manejar el estado y los efectos secundarios.
*   **Descripción:** Si los componentes son los ladrillos de React, los hooks son las herramientas que les dan vida. En este módulo, te centrarás en los dos hooks más fundamentales que usarás constantemente.

    La **documentación oficial de React.dev** y los **videos** te guiarán a través de:

    1.  **`useState`:** Este es el hook que te permite añadir estado (memoria) a tus componentes funcionales. El concepto clave es que cuando actualizas una variable de estado con su función `set`, React automáticamente vuelve a renderizar el componente para reflejar el cambio en la UI. Practica creando contadores, manejando inputs de formularios y alternando la visibilidad de elementos.
    2.  **`useEffect`:** Este hook te permite ejecutar "efectos secundarios" en tus componentes. Un efecto secundario es cualquier código que interactúa con el mundo exterior al componente, como hacer una petición a una API, suscribirse a un evento o manipular el DOM directamente. El concepto clave es el array de dependencias: es el segundo argumento de `useEffect` y controla *cuándo* se vuelve a ejecutar el efecto. Un array vacío `[]` significa que el efecto se ejecuta solo una vez, cuando el componente se monta.

    Tu objetivo es entender la diferencia fundamental entre estado y efectos. `useState` es para datos que el componente *posee*, mientras que `useEffect` es para interactuar con sistemas *externos*. Al final, deberías ser capaz de construir un componente que obtenga datos de una API al montarse (`useEffect`) y los guarde en su estado interno (`useState`) para mostrarlos en la UI.
*   **Recursos Web:**
    *   [Hooks: useState y useEffect (React.dev)](https://react.dev/reference/react/useState) (1.5h)
*   **Videos:** 
    *   [Introducción a Hooks – useState y useEffect](https://www.youtube.com/watch?v=P5p3vMeJ6LQ) (0.5h)
    *   [useState en 15 minutos](https://www.youtube.com/watch?v=O6P86uwfdR0) (0.25h)

### Módulo 5: MongoDB Atlas - Configuración y Primeros Pasos (Path 5)
*   **Objetivo:** Configurar MongoDB Atlas y realizar las primeras conexiones.
*   **Descripción:** Este módulo es práctico y te llevará de la teoría a la acción. El objetivo es que crees tu propio clúster de base de datos en la nube y aprendas a interactuar con él.

    El curso **"Getting Started with MongoDB Atlas"** de MongoDB University es tu guía paso a paso. Las tareas clave que debes completar son:

    1.  **Crear una cuenta en MongoDB Atlas:** Regístrate y familiarízate con el dashboard principal.
    2.  **Desplegar un clúster gratuito (M0):** Aprende a configurar un clúster, seleccionando un proveedor de nube y una región. Entiende que Atlas se encarga de toda la provisión y gestión de la infraestructura por ti.
    3.  **Configurar la seguridad:** Esta es una parte crítica. Debes aprender a añadir tu dirección IP a la lista de acceso (IP Access List) para poder conectarte a tu clúster. También crearás tu primer usuario de base de datos con un nombre y una contraseña.
    4.  **Cargar datos de ejemplo:** Atlas proporciona datasets de ejemplo que puedes cargar en tu clúster. Esto te dará datos reales con los que podrás practicar consultas.
    5.  **Obtener la cadena de conexión:** Aprende a encontrar y copiar la "connection string". Esta es la URL especial que tus aplicaciones usarán para conectarse a la base de datos.

    El **video tutorial** reforzará estos pasos visualmente. Al final de este módulo, no solo tendrás un clúster de MongoDB funcionando en la nube, sino que también entenderás los pasos de seguridad básicos necesarios para protegerlo y permitir el acceso a tus aplicaciones.
*   **Recursos Web:**
    *   [Getting Started with MongoDB Atlas](https://learn.mongodb.com/courses/getting-started-with-mongodb-atlas) (1.25h)
*   **Videos:** Tutorial de configuración de MongoDB Atlas

### Módulo 6: Comandos Esenciales de Terminal y Navegación (Path 6)
*   **Objetivo:** Dominar los comandos esenciales de la terminal para navegación y manipulación básica de archivos.
*   **Descripción:** La terminal es una de las herramientas más poderosas de un desarrollador. En este módulo, te asegurarás de dominar los comandos fundamentales para moverte por el sistema de archivos y realizar operaciones básicas. La eficiencia en la línea de comandos te ahorrará incontables horas a lo largo de tu carrera.

    Utiliza los **recursos de Wikipedia y GNU Coreutils** como referencia, pero el aprendizaje real vendrá de la práctica. Los **videos** te darán un tour guiado. Abre tu terminal y practica con cada uno de estos comandos hasta que se sientan como una segunda naturaleza:

    *   **Navegación:**
        *   `pwd` (print working directory): ¿Dónde estoy?
        *   `ls` (list): ¿Qué hay aquí? (Usa `ls -la` para ver archivos ocultos y detalles).
        *   `cd` (change directory): Muévete a otro directorio (Usa `cd ..` para subir un nivel, `cd ~` para ir a tu home).
    *   **Manipulación de archivos y directorios:**
        *   `mkdir` (make directory): Crea un nuevo directorio.
        *   `touch`: Crea un archivo vacío.
        *   `cp` (copy): Copia un archivo o directorio.
        *   `mv` (move): Mueve o renombra un archivo o directorio.
        *   `rm` (remove): Elimina un archivo (Usa `rm -r` para eliminar un directorio y su contenido. ¡CON CUIDADO!).
    *   **Permisos:**
        *   `chmod` (change mode): Entiende a un alto nivel cómo cambiar los permisos de lectura, escritura y ejecución de un archivo.

    El objetivo no es memorizar cada opción de cada comando, sino construir un mapa mental de cómo navegar y manipular tu sistema de archivos sin depender de una interfaz gráfica.
*   **Recursos Web:**
    *   **Comandos Bash:**
        * [Comandos Bash – Wikipedia (Español)](https://es.wikipedia.org/wiki/Comandos_Bash)
        * [GNU Coreutils – ls, cd, etc. (Inglés)](https://www.gnu.org/software/coreutils/)
*   **Videos:** 
    *   [Comandos LINUX Básicos Desde Cero – DeciLearn (Español)](https://www.youtube.com/watch?v=_KCc-tvpPRM) (2022)
    *   [Linux Command Line for Beginners – freeCodeCamp (Inglés)](https://www.youtube.com/watch?v=sWbUDq4S6Y8) (2021)

---

## Día 3: Tecnologías de Datos y Herramientas

### Introducción del Día

Hoy es un día de acción y herramientas. El objetivo es que instales y utilices las tecnologías clave de nuestro ecosistema. Generarás tu primer microservicio con el CLI de NebulaE, un hito importante en tu aprendizaje. Profundizarás en el estilo de programación declarativa que favorecemos y te introducirás a la gestión de estado global en el frontend con Redux. Además, te conectarás directamente a tu base de datos usando la shell de MongoDB y mejorarás tu dominio de la terminal con herramientas de búsqueda potentes. Se espera que al final del día te sientas cómodo generando código y manipulando datos desde la línea de comandos.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Instalación del Entorno y Generación de Primer Microservicio (Path 2)
*   **Módulo 2:** Programación Declarativa vs Imperativa (Path 3)
*   **Módulo 3:** Introducción a Redux - Conceptos Fundamentales (Path 4)
*   **Módulo 4:** Conexión a MongoDB usando MongoDB Shell (Path 5)
*   **Módulo 5:** Manipulación y Búsqueda de Texto con grep y find (Path 6)

### Módulo 1: Instalación del Entorno y Generación de Primer Microservicio (Path 2)
*   **Objetivo:** Instalar el entorno de desarrollo de NebulaE y generar el primer microservicio desde cero.
*   **Descripción:** Este es el módulo donde todo lo aprendido hasta ahora converge en una acción concreta. El objetivo es instalar la interfaz de línea de comandos (CLI) de NebulaE y usarla para generar tu primer microservicio.

    Las tareas son muy prácticas:

    1.  **Instalación del CLI de NebulaE:** Siguiendo la documentación, instalarás nuestro paquete `@nebulae/cli` de forma global en tu sistema usando npm. Esto te dará acceso al comando `nebulae` en tu terminal.
    2.  **Generación de un microservicio:** Ejecutarás el comando para generar un nuevo microservicio. Presta atención a las preguntas que te hace el CLI (como el nombre del servicio, el agregado principal, etc.).
    3.  **Exploración del código generado:** Una vez generado, abrirás el proyecto en tu editor de código y verificarás que la estructura de carpetas (`frontend`, `api`, `backend`, etc.) coincide con lo que aprendiste en el módulo de "Estructura de Microservicio NebulaE".
    4.  **Aplicación de conceptos:** Este ejercicio práctico es una aplicación directa de los conceptos de los días anteriores. La estructura del microservicio está diseñada en torno a los principios de DDD y CQRS. El backend utiliza NodeJS y su asincronismo. El frontend es una aplicación de React. Y todo está gestionado con Git y se ejecuta sobre Node.js, herramientas que ya has instalado.

    Al final de este módulo, tendrás un esqueleto de microservicio funcional en tu máquina local. Este será el punto de partida para las implementaciones de las próximas semanas.
*   **Recursos Web:**
    *   [npm: @nebulae/cli](https://www.npmjs.com/package/@nebulae/cli)
    *   [Architecture Overview](https://www.npmjs.com/package/@nebulae/cli#architecture-overview)
    *   [npm: @nebulae/event-store](https://www.npmjs.com/package/@nebulae/event-store)
    *   [npm: @nebulae/backend-node-tools](https://www.npmjs.com/package/@nebulae/backend-node-tools)
*   **Videos:** [Instalación del Entorno y Generación de Primer Microservicio](https://youtu.be/MdLlDh7y9kI)

### Módulo 2: Programación Declarativa vs Imperativa (Path 3)
*   **Objetivo:** Dominar el estilo de programación declarativa utilizado en NebulaE.
*   **Descripción:** Este módulo es una continuación práctica del Día 1. El objetivo es que dejes de *entender* la diferencia entre programación declarativa e imperativa y comiences a *aplicarla* de forma natural. Nos centraremos en los métodos de Array, que son la herramienta principal para escribir código declarativo en JavaScript.

    La **documentación de MDN** sobre los métodos de Array es tu referencia. No tienes que memorizarla, sino entender el propósito de los métodos más comunes:

    *   `.map()`: Transforma cada elemento de un array en algo nuevo. (Ej: un array de usuarios -> un array de nombres de usuario).
    *   `.filter()`: Crea un nuevo array con solo los elementos que cumplen una condición. (Ej: un array de números -> un array solo con los números pares).
    *   `.reduce()`: "Reduce" un array a un único valor. (Ej: un array de números -> la suma de todos los números).

    El **video sobre métodos de Array** te mostrará ejemplos prácticos de cómo usar y encadenar estos métodos. Tu tarea es tomar problemas que normalmente resolverías con un bucle `for` (imperativo) y reescribirlos usando una combinación de `.map()`, `.filter()` y `.reduce()` (declarativo).

    El concepto clave a extraer es la **composición**. El poder del enfoque declarativo reside en encadenar estas funciones para realizar operaciones complejas de una manera muy legible y concisa. Al final, deberías sentirte cómodo manipulando colecciones de datos sin necesidad de escribir bucles `for`.
*   **Recursos Web:**
    *   [Práctica Declarativa: Métodos de Array (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) (1.5h)
*   **Videos:** [Métodos de Array en JavaScript](https://www.youtube.com/watch?v=8MoElay6dWU)

### Módulo 3: Introducción a Redux - Conceptos Fundamentales (Path 4)
*   **Objetivo:** Comprender los conceptos fundamentales de Redux para gestión de estado global.
*   **Descripción:** Mientras que `useState` es excelente para el estado local de un componente, las aplicaciones complejas necesitan una forma de gestionar el "estado global" (datos que son compartidos por muchas partes de la aplicación). Aquí es donde entra Redux. El objetivo de este módulo es que entiendas el *problema* que Redux resuelve y los conceptos básicos de su solución.

    La **documentación oficial de Redux** y el **video tutorial** te introducirán a los tres pilares de Redux:

    1.  **Store (Tienda):** Es un único objeto JavaScript que contiene todo el estado de tu aplicación. Es la "única fuente de verdad".
    2.  **Actions (Acciones):** Son objetos planos que describen *qué pasó*. No contienen la lógica, solo la intención. (Ej: `{ type: 'todos/todoAdded', payload: 'Comprar leche' }`).
    3.  **Reducers (Reductores):** Son funciones puras que toman el estado actual y una acción, y devuelven el *nuevo* estado. Son los únicos que pueden modificar el estado. La clave es que no modifican el estado original, sino que devuelven una copia inmutable con los cambios.

    El flujo de datos en Redux es unidireccional: una acción se "despacha" al store, el store llama al reducer correspondiente con el estado actual y la acción, el reducer devuelve el nuevo estado, y el store se actualiza.

    Tu objetivo no es convertirte en un experto en Redux en un día, sino entender este flujo y el propósito de cada una de sus partes. Al final, deberías poder dibujar un diagrama del flujo de datos de Redux y explicar el rol del store, las acciones y los reducers.
*   **Recursos Web:**
    *   [Redux: Conceptos Fundamentales (Redux.js.org)](https://redux.js.org/introduction/getting-started) (1.5h)
*   **Videos:** Tutoriales de Redux básico
    * [Redux Tutorial](https://www.youtube.com/watch?v=poQXNp9ItL4) (1.75h)

### Módulo 4: Conexión a MongoDB usando MongoDB Shell (Path 5)
*   **Objetivo:** Aprender a interactuar con MongoDB usando la shell nativa.
*   **Descripción:** Ahora que tienes un clúster de MongoDB Atlas en la nube, es hora de conectarte a él y empezar a "hablar" con la base de datos. La forma más directa de hacerlo es a través de la **MongoDB Shell (`mongosh`)**, una interfaz de línea de comandos interactiva.

    El curso de **MongoDB University** te guiará en el proceso:

    1.  **Instalación de `mongosh`:** Primero, deberás instalar la shell en tu máquina local.
    2.  **Conexión al clúster:** Usarás la "connection string" que obtuviste de Atlas para conectarte a tu clúster desde tu terminal.
    3.  **Operaciones básicas:** Una vez conectado, aprenderás los comandos fundamentales para interactuar con la base de datos. Estos comandos son JavaScript, por lo que la sintaxis te resultará familiar. Las operaciones clave a practicar son:
        *   Mostrar bases de datos y colecciones.
        *   Cambiar a una base de datos específica.
        *   **CRUD (Create, Read, Update, Delete):**
            *   Insertar documentos (`insertOne`, `insertMany`).
            *   Buscar documentos (`findOne`, `find`).
            *   Actualizar documentos (`updateOne`, `updateMany`).
            *   Eliminar documentos (`deleteOne`, `deleteMany`).

    El objetivo es que te sientas cómodo realizando operaciones básicas directamente en la base de datos. Esto es invaluable para la depuración, la inspección de datos y la ejecución de tareas administrativas. Al final, deberías ser capaz de conectarte a tu clúster y realizar las cuatro operaciones CRUD desde la `mongosh`.
*   **Recursos Web:**
    *   [Connecting to a MongoDB Database Using the MongoDB Shell](https://learn.mongodb.com/courses/connecting-to-a-mongodb-database-using-the-mongodb-shell) (1.75h)
*   **Videos:** Material práctico de MongoDB Shell

### Módulo 5: Manipulación y Búsqueda de Texto con grep y find (Path 6)
*   **Objetivo:** Dominar herramientas avanzadas de búsqueda y manipulación de texto en terminal.
*   **Descripción:** Este módulo amplía tus habilidades en la línea de comandos, centrándose en dos de las herramientas más potentes para trabajar con archivos y texto: `find` y `grep`.

    Usa los **recursos y videos** para aprender y practicar:

    1.  **Visualización de archivos:**
        *   `cat` (concatenate): Imprime el contenido completo de un archivo en la terminal. Útil para archivos pequeños.
        *   `less`: Muestra el contenido de un archivo de forma paginada. Esencial para archivos grandes, ya que no carga todo el archivo en memoria.
        *   `head` y `tail`: Muestran las primeras o últimas líneas de un archivo, respectivamente. Muy útil para revisar logs.

    2.  **Búsqueda de contenido (`grep`):**
        *   `grep` (Global Regular Expression Print) es tu navaja suiza para buscar texto dentro de los archivos. Aprende a usarlo para encontrar líneas que coincidan con una cadena de texto o una expresión regular. Practica con sus opciones más comunes, como `-i` (ignorar mayúsculas/minúsculas) y `-r` (búsqueda recursiva en un directorio).

    3.  **Búsqueda de archivos (`find`):**
        *   `find` es la herramienta para buscar archivos y directorios basándose en criterios como el nombre, el tipo, el tamaño o la fecha de modificación. Es mucho más potente que la búsqueda de tu explorador de archivos.

    El objetivo es que dejes de abrir archivos manualmente para buscar cosas. Al final, deberías ser capaz de responder preguntas como "¿En qué archivos de mi proyecto se usa la función `getUser`?" o "Encuéntrame todos los archivos `.log` que se modificaron en las últimas 24 horas" usando una sola línea de comandos.
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

### Introducción del Día

El cuarto día se centra en conectar las piezas. El objetivo es que integres las diferentes tecnologías que has aprendido para construir flujos de datos funcionales. Hoy harás que tu backend en Node.js se comunique con la base de datos de MongoDB y que tu frontend en React se integre con Redux para una gestión de estado robusta. Profundizarás en la programación funcional, un paradigma clave en nuestro estilo de código, y aprenderás a crear potentes cadenas de comandos en la terminal. Se espera que hoy logres una visión más clara de cómo las diferentes capas de la arquitectura interactúan entre sí.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Métodos Funcionales en JavaScript (Path 3)
*   **Módulo 2:** React Redux Integración (Path 4)
*   **Módulo 3:** Conexión MongoDB desde Node.js (Path 5)
*   **Módulo 4:** Encadenamiento de Comandos y Redirección (Path 6)

### Módulo 1: Métodos Funcionales en JavaScript (Path 3)
*   **Objetivo:** Profundizar en programación funcional y métodos de Array.
*   **Descripción:** Este módulo es una inmersión profunda en el paradigma de programación funcional en JavaScript. El objetivo es que no solo uses `.map` o `.filter`, sino que entiendas los principios subyacentes y puedas componer funciones complexas para manipular datos de manera elegante y predecible.

    Los **recursos de MDN y freeCodeCamp** te guiarán a través de:

    1.  **Dominio de `map`, `filter`, `reduce`:** Irás más allá del uso básico. Practicarás encadenando estos métodos para realizar transformaciones de datos en varios pasos sin crear variables intermedias.
    2.  **Programación Funcional:** Se introducirán conceptos clave del paradigma funcional:
        *   **Funciones Puras:** Funciones que, para la misma entrada, siempre devuelven la misma salida y no tienen efectos secundarios observables.
        *   **Inmutabilidad:** La práctica de no modificar los datos existentes, sino crear nuevas estructuras de datos con los valores actualizados. Esto es fundamental para la previsibilidad del estado (y es por eso que Redux lo exige).
        *   **Funciones de Orden Superior (Higher-Order Functions):** Funciones que toman otras funciones como argumentos o las devuelven como resultado (`map`, `filter` y `reduce` son ejemplos perfectos).

    Los **videos** te mostrarán cómo refactorizar código imperativo a un estilo funcional. Tu objetivo es empezar a "pensar en flujos de datos". En lugar de "hacer un bucle y cambiar cosas", pensarás en "tomar estos datos, filtrarlos, luego transformarlos, y finalmente calcular un resultado". Al final, deberías ser capaz de escribir transformaciones de datos complexas usando la composición de funciones puras.
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
*   **Descripción:** Ahora que entiendes los conceptos de React y Redux por separado, es hora de unirlos. Este módulo te enseñará a conectar tus componentes de React al store de Redux para que puedan leer el estado global y despachar acciones.

    La **documentación de React-Redux** y el **video crash course** se centrarán en las herramientas modernas (hooks) que hacen esta integración muy sencilla:

    1.  **`<Provider>`:** Este es un componente de React-Redux que "envuelve" toda tu aplicación. Su único propósito es hacer que el store de Redux esté disponible para todos los componentes que lo necesiten, sin tener que pasar el store manualmente a través de las props.
    2.  **`useSelector`:** Este es un hook que permite a un componente *leer* datos del store de Redux. Le pasas una función que selecciona la porción del estado que te interesa, y `useSelector` se encargará de que tu componente se vuelva a renderizar automáticamente si esos datos cambian.
    3.  **`useDispatch`:** Este hook te da acceso a la función `dispatch` del store. La usarás para despachar acciones desde tus componentes en respuesta a eventos del usuario (como hacer clic en un botón).

    El flujo completo que debes practicar es:
    *   Un usuario interactúa con un componente (ej: hace clic en "Añadir Tarea").
    *   El manejador de eventos del componente usa `useDispatch` para despachar una acción (ej: `{ type: 'todos/todoAdded', ... }`).
    *   El reducer correspondiente actualiza el estado en el store.
    *   El componente que muestra la lista de tareas, que está usando `useSelector` para leer esa parte del estado, se vuelve a renderizar automáticamente para mostrar la nueva tarea.

    Al final, deberías ser capaz de construir una pequeña aplicación donde el estado es gestionado completamente por Redux y los componentes de React son solo la capa de visualización que lee y reacciona a los cambios en el store.
*   **Recursos Web:**
    *   [React Redux: Conectando Redux con React (React-Redux.js.org)](https://react-redux.js.org/introduction/getting-started) (1h)
*   **Videos:** [Crash Course React completo](https://www.youtube.com/watch?v=CgkZ7MvWUAA) (2h)

### Módulo 3: Conexión MongoDB desde Node.js (Path 5)
*   **Objetivo:** Aprender a interactuar con MongoDB desde aplicaciones Node.js.
*   **Descripción:** Mientras que la MongoDB Shell es útil para tareas manuales, tus aplicaciones necesitan una forma programática de conectarse a la base de datos. En este módulo, aprenderás a usar el driver oficial de MongoDB para Node.js para conectar tu backend a tu clúster de Atlas.

    Los **cursos de MongoDB University** te guiarán a través del proceso:

    1.  **Instalación del Driver:** Aprenderás a añadir el paquete `mongodb` a tu proyecto de Node.js como una dependencia.
    2.  **Establecimiento de la Conexión:** Usarás la "connection string" de Atlas para crear un cliente de MongoDB en tu código de Node.js y establecer una conexión con la base de datos. Aprenderás a manejar tanto la conexión exitosa como los posibles errores.
    3.  **Realización de Operaciones CRUD:** Una vez conectado, replicarás las operaciones que hiciste en la shell, pero esta vez desde tu código JavaScript:
        *   Obtendrás una referencia a una colección específica.
        *   Usarás funciones asíncronas (con `async/await`) para insertar, buscar, actualizar y eliminar documentos.
        *   Aprenderás a manejar los resultados de estas operaciones (por ejemplo, el documento encontrado o el número de documentos modificados).

    El objetivo es que te sientas cómodo escribiendo la lógica de acceso a datos en tu aplicación de Node.js. Al final de este módulo, deberías ser capaz de escribir un script simple de Node.js que se conecte a tu base de datos de Atlas y realice las cuatro operaciones CRUD, registrando los resultados en la consola. Esta es la base para construir los repositorios de datos en tus microservicios.
*   **Recursos Web:**
    *   [Connecting to a MongoDB Database Using the MongoDB Shell](https://learn.mongodb.com/courses/connecting-to-a-mongodb-database-using-the-mongodb-shell) (1.75h)
    *   [Connecting to MongoDB in Node.js](https://learn.mongodb.com/courses/connecting-to-mongodb-in-nodejs) (1h)
*   **Videos:** Material práctico de conexión con MongoDB

### Módulo 4: Encadenamiento de Comandos y Redirección (Path 6)
*   **Objetivo:** Dominar técnicas avanzadas de encadenamiento de comandos y redirección en terminal.
*   **Descripción:** Este módulo te enseñará a componer las herramientas de línea de comandos que has aprendido para crear flujos de trabajo potentes y automatizados. El objetivo es que dejes de ver los comandos como herramientas aisladas y empieces a verlos como bloques de construcción que puedes conectar.

    Los **recursos y videos** se centrarán en tres conceptos clave:

    1.  **Pipes (`|`):** El pipe es uno de los conceptos más poderosos de la terminal. Te permite tomar la salida estándar (stdout) de un comando y usarla como la entrada estándar (stdin) de otro. Esto te permite "encadenar" comandos. Por ejemplo, `ls -l | grep ".js"` primero lista todos los archivos con detalles y luego filtra esa lista para mostrar solo las líneas que contienen ".js".
    2.  **Redirección (`>` y `>>`):** La redirección te permite cambiar dónde va la salida de un comando.
        *   `>`: Redirige la salida a un archivo, sobrescribiendo el archivo si ya existe. (Ej: `ls -l > mis_archivos.txt`).
        *   `>>`: Redirige la salida a un archivo, añadiéndola al final del archivo si ya existe. (Ej: `echo "Nuevo log" >> log.txt`).
    3.  **Operadores de Control (`;`, `&&`, `||`):** Estos te permiten ejecutar múltiples comandos en una sola línea.
        *   `;`: Ejecuta los comandos en secuencia, sin importar si el anterior tuvo éxito o no.
        *   `&&` (AND): Ejecuta el segundo comando solo si el primero tuvo éxito.
        *   `||` (OR): Ejecuta el segundo comando solo si el primero falló.

    Tu objetivo es practicar la combinación de estas técnicas. Intenta construir comandos complejos, como "Encuentra todos los archivos de log en mi proyecto, busca las líneas que contienen la palabra 'ERROR', y guarda esas líneas en un nuevo archivo llamado `errores.log`". Al final, deberías poder automatizar tareas simples combinando varios comandos en una sola línea.
*   **Recursos Web:**
    *   **Pipes y Redirección:**
        * [Guía de Redirección y Pipes en Linux – Tecmint (Español)](https://www.tecmint.com/use-linux-pipes-to-connect-commands/)
        * [Bash Reference Manual – Pipelines (Inglés)](https://www.gnu.org/software/bash/manual/html_node/Pipelines.html)
*   **Videos:** 
    *   [Pipes y Redirecciones en Linux (Español)](https://www.youtube.com/watch?v=Hsno6279tik) 
    *   [Linux Pipes and Redirection (Inglés)](https://www.youtube.com/watch?v=mV_8GbzwZMM) (2022)

---

## Día 5: Consolidación y Práctica Integral

### Introducción del Día

Llegamos al último día de la semana, dedicado a consolidar y aplicar todo lo aprendido. El objetivo es que conectes todos los conceptos a través de prácticas integrales que simulan el trabajo diario de un desarrollador en NebulaE. Refinarás tus conocimientos de JavaScript, construirás un componente de React con estado global, realizarás operaciones en MongoDB desde múltiples interfaces y darás tus primeros pasos en la automatización de tareas. Se espera que al final del día tengas una visión holística del ecosistema y puedas articular cómo cada tecnología contribuye a la solución final.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Conceptos Avanzados de JavaScript (Path 3)
*   **Módulo 2:** Práctica Integral React (Path 4)
*   **Módulo 3:** Práctica Integral MongoDB (Path 5)
*   **Módulo 4:** Configuración Completa del Entorno (Path 6)
*   **Módulo 5:** Integración de Conocimientos

### Módulo 1: Conceptos Avanzados de JavaScript (Path 3)
*   **Objetivo:** Consolidar conocimientos de JavaScript con conceptos de igualdad y valores falsy.
*   **Descripción:** A menudo, los errores más sutiles en JavaScript provienen de una mala comprensión de cómo el lenguaje maneja la igualdad y los valores "falsos". Este módulo se enfoca en clarificar estos conceptos para que puedas escribir código más robusto.

    La **documentación de MDN** y los **videos** son tus recursos. Los conceptos clave son:

    1.  **Igualdad Estricta (`===`) vs. Igualdad Débil (`==`):** La regla de oro es: **usa siempre la igualdad estricta (`===`)**. Aprende por qué. La igualdad estricta compara tanto el valor como el tipo, sin hacer conversiones mágicas. La igualdad débil (`==`) intenta convertir los tipos antes de comparar, lo que lleva a resultados inesperados (ej: `0 == false` es `true`). Entiende los peligros de la coerción de tipos.
    2.  **Valores "Falsy":** En JavaScript, no solo `false` es falso en un contexto booleano. Hay una lista corta de valores "falsy" que debes memorizar: `false`, `0`, `""` (string vacío), `null`, `undefined`, y `NaN`. Todos los demás valores son "truthy" (incluyendo objetos vacíos `{}` y arrays vacíos `[]`).

    Tu objetivo es entender cómo estos conceptos afectan las sentencias condicionales (`if`). Practica escribiendo condicionales que verifiquen explícitamente la existencia de valores. Por ejemplo, en lugar de `if (miVariable)`, que podría fallar si `miVariable` es `0` o un string vacío pero es un valor válido, podrías necesitar una verificación más explícita como `if (miVariable !== undefined && miVariable !== null)`. Al final, deberías poder explicar la diferencia entre `==` y `===` con ejemplos claros y listar los seis valores falsy de memoria.
*   **Recursos Web:**
    *   [Igualdad y Falsy Values en JS (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness) (0.5h)
*   **Videos:** 
    *   [Igualdad en JavaScript](https://www.youtube.com/watch?v=jD2BuBfxRn8)
    *   [Falsy Values](https://www.youtube.com/watch?v=5DVqAFhfSsE)

### Módulo 2: Práctica Integral React (Path 4)
*   **Objetivo:** Conectar el frontend de tu microservicio con un estado global de Redux y manejar un flujo de datos completo.
*   **Descripción:** En esta práctica, darás vida al `frontend` de tu microservicio. Ya no es un ejercicio aislado; es una implementación dentro de la estructura real de tu proyecto que creaste en el Día 3.
    *   **Práctica Dirigida:**
        1.  **Localiza tu micro-frontend:** Navega a la carpeta `frontend` de tu microservicio.
        2.  **Crea un nuevo componente:** Dentro de la estructura de componentes existente (ej: `frontend/src/components/`), crea un nuevo componente funcional en su propio archivo (ej: `DataFetcher.js`).
        3.  **Implementa el flujo de datos de Redux:**
            *   Define una nueva acción y un nuevo reducer para manejar una lista de datos de ejemplo.
            *   Usa `useEffect` en tu componente `DataFetcher` para despachar una acción que cargue datos de ejemplo en el store de Redux cuando el componente se monte.
            *   Usa el hook `useSelector` en tu componente para leer esa lista de datos del store y mostrarla.
        4.  **Añade interacción:** Agrega un botón en tu componente que, al hacer clic, despache otra acción para añadir un nuevo elemento a la lista en el store de Redux.
        5.  **Integra el componente:** Importa y renderiza tu nuevo componente `DataFetcher` en alguna de las páginas existentes del micro-frontend para que sea visible.
    *   **Meta a lograr:** Tener un componente, dentro de la aplicación de React de tu microservicio, que pueda despachar acciones a Redux y reaccionar a los cambios en el estado global, mostrando los datos actualizados sin recargar la página.
*   **Recursos Web:** Integración de todos los recursos de React de la semana
*   **Videos:** Proyecto práctico guiado

### Módulo 3: Práctica Integral MongoDB (Path 5)
*   **Objetivo:** Realizar operaciones completas con MongoDB desde diferentes interfaces.
*   **Descripción:** Al igual que el módulo de React, esta es una práctica integral para consolidar tus habilidades con MongoDB. El objetivo es que te sientas cómodo interactuando con tu base de datos tanto para tareas administrativas como a través de tu aplicación.

    **Integrarás todos los recursos de MongoDB de la semana** y seguirás la **sesión práctica en video**. Las tareas a realizar son:

    1.  **Desde la MongoDB Shell (`mongosh`):**
        *   Conéctate a tu clúster de Atlas.
        *   Crea una nueva base de datos y una nueva colección.
        *   Inserta varios documentos con diferentes estructuras.
        *   Escribe consultas (`find`) para filtrar los documentos basándote en diferentes criterios (ej: igualdad, operadores de comparación como `$gt` (mayor que)).
        *   Actualiza uno o más documentos.
        *   Elimina un documento.

    2.  **Desde Node.js:**
        *   Crea un nuevo script de Node.js.
        *   Conéctate a la misma base de datos de Atlas.
        *   Escribe funciones `async` para replicar las mismas operaciones CRUD que hiciste en la shell.
        *   Asegúrate de manejar los errores y de cerrar la conexión a la base de datos correctamente.

    El objetivo es verificar que puedes realizar las mismas operaciones desde dos entornos diferentes. Esto refuerza tu comprensión de los comandos de MongoDB y te da la confianza para empezar a construir la capa de persistencia de tus microservicios. Al final, deberías tener un script de Node.js que pueda manipular datos en tu base de datos de Atlas de forma fiable.
*   **Recursos Web:** Integración de todos los recursos de MongoDB de la semana
*   **Videos:** Sesión práctica con MongoDB

### Módulo 4: Configuración Completa del Entorno (Path 6)
*   **Objetivo:** Completar la configuración del entorno de desarrollo con todas las herramientas necesarias.
*   **Descripción:** Este módulo final de herramientas es una lista de verificación para asegurar que tu entorno de desarrollo está 100% listo para ser productivo en NebulaE. Además de verificar las instalaciones, te introducirás a la automatización básica con scripts de Bash.

    Las tareas son:

    1.  **Verificación de Herramientas:** Vuelve a verificar que `git`, `nvm`, y `node` están instalados y configurados correctamente. Asegúrate de haber instalado los paquetes globales de npm que sean necesarios, como el CLI de NebulaE.
    2.  **Automatización con Bash:** La **guía de programación de Bash** y el **video crash course** te introducirán a la escritura de scripts de shell simples. El objetivo no es convertirte en un experto en Bash, sino aprender a automatizar tareas repetitivas.
        *   Crea tu primer script `.sh`.
        *   Aprende a usar variables y a ejecutar comandos dentro del script.
        *   Haz que tu script sea ejecutable con `chmod +x mi_script.sh`.
        *   Practica creando un script que haga algo útil, como crear una estructura de carpetas para un nuevo proyecto o ejecutar una serie de comandos de limpieza.

    Al final de este módulo, no solo tendrás un entorno de desarrollo robusto y verificado, sino que también habrás dado tus primeros pasos en la automatización de tareas, una habilidad fundamental en el mundo de DevOps.
*   **Recursos Web:**
    *   **Instalación de herramientas:**
        * [Instalación de Git (Español)](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)
        * [nvm-sh/nvm – GitHub](https://github.com/nvm-sh/nvm#installing-and-updating)
    *   **Automatización:**
        * [Programación de Bash (Español)](https://www.freecodecamp.org/espanol/news/tutorial-de-programacion-de-bash-script-de-shell-de-linux-y-linea-de-comandos-para-principiantes/)
*   **Videos:** [Bash Scripting Crash Course (Inglés)](https://www.youtube.com/watch?v=tK9Oc6AEnR4) (2022)

### Módulo 5: Integración de Conocimientos
*   **Objetivo:** Conectar todos los conceptos aprendidos durante la semana.
*   **Descripción:** Esta es una sesión de recapitulación para conectar todos los puntos. El objetivo es que puedas articular cómo las diferentes tecnologías y conceptos que has aprendido encajan en el panorama general del desarrollo en NebulaE.

    Usando la **síntesis de materiales** y la **sesión de video**, reflexionarás sobre las siguientes conexiones:

    *   ¿Cómo los principios de **DDD** (Path 1) informan la estructura de un microservicio **NebulaE** (Path 2)?
    *   ¿Cómo el backend en **Node.js** (Path 3) se conecta a **MongoDB** (Path 5) para persistir los datos?
    *   ¿Cómo el frontend en **React** (Path 4) se comunica con el backend (aunque aún no hayamos construido la API, puedes conceptualizarlo)?
    *   ¿Cómo las **herramientas CLI** (Path 6) te permiten gestionar, construir y ejecutar todo el sistema?

    El objetivo es que construyas un mapa mental de alto nivel del ecosistema usando miro.com. Dibuja un diagrama que muestre un microservicio, su base de datos, su frontend, y cómo interactuarías con él como desarrollador. Esta visión holística es crucial para prepararte para la Semana 2, donde empezarás a implementar lógica de negocio real dentro de esta estructura.
*   **Recursos Web:** Síntesis de todos los materiales de la semana

---

## Evaluación Integral de la Semana 1: Proyecto de Catering Corporativo

### Introducción y Contexto del Proyecto

A lo largo de esta semana, aplicarás los conceptos de cada path en un único proyecto integral. En lugar de ejercicios aislados, construirás gradualmente una solución de software basada en un caso de estudio del mundo real. El objetivo es consolidar tu aprendizaje y demostrar tu capacidad para integrar arquitectura, backend, frontend, persistencia y herramientas.

**El Escenario: Digitalización de un Servicio de Catering Corporativo**

Una empresa de catering busca optimizar su proceso de gestión de pedidos y entregas. Trabajarás a partir de la siguiente entrevista ficticia con un representante del negocio para modelar e implementar una parte de la solución.

<details>
<summary>Ver Entrevista con el Representante del Negocio</summary>

**Entrevistador:** Gracias por su tiempo. Para comenzar, ¿podría describir cómo se recibe y procesa un pedido actualmente?
**Representante:** Claro. El cliente entra a nuestra web o nos llama. Elige el menú, indica la fecha de entrega y el número de personas. Luego, un coordinador revisa si hay disponibilidad y confirma por correo o teléfono.

**Entrevistador:** ¿Qué información específica necesitan para aceptar un pedido?
**Representante:** Nombre de la empresa, persona de contacto, teléfono, correo, dirección de entrega, número de personas, menú seleccionado, alergias o restricciones alimenticias, y hora deseada de entrega.

**Entrevistador:** Una vez confirmado el pedido, ¿qué pasos siguen internamente?
**Representante:** Generamos una orden interna para cocina y logística. Cocina revisa inventario y solicita compras si es necesario. Logística asigna transporte y ruta. El día de la entrega, cocina prepara desde temprano y logística recoge y distribuye.

**Entrevistador:** ¿Quiénes participan en este proceso y cuáles son sus roles?
**Representante:** Coordinador de pedidos, Jefe de cocina, Compras, Logística y Transportista.

**Entrevistador:** ¿Existen métricas que utilicen para evaluar el servicio?
**Representante:** Sí. Puntualidad en entregas, porcentaje de pedidos sin incidencias, satisfacción del cliente y número de pedidos repetidos.

**Entrevistador:** ¿Cuáles son las incidencias más comunes?
**Representante:** Direcciones erróneas, retrasos por tráfico, cambios de último minuto y problemas con inventario.

**Entrevistador:** ¿Hay algún flujo especial para pedidos urgentes?
**Representante:** Sí, pedidos con menos de 24 horas de anticipación se marcan como urgentes y tienen un proceso especial.

**Entrevistador:** ¿Cómo manejan la facturación?
**Representante:** Contabilidad genera la factura electrónica. Clientes recurrentes se facturan mensual, otros por pedido.

**Entrevistador:** ¿Qué términos clave usan internamente?
**Representante:** Pedido, orden interna, menú base, pedido urgente, incidencia, plan de cocina, ruta de entrega, cliente recurrente y pedido cancelado.

**Entrevistador:** ¿Existen temporadas o eventos que cambien la forma en que trabajan?
**Representante:** En diciembre y fechas especiales, alta demanda y menús temáticos.

**Entrevistador:** ¿Alguna regla de negocio importante?
**Representante:** No aceptamos pedidos con menos de 12 horas de anticipación, cancelaciones con menos de 24 horas se cobran al 50%, y los pedidos urgentes tienen menú reducido.

</details>

### Entregable: Tablero de Diseño en Miro

Para esta evaluación, no escribirás código. En su lugar, consolidarás todo tu entendimiento teórico en un único **tablero de Miro.com público**. Este tablero será tu lienzo para diseñar la solución al problema de catering, demostrando tu comprensión de los patrones y la arquitectura de NebulaE.

**Instrucciones del Entregable:**

Crea un tablero en Miro y organiza las siguientes secciones, cada una respondiendo a las actividades y preguntas propuestas durante la semana.

**Parte 1: Análisis y Diseño Estratégico (DDD)**
1.  **Glosario del Lenguaje Ubicuo:** Crea una tabla con los términos clave extraídos de la entrevista, su definición y el contexto en el que aplica.
2.  **Event Storming (Simplificado):** Modela el flujo principal de un pedido, desde que se solicita hasta que se entrega, identificando los **Eventos de Dominio** (ej: `PedidoSolicitado`, `DisponibilidadConfirmada`, `OrdenEnviadaACocina`).
3.  **Contextos Delimitados (Bounded Contexts):** A partir del lenguaje y los eventos, propón al menos 3 o 4 Bounded Contexts (ej: `Gestión de Pedidos`, `Cocina`, `Logística`, `Facturación`). Describe brevemente la responsabilidad principal de cada uno.
4.  **Mapa de Contextos:** Dibuja un diagrama que muestre tus Bounded Contexts y las relaciones entre ellos (ej: `Upstream/Downstream`, `Shared Kernel`).

**Parte 2: Diseño Técnico y Alineación con NebulaE**
1.  **Mapa de Componentes NebulaE:**
    *   Asigna cada uno de tus Bounded Contexts a un **microservicio** hipotético de NebulaE.
    *   Para **un (1)** de esos microservicios (ej: `Servicio de Pedidos`), define su **Agregado** principal (ej: `Pedido`).
    *   Lista los **Eventos de Dominio** que este agregado emitiría (ej: `PedidoCreado`, `PedidoConfirmado`).
2.  **Diseño de Contratos (Interfaces):**
    *   Para tu agregado seleccionado, define sus contratos siguiendo las convenciones de NebulaE:
        *   **Comandos:** `Pedido.crear`, `Pedido.confirmar`, `Pedido.cancelar` (incluye el payload mínimo para cada uno).
        *   **Eventos:** `PedidoCreado{v1}`, `PedidoConfirmado{v1}` (incluye el `eventTypeVersion` y el payload).
        *   **Queries:** `pedidoById`, `pedidosPorFecha` (describe qué información deberían devolver).
3.  **Diagrama de Flujo de Datos:**
    *   Crea un diagrama de secuencia para un flujo de **escritura (WRITE)**. Muestra cómo un `Comando` viaja desde el `frontend` (conceptual), pasa por la `api`, es manejado por el `backend`, genera un `Evento` y se persiste en la base de datos del `playground` (MongoDB local).
    *   Crea un diagrama de secuencia para un flujo de **lectura (READ)**. Muestra cómo una petición del `frontend` llega a la `api`, que lee directamente de una `vista materializada` (conceptual) en MongoDB y devuelve los datos.
4.  **Justificación Arquitectónica (Texto):**
    *   Responde a las siguientes preguntas en un bloque de texto en tu tablero:
        *   ¿Cómo el uso de eventos de dominio en tu diseño promueve el desacoplamiento entre los contextos de `Logística` y `Facturación`?
        *   Para tu microservicio de `Pedidos`, ¿usarías una estrategia de CQRS/ES puro o CRUD+ES? Justifica brevemente tu elección.
        *   En tu diagrama de flujo de escritura, ¿qué rol cumple el `Event Store` y el `Message Broker`?

### Criterios de Evaluación

Tu tablero de Miro será evaluado con base en la claridad, coherencia y correcta aplicación de los conceptos de la semana.

*   **Análisis de Dominio y DDD (40%)**
    *   **Calidad del Lenguaje Ubicuo:** El glosario es preciso y refleja fielmente la entrevista.
    *   **Coherencia del Modelo:** Los eventos, contextos y el mapa de contextos son lógicos y están bien justificados a partir del caso de estudio.

*   **Diseño Técnico y Comprensión de NebulaE (50%)**
    *   **Alineación de Componentes:** La traducción de contextos a microservicios y agregados es coherente.
    *   **Calidad de los Contratos:** Los comandos, eventos (con versión) y queries están bien definidos y siguen las convenciones.
    *   **Claridad de los Flujos de Datos:** Los diagramas de lectura y escritura demuestran una clara comprensión de la arquitectura CQRS y las responsabilidades de cada capa (`frontend`, `api`, `backend`, `playground`).
    *   **Profundidad de la Justificación:** Las respuestas a las preguntas de arquitectura son claras y demuestran un entendimiento de los principios del framework.

*   **Presentación y Claridad (10%)**
    *   El tablero de Miro está limpio, bien organizado y es fácil de navegar y entender.
