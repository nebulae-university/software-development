# Plan de Estudios Detallado: Semana 2

## Objetivo de la Semana

Al finalizar esta semana, el desarrollador será capaz de **construir y modelar la lógica de negocio de un microservicio funcional**. Habrá pasado de la teoría a la práctica, implementando:

1.  **Patrones Tácticos de DDD:** Modelar Agregados, Entidades y Objetos de Valor en el código.
2.  **Implementación Backend Completa:** Desarrollar la lógica de negocio para una entidad, incluyendo comandos y la conexión con la API de GraphQL.
3.  **Programación Reactiva (RxJS):** Comprender y utilizar los fundamentos de RxJS para manejar flujos de datos asíncronos.
4.  **Formularios y UI Avanzada:** Crear formularios robustos con Material UI, Formik y Yup para la validación.
5.  **Persistencia de Datos (CRUD):** Realizar operaciones de Crear, Leer, Actualizar y Eliminar en MongoDB.
6.  **Contenerización:** Empaquetar y ejecutar el entorno de desarrollo local utilizando Docker y Docker Compose.

Esta semana es fundamentalmente práctica y se enfoca en la **implementación de una funcionalidad de negocio completa**, desde la base de datos hasta la interfaz de usuario.

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
| **1** | Patrones Tácticos de DDD: Agregados y Entidades | Modificación básica FullStack de un µServicio | Fundamentos de RxJS: Observable, Observer, Subscription | Estilizado con Material UI | Operaciones CRUD: Insertar y Encontrar | Fundamentos de Docker y gestión de contenedores |
| **2** | Aislamiento de Datos: Base de Datos por Servicio | Implementación de Lógica de Comandos (Backend) | Creación de Streams y Hot vs Cold Observables | Estilizado con Tailwind CSS | Operaciones CRUD: Reemplazar y Eliminar | Creación de Imágenes con Dockerfile |
| **3** | - | Conexión API GraphQL con Backend | Subjects en RxJS y utilidad en Node.js | Formularios con Formik | Operaciones CRUD desde Node.js | Fundamentos de Docker Compose |
| **4** | - | Generación de Nueva Vista FrontEnd | Operadores de utilidad: `tap`, `delay`, `timeout` | Validación de formularios con Yup | Introducción al Modelado de Datos en MongoDB | Redes y Volúmenes en Docker Compose |
| **5** | **Práctica Integral:** Diseño de un Agregado | **Práctica Integral:** Conexión Full-Stack | **Práctica Integral:** Creación de un flujo reactivo simple | **Práctica Integral:** Construcción de un formulario completo | **Práctica Integral:** Implementación de un CRUD completo | **Práctica Integral:** Orquestación del entorno con Docker Compose |

---

## Día 1: Modelado del Corazón del Servicio y Contenerización

### Introducción del Día

¡Bienvenido a la segunda semana! Hoy nos sumergimos en el corazón de un microservicio. El objetivo es que aprendas a modelar la lógica de negocio utilizando los patrones tácticos de DDD y a implementar las operaciones básicas de datos. Empezarás a modificar el microservicio que generaste, te introducirás en los fundamentos de la programación reactiva con RxJS y darás tus primeros pasos en la contenerización con Docker. Al final del día, habrás diseñado el núcleo de tu entidad de negocio y entendido cómo empaquetar tu aplicación para un despliegue consistente.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Patrones Tácticos de DDD (Path 1)
*   **Módulo 2:** Modificación Básica FullStack (Path 2)
*   **Módulo 3:** Fundamentos de RxJS (Path 3)
*   **Módulo 4:** Estilizado con Material UI (Path 4)
*   **Módulo 5:** Operaciones CRUD en MongoDB (Path 5)
*   **Módulo 6:** Fundamentos de Docker (Path 6)

### Módulo 1: Patrones Tácticos de DDD (Path 1)
*   **Objetivo:** Diseñar el interior de un microservicio, modelando su lógica de negocio con los patrones tácticos de DDD.
*   **Descripción:** Si la semana pasada definimos los límites de los servicios (diseño estratégico), esta semana construiremos su interior. Este módulo se centra en los **patrones tácticos de DDD**, que son los bloques de construcción de tu lógica de negocio.

    La guía de **Microsoft Docs** es tu recurso principal. Los conceptos clave que debes dominar son:
    1.  **Entidad:** Un objeto que no se define por sus atributos, sino por su continuidad e identidad a lo largo del tiempo (ej: un `Usuario` con un `ID` único).
    2.  **Objeto de Valor (Value Object):** Un objeto que describe una característica y se define por sus atributos. Es inmutable y no tiene identidad propia (ej: un objeto `Direccion` compuesto por calle, ciudad y código postal).
    3.  **Agregado (Aggregate):** Este es el concepto más importante. Un Agregado es un clúster de entidades y objetos de valor que se tratan como una única unidad para los cambios de datos. Define una **barrera transaccional**. El `Aggregate Root` es la única entidad del agregado a la que los objetos externos pueden hacer referencia.

    El video de **DDD Building Blocks** reforzará estos conceptos visualmente. Tu objetivo es empezar a pensar en tus entidades de negocio como Agregados. Para el caso del catering, el `Pedido` sería el `Aggregate Root`. Al final, deberías ser capaz de esbozar el Agregado `Pedido`, identificando qué debería ser una entidad y qué un objeto de valor dentro de él.
*   **Recursos Web:**
    *   [Identificando los bloques de construcción de DDD (Microsoft Docs)](https://docs.microsoft.com/es-es/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/microservice-domain-model) (2h)
*   **Videos:**
    *   [Video: DDD Building Blocks](https://www.youtube.com/watch?v=xFl-QQZJFTA) (18min)

### Módulo 2: Modificación Básica FullStack (Path 2)
*   **Objetivo:** Aprender a modificar una entidad de negocio en todo el stack de NebulaE.
*   **Descripción:** Es hora de poner en práctica la teoría. En este módulo, tomarás el microservicio que generaste y realizarás tu primera modificación completa, tocando todas las capas de la arquitectura.

    El video **"Modificación básica FullStack de un µServicio NebulaE"** es tu guía principal. Seguirás un tutorial práctico que te enseñará a:
    1.  **Identificar el código generado:** Localizar los archivos en el `frontend`, `api` y `backend` que corresponden a la entidad de negocio que creó el CLI.
    2.  **Realizar un cambio simple:** Modificarás un campo o añadirás uno nuevo. Esto implicará:
        *   Ajustar el esquema en la capa `api` (GraphQL).
        *   Modificar la lógica en el `backend` para manejar el nuevo campo.
        *   Actualizar el componente de React en el `frontend` para mostrar o editar el campo.
    3.  **Probar el flujo completo:** Levantarás el entorno de desarrollo local y verificarás que tu cambio se refleja desde la interfaz de usuario hasta la base de datos.

    El objetivo no es realizar un cambio complejo, sino entender el **flujo de desarrollo** y cómo las diferentes partes del microservicio están conectadas. Al final, habrás ganado la confianza para navegar por el código base y realizar cambios de forma autónoma.
*   **Videos:**
    *   [Modificación básica FullStack de un µServicio NebulaE](https://youtu.be/GC8qjgkX3F8)

### Módulo 3: Fundamentos de RxJS (Path 3)
*   **Objetivo:** Comprender los conceptos esenciales de la programación reactiva: `Observable`, `Observer` y `Subscription`.
*   **Descripción:** Este módulo te introduce a un nuevo paradigma: la **programación reactiva**. En lugar de pedir datos (pull), reaccionarás a los datos a medida que llegan (push). RxJS es la librería que usamos para esto, y es fundamental para manejar la comunicación asíncrona y los eventos en NebulaE.

    La **guía de inicio rápido de RxJS** y el **video recomendado** son cruciales. Los conceptos que debes internalizar son:
    1.  **Observable:** Representa un flujo (stream) de datos que puede emitir múltiples valores a lo largo del tiempo. Piensa en él como una cinta transportadora de datos.
    2.  **Observer:** Es un objeto con tres callbacks (`next`, `error`, `complete`) que sabe cómo reaccionar a los valores emitidos por el Observable.
    3.  **Subscription (Suscripción):** Es la ejecución de un Observable. Se crea cuando un Observer se suscribe a un Observable. La suscripción se puede cancelar para dejar de escuchar y liberar memoria.

    Tu objetivo es entender esta relación. Un Observable es la fuente de datos, el Observer es el consumidor, y la Suscripción es el vínculo que los une. Practica creando un observable simple y suscribiéndote a él. Al final, deberías poder explicar la diferencia entre una Promesa (que emite un solo valor) y un Observable (que puede emitir muchos).
*   **Recursos Web:**
    *   [Guía de Inicio Rápido de RxJS (rxjs.dev)](https://rxjs.dev/guide/overview) (1.5h)
*   **Videos:**
    *   [¿Qué es RxJS?](https://www.youtube.com/watch?v=PhggNGsSQyg)

### Módulo 4: Estilizado con Material UI (Path 4)
*   **Objetivo:** Aprender a utilizar la biblioteca de componentes Material UI para estilizar la aplicación.
*   **Descripción:** Una aplicación no solo debe ser funcional, sino también visualmente atractiva y consistente. En NebulaE, usamos **Material UI (MUI)** como nuestra biblioteca de componentes principal para lograr un diseño profesional basado en los principios de Material Design de Google.

    La **guía de inicio de Material UI** es tu punto de partida. El objetivo es que te familiarices con su ecosistema:
    1.  **Instalación y Configuración:** Aprende a añadir MUI a un proyecto de React.
    2.  **Componentes Pre-construidos:** Explora la vasta biblioteca de componentes que ofrece MUI: botones, inputs, tarjetas, menús, etc. Elige algunos y pruébalos en tu aplicación.
    3.  **Sistema de Estilizado (`sx` prop):** La forma moderna de estilizar componentes en MUI es a través de la prop `sx`. Aprende a usarla para aplicar estilos personalizados de manera concisa y potente, accediendo directamente a los tokens del tema (como colores primarios, espaciado, etc.).

    El **video del curso** te mostrará cómo integrar MUI en un proyecto real junto con Tailwind y Redux, dándote una visión más completa. Tu objetivo práctico es reemplazar algunos elementos HTML básicos de tu aplicación (como `<button>` o `<input>`) por sus equivalentes de Material UI (`<Button>`, `<TextField>`), y aplicarles algunos estilos básicos con la prop `sx`.
*   **Recursos Web:**
    *   [Introducción a Material UI (MUI.com)](https://mui.com/material-ui/getting-started/overview/) (1.5h)
*   **Videos:**
    *   [React Material UI Tutorial](https://www.youtube.com/playlist?list=PLC3y8-rFHvwh-K9mDlrrcDywl7CeVL2rO)

### Módulo 5: Operaciones CRUD en MongoDB (Path 5)
*   **Objetivo:** Dominar las operaciones de inserción y búsqueda de documentos en MongoDB.
*   **Descripción:** Este módulo profundiza en las operaciones de datos, centrándose en las dos primeras letras de CRUD: Crear y Leer (Create, Read). Dominar la inserción y, sobre todo, la búsqueda eficiente de datos es fundamental para cualquier aplicación.

    El curso de **MongoDB University** es tu guía. Las operaciones clave que practicarás (tanto en la shell como desde Node.js) son:
    1.  **Inserción de Documentos:**
        *   `insertOne()`: Para insertar un único documento.
        *   `insertMany()`: Para insertar múltiples documentos a la vez, lo cual es mucho más eficiente.
    2.  **Búsqueda de Documentos (`find`):**
        *   **Filtros de Consulta:** Aprenderás a pasar un documento como filtro a `find()` para especificar qué documentos quieres. (Ej: `db.collection.find({ status: "activo" })`).
        *   **Operadores de Consulta:** Irás más allá de la igualdad simple y usarás operadores como `$gt` (mayor que), `$lt` (menor que), `$in` (el valor está en un array), etc.
        *   **Proyecciones:** Aprenderás a usar el segundo argumento de `find()` para especificar qué campos del documento quieres que te devuelva la consulta, optimizando el uso de la red.

    Tu objetivo es sentirte cómodo construyendo consultas complejas para obtener exactamente los datos que necesitas. Al final, deberías ser capaz de insertar datos en tu colección y luego escribir varias consultas diferentes para recuperarlos basándote en distintos criterios.
*   **Recursos Web:**
    *   [MongoDB CRUD Operations: Insert and Find Documents](https://learn.mongodb.com/courses/mongodb-crud-operations-insert-and-find-documents) (1.75h)
*   **Videos:** Material práctico de MongoDB University

### Módulo 6: Fundamentos de Docker (Path 6)
*   **Objetivo:** Comprender los conceptos fundamentales de Docker y la gestión de contenedores.
*   **Descripción:** Docker es la tecnología que nos permite empaquetar nuestras aplicaciones y sus dependencias en unidades portátiles y aisladas llamadas **contenedores**. Esto resuelve el clásico problema de "funciona en mi máquina". Este módulo te introduce a los conceptos básicos de Docker.

    La **documentación oficial de Docker** y el **video tutorial** son tus recursos. Los conceptos clave son:
    1.  **Imagen de Docker:** Es una plantilla de solo lectura que contiene las instrucciones para crear un contenedor. Incluye el código, un sistema operativo base, librerías y dependencias.
    2.  **Contenedor de Docker:** Es una instancia en ejecución de una imagen. Es un entorno ligero, aislado y ejecutable. Puedes iniciar, detener, mover y eliminar contenedores.
    3.  **Dockerfile:** Es un archivo de texto que contiene los comandos para construir una imagen de Docker. Es la "receta" de tu imagen.

    Tu tarea práctica es empezar a interactuar con Docker desde la línea de comandos. Aprende los comandos básicos:
    *   `docker pull <imagen>`: Descarga una imagen de un registro (como Docker Hub).
    *   `docker images`: Lista las imágenes en tu máquina.
    *   `docker run <imagen>`: Crea y ejecuta un contenedor a partir de una imagen.
    *   `docker ps`: Lista los contenedores en ejecución.

    Al final, deberías ser capaz de descargar una imagen pública (como la de `nginx`) y ejecutarla como un contenedor en tu máquina.
*   **Recursos Web:**
    *   [Introducción a Docker – Docker Docs ES](https://docs.docker.com/get-started/overview/?lang=es)
*   **Videos:**
    *   [Docker Tutorial for Beginners – TechWorld](https://www.youtube.com/watch?v=3c-iBn73dDE) (2021)

---

## Día 2: Construcción del Backend y Aislamiento de Datos

### Introducción del Día

Hoy nos enfocamos en la construcción del "write-side" de nuestra arquitectura. El objetivo es que implementes la lógica de negocio principal en el backend, aprendas a aislar los datos de tu servicio y profundices en la creación de flujos de datos con RxJS. También te familiarizarás con la creación de tus propias imágenes de Docker. Al final del día, tendrás un backend que puede procesar comandos y habrás dado un paso crucial hacia la autonomía de tus microservicios.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Aislamiento de Datos (Path 1)
*   **Módulo 2:** Implementación de Lógica de Comandos (Path 2)
*   **Módulo 3:** Creación de Streams y Hot vs Cold Observables (Path 3)
*   **Módulo 4:** Estilizado con Tailwind CSS (Path 4)
*   **Módulo 5:** Operaciones CRUD de Modificación (Path 5)
*   **Módulo 6:** Creación de Imágenes con Dockerfile (Path 6)

### Módulo 1: Aislamiento de Datos (Path 1)
*   **Objetivo:** Garantizar la encapsulación y persistencia de los datos de un microservicio.
*   **Descripción:** Este módulo aborda uno de los principios más importantes de la arquitectura de microservicios: la autonomía de los datos. El objetivo es que internalices por qué cada microservicio debe ser el dueño exclusivo de su propia base de datos.

    El recurso principal es el artículo de **microservices.io sobre el patrón "Base de Datos por Servicio"**. Los puntos clave que debes entender son:
    1.  **Bajo Acoplamiento:** Si los servicios comparten una base de datos, cualquier cambio en el esquema puede romper múltiples servicios. Esto crea un acoplamiento fuerte y ralentiza el desarrollo.
    2.  **Autonomía del Equipo:** El equipo dueño de un servicio debe poder elegir la tecnología de base de datos que mejor se adapte a las necesidades de ese servicio (ej: MongoDB para datos de documentos, Redis para caché, etc.).
    3.  **Encapsulación:** La base de datos es un detalle de implementación del servicio. Otros servicios no deben acceder a ella directamente; deben hacerlo a través de la API del servicio dueño.

    El video de **Nick Tune sobre "Dissecting Bounded Contexts"** complementa esto, mostrando cómo diferentes tipos de contextos de negocio pueden tener diferentes necesidades de persistencia y cómo los patrones de relación entre contextos (como `Shared Kernel` o `Anti-Corruption Layer`) ayudan a gestionar las dependencias de datos de manera controlada.

    Al final, deberías poder explicar con firmeza por qué compartir una base de datos entre microservicios es un anti-patrón y cómo el patrón "Base de Datos por Servicio" promueve la escalabilidad y la agilidad.
*   **Recursos Web:**
    *   [Patrón: Base de Datos por Servicio (microservices.io)](https://microservices.io/patterns/data/database-per-service.html) (1h)
*   **Videos:**
    *   [Video: Dissecting Bounded Contexts (Nick Tune)](https://www.youtube.com/watch?v=zkRfDw0N4W8) (1h)

### Módulo 2: Implementación de Lógica de Comandos (Path 2)
*   **Objetivo:** Implementar la lógica de negocio para los comandos en la capa `backend`.
*   **Descripción:** Ahora que has diseñado tu Agregado, es hora de implementar la lógica que lo modifica. En la arquitectura CQRS, esto se hace a través de **Comandos**. Un comando es una solicitud para realizar una acción que cambia el estado del sistema (ej: `CrearPedido`, `ActualizarDireccionPedido`).

    El video **"Implementación de Lógica de Comandos en el Backend"** es tu guía práctica. Aprenderás a:
    1.  **Localizar el manejador de comandos (Command Handler):** Encontrarás el archivo en la capa `backend` que recibe los comandos de la API.
    2.  **Implementar la lógica de negocio:** Dentro del manejador, escribirás la lógica para:
        *   Validar el comando.
        *   Cargar el estado actual del Agregado (si existe).
        *   Tomar una decisión de negocio.
        *   Generar y persistir uno o más Eventos de Dominio (ej: `PedidoCreado`).
    3.  **Uso de RxJS:** Verás cómo usamos flujos de RxJS para orquestar estas operaciones asíncronas de manera declarativa.

    El objetivo es que te sientas cómodo escribiendo la lógica de negocio principal de tu servicio. Al final, habrás implementado la lógica para un comando de creación o actualización, sentando las bases para el "write-side" de tu microservicio.
*   **Videos:**
    *   [Implementación de Lógica de Comandos en el Backend](https://www.youtube.com/watch?v=dummy_video) (2.5h)

### Módulo 3: Creación de Streams y Hot vs Cold Observables (Path 3)
*   **Objetivo:** Aprender a crear flujos de datos desde diversas fuentes y entender la diferencia entre observables "fríos" y "calientes".
*   **Descripción:** Este módulo profundiza en RxJS, centrándose en cómo se crean los Observables y en un concepto crucial: la diferencia entre "frío" y "caliente".

    La guía de **LearnRxJS sobre operadores de creación** te mostrará las diferentes formas de crear un stream:
    *   `of()`: Crea un observable a partir de una secuencia de valores.
    *   `from()`: Convierte un array, una promesa o un iterable en un observable.
    *   `interval()` y `timer()`: Crean observables que emiten valores en intervalos de tiempo.

    Luego, el video de **Academind sobre "Hot vs Cold Observables"** aborda un concepto clave:
    1.  **Cold Observables (Fríos):** Son observables que no empiezan a emitir valores hasta que un observer se suscribe. Cada suscripción desencadena una nueva ejecución independiente. La mayoría de los observables que creas son fríos por defecto.
    2.  **Hot Observables (Calientes):** Son observables que emiten valores independientemente de si hay suscriptores o no. Todos los suscriptores reciben los mismos valores emitidos después de que se suscriben. Piensa en los eventos del DOM (como los clics del ratón) como un observable caliente.

    Entender esta diferencia es vital para evitar comportamientos inesperados y gestionar los recursos correctamente. Tu objetivo es practicar la creación de observables desde diferentes fuentes y poder explicar cuándo un observable es frío o caliente y por qué es importante.
*   **Recursos Web:**
    *   [Operadores de Creación (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/creation) (2h)
*   **Videos:**
    *   [Hot vs Cold Observables (Academind)](https://www.youtube.com/watch?v=zfQoleQEa4w) (1h)
    *   [Videos de Operadores de Creación](https://www.youtube.com/watch?v=BgHphtY8IPE), [Video 2](https://www.youtube.com/watch?v=xYiafdImxU8), [Video 3](https://www.youtube.com/watch?v=Niwo4bY1CU4)

### Módulo 4: Estilizado con Tailwind CSS (Path 4)
*   **Objetivo:** Aprender a utilizar el framework CSS utility-first Tailwind CSS.
*   **Descripción:** Además de Material UI para componentes complejos, en NebulaE usamos **Tailwind CSS** para un estilizado rápido y personalizado a nivel de utilidad. Tailwind es un framework "utility-first", lo que significa que en lugar de darte componentes pre-hechos, te da clases de bajo nivel que puedes componer para construir diseños únicos.

    La **guía de Tailwind CSS** es tu recurso principal. Los conceptos que debes aprender son:
    1.  **Clases de Utilidad:** En lugar de escribir CSS personalizado, aplicarás clases directamente en tu HTML/JSX. (Ej: `<div class="bg-blue-500 text-white p-4">`).
    2.  **Diseño Responsivo:** Aprende a usar los prefijos de breakpoint (como `md:` o `lg:`) para aplicar diferentes estilos en diferentes tamaños de pantalla. (Ej: `class="w-1/2 md:w-1/3"`).
    3.  **Composición:** El poder de Tailwind reside en combinar estas pequeñas clases para crear diseños complejos sin salir de tu archivo de marcado.

    Tu objetivo es familiarizarte con la sintaxis de Tailwind y empezar a usarla para ajustes de layout, espaciado, colores y tipografía. Intenta refactorizar una pequeña parte de tu UI para que use clases de Tailwind en lugar de estilos en línea o archivos CSS separados.
*   **Recursos Web:**
    *   [Guía de Tailwind CSS (Tailwindcss.com)](https://tailwindcss.com/docs) (1.5h)
*   **Videos:**
    *   [Curso React con Tailwind, Redux y MUI](https://www.youtube.com/watch?v=LdomMuzp6jM)

### Módulo 5: Operaciones CRUD de Modificación (Path 5)
*   **Objetivo:** Dominar las operaciones de actualización y eliminación de documentos en MongoDB.
*   **Descripción:** Completamos el acrónimo CRUD con las operaciones de Actualizar y Eliminar (Update, Delete). Este módulo se centra en cómo modificar y borrar datos de forma segura y eficiente en MongoDB.

    El curso de **MongoDB University** te guiará a través de las operaciones clave:
    1.  **Reemplazo de Documentos (`replaceOne`):** Aprenderás a reemplazar un documento completo por uno nuevo. Esto es útil cuando quieres cambiar toda la estructura del documento.
    2.  **Actualización de Documentos (`updateOne`, `updateMany`):** Esta es la forma más común de modificar datos. No reemplazas todo el documento, sino que usas **operadores de actualización** para modificar campos específicos. Debes dominar operadores como:
        *   `$set`: Establece el valor de un campo.
        *   `$unset`: Elimina un campo.
        *   `$inc`: Incrementa el valor de un campo numérico.
        *   `$push`: Añade un elemento a un array.
    3.  **Eliminación de Documentos (`deleteOne`, `deleteMany`):** Aprenderás a eliminar documentos basándote en un filtro de consulta.

    Tu objetivo es practicar estas operaciones de modificación. Presta especial atención a la diferencia entre `replaceOne` y `updateOne`. Al final, deberías ser capaz de escribir consultas para modificar campos específicos de tus documentos y eliminarlos de forma segura.
*   **Recursos Web:**
    *   [MongoDB CRUD Operations: Replace and Delete Documents](https://learn.mongodb.com/courses/mongodb-crud-operations-replace-and-delete-documents) (1.75h)
*   **Videos:** Material práctico de MongoDB University

### Módulo 6: Creación de Imágenes con Dockerfile (Path 6)
*   **Objetivo:** Aprender a escribir un Dockerfile para crear imágenes de Docker personalizadas.
*   **Descripción:** Mientras que `docker pull` es útil para usar imágenes existentes, el verdadero poder de Docker reside en crear tus propias imágenes para tus aplicaciones. Esto se hace con un archivo de texto llamado **Dockerfile**.

    La **referencia del Dockerfile** en la documentación oficial es tu guía. Las instrucciones clave que debes aprender son:
    *   `FROM`: Especifica la imagen base sobre la que construirás la tuya (ej: `FROM node:18-alpine`).
    *   `WORKDIR`: Establece el directorio de trabajo dentro del contenedor.
    *   `COPY`: Copia archivos desde tu máquina local al contenedor (ej: `COPY package.json .`).
    *   `RUN`: Ejecuta un comando durante el proceso de construcción de la imagen (ej: `RUN npm install`).
    *   `CMD`: Especifica el comando por defecto que se ejecutará cuando se inicie un contenedor a partir de la imagen (ej: `CMD ["node", "server.js"]`).
    *   `EXPOSE`: Informa a Docker que el contenedor escucha en un puerto de red específico.

    Tu tarea es analizar el Dockerfile que se generó en tu microservicio. Identifica cada una de estas instrucciones y entiende su propósito. Luego, usa el comando `docker build -t mi-app .` para construir una imagen a partir de ese Dockerfile. Al final, deberías ser capaz de explicar el propósito de cada línea en un Dockerfile y construir una imagen personalizada para tu aplicación.
*   **Recursos Web:**
    *   [Referencia de Dockerfile – Docker Docs](https://docs.docker.com/engine/reference/builder/)
*   **Videos:**
    *   [Docker Tutorial for Beginners – TechWorld](https://www.youtube.com/watch?v=3c-iBn73dDE) (2021)

---

## Día 3: Conexión de Capas y Formularios

### Introducción del Día

Hoy es un día de conexiones. El objetivo es que enlaces la capa de API con el backend y empieces a construir los formularios en el frontend que permitirán a los usuarios interactuar con tu lógica de negocio. Profundizarás en conceptos más avanzados de RxJS, como los Subjects, y aprenderás a realizar operaciones CRUD desde tu aplicación Node.js. Además, darás el salto de gestionar contenedores individuales a orquestar una aplicación completa con Docker Compose. Al final del día, tendrás un flujo de datos más completo, desde la API hasta el backend, y una forma de capturar la entrada del usuario.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Conexión API GraphQL con Backend (Path 2)
*   **Módulo 2:** Subjects en RxJS y Utilidad en Node.js (Path 3)
*   **Módulo 3:** Formularios con Formik (Path 4)
*   **Módulo 4:** Operaciones CRUD desde Node.js (Path 5)
*   **Módulo 5:** Fundamentos de Docker Compose (Path 6)

### Módulo 1: Conexión API GraphQL con Backend (Path 2)
*   **Objetivo:** Entender cómo conectar las operaciones de GraphQL con el backend.
*   **Descripción:** La capa `api` de tu microservicio actúa como la puerta de entrada. En este módulo, aprenderás cómo esta capa (que usa GraphQL) se comunica con la capa `backend` para ejecutar la lógica de negocio.

    El video **"Conexión API GraphQL con FrontEnd y Backend"** es tu guía principal. Los conceptos clave a entender son:
    1.  **Resolvers de GraphQL:** Un resolver es una función que "resuelve" un valor para un campo en tu esquema de GraphQL. Para las mutaciones (operaciones de escritura), el resolver es el puente hacia tu lógica de negocio.
    2.  **Invocación de Comandos:** Dentro del resolver de una mutación, verás cómo se construye y se envía un **Comando** a la capa `backend`. La capa `api` no contiene lógica de negocio; su responsabilidad es traducir una petición de GraphQL en un comando y despacharlo.
    3.  **Flujo de Datos:** Trazarás el camino de una petición desde que llega al endpoint de GraphQL, es manejada por el resolver apropiado, se convierte en un comando, y se envía al backend para su procesamiento.

    Tu objetivo es entender este patrón de delegación. La API define el "qué" (las operaciones disponibles), y el backend implementa el "cómo" (la lógica de negocio real). Al final, deberías poder explicar cómo una mutación de GraphQL desencadena la ejecución de un comando en el backend de tu microservicio.
*   **Videos:**
    *   [Conexión API GraphQL con FrontEnd y Backend](https://www.youtube.com/watch?v=dummy_video) (1.5h)

### Módulo 2: Subjects en RxJS y Utilidad en Node.js (Path 3)
*   **Objetivo:** Comprender el uso de Subjects y la relevancia de RxJS en el backend.
*   **Descripción:** Este módulo introduce un tipo especial de Observable llamado **Subject**. Además, justifica por qué usamos un paradigma reactivo como RxJS en un entorno de backend.

    Primero, la guía de **LearnRxJS sobre Subjects** y los **videos recomendados** te enseñarán que un Subject es tanto un Observable como un Observer. Esto significa que puede emitir valores, pero también puedes enviarle valores manualmente usando su método `.next()`. Los Subjects son la forma más común de crear observables "calientes" y son útiles para emitir eventos dentro de tu aplicación.

    Luego, el artículo de **dev.to sobre "Por qué usar RxJS en Node.js"** te dará el contexto de negocio. Las razones clave son:
    *   **Manejo de Concurrencia:** En un microservicio, muchas cosas pueden estar sucediendo a la vez (peticiones de API, eventos de mensajes, etc.). RxJS nos da herramientas poderosas para orquestar estos flujos de eventos concurrentes de una manera mucho más limpia que con callbacks o promesas anidadas.
    *   **Código Declarativo:** Como ya has visto, RxJS promueve un estilo de código declarativo que es más fácil de leer y razonar, especialmente para lógicas de negocio complejas.

    Tu objetivo es entender que los Subjects son una herramienta para la comunicación basada en eventos dentro de tu aplicación, y que RxJS en su conjunto es nuestra elección estratégica para manejar la complejidad asíncrona inherente a los microservicios.
*   **Recursos Web:**
    *   [Subjects en RxJS (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/subjects) (1h)
    *   [¿Por qué usar RxJS en el Backend de Node.js? (dev.to)](https://dev.to/this-is-learning/why-use-rxjs-in-node-js-backend-5eh1) (1h)
*   **Videos:**
    *   [Subjects en RxJS](https://www.youtube.com/watch?v=rdK92pf3abs), [Video 2](https://www.youtube.com/watch?v=s1oV2FMK1jc)
    *   [Aplicación práctica en JS](https://www.youtube.com/watch?v=j6fY0QjLSYo)

### Módulo 3: Formularios con Formik (Path 4)
*   **Objetivo:** Aprender a construir formularios en React utilizando la librería Formik.
*   **Descripción:** Los formularios son una parte fundamental de casi cualquier aplicación web. Manejar su estado (valores, errores, estado de envío) puede ser complicado. **Formik** es una librería que simplifica enormemente la creación de formularios en React.

    El **tutorial oficial de Formik** es tu recurso principal. Los conceptos que debes dominar son:
    1.  **Componente `<Formik>`:** Es el componente principal que envuelve tu formulario. Se encarga de gestionar todo el estado del formulario.
    2.  **Componentes `<Form>` y `<Field>`:** Formik proporciona estos componentes que se conectan automáticamente al estado de Formik, reduciendo la cantidad de código que tienes que escribir.
    3.  **Manejo de Estado:** Formik te da acceso a los valores del formulario, los errores de validación, y si el formulario está siendo enviado, todo ello sin que tengas que manejarlo manualmente con `useState`.
    4.  **Manejo de Envío (`onSubmit`):** Le pasas una función `onSubmit` a Formik que será llamada con los valores del formulario cuando este se envíe y sea válido.

    El video sobre **"Formularios con Material UI y Formik"** te mostrará cómo integrar los componentes de Formik con los componentes de UI de Material UI para crear formularios que se vean bien y funcionen de manera robusta. Tu objetivo es construir tu primer formulario con Formik para capturar los datos de tu entidad de negocio.
*   **Recursos Web:**
    *   [Formik: Construyendo Formularios en React (Formik.org)](https://formik.org/docs/overview) (2h)
*   **Videos:**
    *   [Formularios con Material UI y Formik](https://www.youtube.com/watch?v=MV9NC3FoCmM)

### Módulo 4: Operaciones CRUD desde Node.js (Path 5)
*   **Objetivo:** Implementar las operaciones CRUD completas en una aplicación Node.js.
*   **Descripción:** Este módulo es la culminación de tu aprendizaje sobre MongoDB esta semana. El objetivo es que apliques todo lo que has aprendido sobre operaciones CRUD y lo implementes dentro de tu aplicación de Node.js.

    El curso de **MongoDB University** te guiará en la creación de una capa de acceso a datos simple. Las tareas son:
    1.  **Estructurar el Código:** Organizarás tu código de Node.js para tener funciones separadas para cada operación CRUD (ej: `createDocument`, `findDocument`, `updateDocument`, `deleteDocument`).
    2.  **Implementar cada función:** Usando el driver de MongoDB y `async/await`, implementarás la lógica para cada una de estas funciones, asegurándote de que reciben los parámetros necesarios (como el filtro de consulta o los datos a insertar) y devuelven los resultados.
    3.  **Manejo de Errores:** Implementarás bloques `try/catch` para manejar posibles errores de la base de datos de manera elegante.

    Esta práctica es crucial porque el código que escribas aquí es muy similar a lo que harás en la capa de persistencia de tu microservicio. Al final, tendrás un módulo de Node.js reutilizable que encapsula toda la lógica para interactuar con una colección de tu base de datos.
*   **Recursos Web:**
    *   [MongoDB CRUD Operations in Node.js](https://learn.mongodb.com/courses/mongodb-crud-operations-in-nodejs) (2h)
*   **Videos:** Material práctico de MongoDB University

### Módulo 5: Fundamentos de Docker Compose (Path 6)
*   **Objetivo:** Aprender a orquestar aplicaciones multi-servicio con Docker Compose.
*   **Descripción:** Mientras que Docker es genial para gestionar contenedores individuales, las aplicaciones reales suelen estar compuestas por múltiples servicios que necesitan comunicarse entre sí (ej: tu microservicio, una base de datos, un message broker). **Docker Compose** es la herramienta para definir y ejecutar aplicaciones Docker multi-contenedor.

    La **documentación oficial** y el **video introductorio** son tus guías. El concepto clave es el archivo `docker-compose.yml`. Este archivo YAML te permite configurar los servicios de tu aplicación:
    *   **`services`:** Aquí defines cada uno de los contenedores que forman tu aplicación (ej: `api`, `db`).
    *   **`image` o `build`:** Para cada servicio, especificas la imagen a usar o el path al Dockerfile para construirla.
    *   **`ports`:** Mapeas los puertos del contenedor a los puertos de tu máquina local.
    *   **`volumes`:** Montas directorios de tu máquina local dentro del contenedor para persistir datos o reflejar cambios en el código al instante.
    *   **`networks`:** Defines redes personalizadas para que tus contenedores puedan comunicarse entre sí.

    Tu tarea es analizar el archivo `docker-compose.yml` que se encuentra en el `integrated-local-environment`. Identifica los diferentes servicios que define y cómo están configurados. Luego, aprende los comandos básicos: `docker-compose up` para iniciar toda la aplicación y `docker-compose down` para detenerla. Al final, entenderás cómo Docker Compose nos permite levantar un entorno de desarrollo complejo y realista con un solo comando.
*   **Recursos Web:**
    *   [Docker Compose – Docker Docs](https://docs.docker.com/compose/)
*   **Videos:**
    *   [Docker Compose in 12 Minutes](https://www.youtube.com/watch?v=HG6yIjZapSA) (2022)

---

## Día 4: Vistas, Validación y Orquestación Avanzada

### Introducción del Día

Hoy nos centramos en mejorar la interacción con el usuario y la robustez de nuestro sistema. El objetivo es que generes las vistas en el frontend para mostrar los datos de tu entidad, implementes validaciones a prueba de errores en tus formularios y profundices en el modelado de datos en MongoDB. Además, aprenderás a manejar la comunicación entre contenedores y la persistencia de datos en Docker Compose. Al final del día, tendrás una aplicación más completa, con una interfaz de usuario funcional y validaciones que aseguran la calidad de los datos.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Generación de Nueva Vista FrontEnd (Path 2)
*   **Módulo 2:** Operadores de Utilidad en RxJS (Path 3)
*   **Módulo 3:** Validación de Formularios con Yup (Path 4)
*   **Módulo 4:** Introducción al Modelado de Datos en MongoDB (Path 5)
*   **Módulo 5:** Redes y Volúmenes en Docker Compose (Path 6)

### Módulo 1: Generación de Nueva Vista FrontEnd (Path 2)
*   **Objetivo:** Entender cómo conectar las operaciones de GraphQL con el backend para crear vistas.
*   **Descripción:** Si en el módulo anterior conectaste las mutaciones (escritura), ahora te centrarás en las **queries** (lectura). El objetivo es que aprendas a crear los componentes de React necesarios para consultar datos a través de la API de GraphQL y mostrarlos al usuario.

    El video **"Generación de Nueva Vista FrontEnd"** te guiará a través del proceso:
    1.  **Definición de la Query:** Verás cómo se define una query en el esquema de GraphQL de la capa `api` para obtener los datos que necesitas.
    2.  **Implementación del Resolver:** Aprenderás cómo el resolver de esta query lee de la vista materializada (la colección de solo lectura en MongoDB) para obtener los datos de manera eficiente.
    3.  **Consumo desde el Frontend:** En la capa `frontend`, usarás una librería como Apollo Client para ejecutar la query de GraphQL. Aprenderás a manejar los diferentes estados de la petición (cargando, error, éxito).
    4.  **Renderizado de Datos:** Una vez que los datos se reciben, los guardarás en el estado del componente y los renderizarás en la UI, por ejemplo, en una tabla o una lista.

    Tu objetivo es entender el flujo de datos del "read-side" de la arquitectura CQRS. Al final, serás capaz de crear un nuevo componente de React que consulte y muestre la información de tu entidad de negocio.
*   **Videos:**
    *   [Generación de Nueva Vista FrontEnd](https://www.youtube.com/watch?v=dummy_video) (1.5h)

### Módulo 2: Operadores de Utilidad en RxJS (Path 3)
*   **Objetivo:** Aprender a usar operadores de utilidad para depuración y control de flujos.
*   **Descripción:** Este módulo te introduce a un conjunto de operadores de RxJS que, aunque no transforman los datos directamente, son increíblemente útiles para la depuración, el control del tiempo y la interacción con el mundo exterior.

    Las guías de **LearnRxJS** te enseñarán sobre:
    *   **`tap`:** Este es el operador de depuración por excelencia. Te permite "espiar" los valores que pasan por un stream sin modificarlos. Es perfecto para añadir `console.log` en medio de una cadena de operadores y ver qué está pasando.
    *   **`delay`:** Retrasa la emisión de valores de un observable por un tiempo determinado. Útil para simular latencia de red o para animaciones.
    *   **`timeout`:** Emite un error si el observable no emite ningún valor en un período de tiempo especificado. Esencial para evitar que las peticiones se queden colgadas indefinidamente.
    *   **`toPromise` (deprecado):** Aunque está deprecado en favor de `firstValueFrom` y `lastValueFrom`, es importante que entiendas su propósito: convertir un observable en una promesa. Esto es útil para interactuar con código más antiguo que espera promesas en lugar de observables.

    Tu objetivo es añadir estos operadores a tus flujos de RxJS. Usa `tap` para depurar, `delay` para simular una carga lenta, y `timeout` para hacer tus flujos más robustos.
*   **Recursos Web:**
    *   [Operador `tap` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/tap) (1h)
    *   [Operador `delay` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/delay) (0.5h)
    *   [Operador `timeout` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/timeout) (0.5h)
    *   [Operador `toPromise` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/topromise) (0.5h)
*   **Videos:**
    *   [Videos de `tap`](https://www.youtube.com/watch?v=2N9KA6UHjmw), [Video 2](https://www.youtube.com/watch?v=HcwPyzD4LXQ)
    *   [Videos de `delay`](https://www.youtube.com/watch?v=fzijXza_660), [Video 2](https://www.youtube.com/watch?v=tVVAvVd61zo)
    *   [Video de `timeout`](https://www.youtube.com/watch?v=Xi9w4GmbidM)
    *   [Video de `toPromise` (alternativas)](https://www.youtube.com/live/3aeK5SfWBSU)

### Módulo 3: Validación de Formularios con Yup (Path 4)
*   **Objetivo:** Aprender a definir esquemas de validación de datos con Yup.
*   **Descripción:** Un formulario sin validación es una fuente de datos sucios y errores. Para asegurar la integridad de los datos que capturamos, usamos **Yup**, una librería para la construcción y validación de esquemas de objetos. Yup se integra perfectamente con Formik.

    La **documentación de Yup en GitHub** y el **video de validación** son tus recursos. El proceso es el siguiente:
    1.  **Definir un Esquema:** Creas un objeto de esquema usando los constructores de Yup (ej: `yup.object()`).
    2.  **Definir la Forma (`shape`):** Dentro del esquema, defines una "forma" que coincide con los campos de tu formulario.
    3.  **Añadir Validaciones:** Para cada campo, encadenas las reglas de validación que necesites. Yup ofrece una gran cantidad de validaciones pre-construidas:
        *   `yup.string()`: El campo debe ser un string.
        *   `.required()`: El campo no puede estar vacío.
        *   `.min(length)`: Longitud mínima para un string.
        *   `.email()`: Debe ser un formato de email válido.
        *   `.number()`: Debe ser un número.
    4.  **Integrar con Formik:** Pasas tu esquema de Yup a la prop `validationSchema` del componente `<Formik>`. Formik usará automáticamente este esquema para validar el formulario y poblar el objeto de errores.

    Tu objetivo es crear un esquema de validación con Yup para tu formulario y conectarlo a Formik. Al final, tu formulario debería mostrar mensajes de error específicos para cada campo cuando los datos introducidos no cumplan con las reglas.
*   **Recursos Web:**
    *   [Yup: Validación de Esquemas (GitHub)](https://github.com/jquense/yup) (1h)
*   **Videos:**
    *   [Validación de formularios con Yup](https://www.youtube.com/watch?v=RQ1E2EjyqY4)
    *   [Formularios con Material UI, Formik y Yup](https://www.youtube.com/watch?v=aeU2nU45sw4)

### Módulo 4: Introducción al Modelado de Datos en MongoDB (Path 5)
*   **Objetivo:** Aprender los principios del modelado de datos en MongoDB para diseñar schemas eficientes.
*   **Descripción:** El rendimiento de tu aplicación depende en gran medida de cómo modeles tus datos. A diferencia de SQL, donde la normalización es la norma, en MongoDB (y otras bases de datos NoSQL) tienes que tomar decisiones estratégicas sobre la estructura de tus documentos.

    El curso de **MongoDB University sobre Modelado de Datos** te introducirá a los conceptos fundamentales:
    1.  **Relaciones:** Entenderás cómo representar diferentes tipos de relaciones entre datos (uno a uno, uno a muchos, muchos a muchos) en un modelo de documentos.
    2.  **Embedding (Incrustar):** Aprenderás cuándo es apropiado incrustar sub-documentos o arrays de sub-documentos dentro de un documento principal. Esto es bueno para el rendimiento de lectura, ya que obtienes todos los datos en una sola consulta, pero puede llevar a documentos muy grandes.
    3.  **Referencing (Referenciar):** Aprenderás cuándo es mejor guardar solo el ID de un documento relacionado en otro, similar a una clave foránea. Esto mantiene los documentos más pequeños y evita la duplicación de datos, pero puede requerir consultas adicionales (`$lookup`) para unir los datos.

    La regla general es: **"los datos que se leen juntos, se guardan juntos"**. Tu objetivo es analizar tu entidad de negocio y decidir qué estrategia de modelado es la más apropiada. Para el `Pedido` del catering, ¿deberías incrustar los `ItemsDelMenu` o referenciarlos? Al final, deberías poder justificar tu decisión de modelado basándote en los patrones de acceso a los datos.
*   **Recursos Web:**
    *   [MongoDB Data Modeling Intro](https://learn.mongodb.com/courses/introduction-to-mongodb-data-modeling) (45min)
*   **Videos:** Material práctico de MongoDB University

### Módulo 5: Redes y Volúmenes en Docker Compose (Path 6)
*   **Objetivo:** Aprender a gestionar la comunicación y la persistencia de datos en Docker Compose.
*   **Descripción:** Para que una aplicación multi-contenedor sea útil, sus servicios necesitan comunicarse entre sí y sus datos deben persistir incluso si los contenedores se detienen. Este módulo se centra en dos características clave de Docker Compose: **redes** y **volúmenes**.

    La **documentación oficial** es tu guía:
    1.  **Redes (Networking):**
        *   Por defecto, Docker Compose crea una red única para todos los servicios definidos en tu archivo `docker-compose.yml`.
        *   Esto permite que los contenedores se descubran y se comuniquen entre sí utilizando el nombre del servicio como si fuera un hostname. Por ejemplo, tu contenedor `api` puede conectarse a tu contenedor de base de datos en la URL `mongodb://db:27017`.
        *   Aprende a definir redes personalizadas para aislar grupos de servicios.
    2.  **Volúmenes (Volumes):**
        *   Los contenedores son efímeros. Si un contenedor se detiene, cualquier dato escrito dentro de él se pierde. Los volúmenes son el mecanismo para persistir datos.
        *   **Bind Mounts:** Montan un directorio de tu máquina host directamente dentro del contenedor. Son geniales para el desarrollo, ya que cualquier cambio que hagas en tu código se refleja instantáneamente en el contenedor.
        *   **Named Volumes:** Son volúmenes gestionados por Docker. Son la forma preferida de persistir datos de bases de datos en producción.

    Tu tarea es volver a analizar tu archivo `docker-compose.yml` y identificar cómo se están utilizando las redes para la comunicación entre servicios y los volúmenes para persistir los datos de la base de datos y para el desarrollo en vivo del código.
*   **Recursos Web:**
    *   [Redes en Docker Compose](https://docs.docker.com/compose/networking/)
    *   [Volúmenes en Docker](https://docs.docker.com/storage/volumes/)
*   **Videos:**
    *   [Docker Compose in 12 Minutes](https://www.youtube.com/watch?v=HG6yIjZapSA) (2022)

---

## Día 5: Práctica Integral y Consolidación

### Introducción del Día

Llegamos al último día de la semana, un día para consolidar todo lo que has aprendido a través de una práctica integral. El objetivo es que conectes todas las piezas: diseñarás un Agregado de DDD, implementarás un flujo completo desde el frontend hasta el backend, construirás un formulario con validación robusta, y orquestarás todo el entorno con Docker Compose. Hoy es el día en que la teoría se convierte en una aplicación funcional y tangible. Se espera que al final del día te sientas con la confianza de poder construir una funcionalidad de negocio completa dentro del ecosistema de NebulaE.

Hoy te enfocarás en los siguientes módulos:
*   **Módulo 1:** Práctica Integral - Diseño de un Agregado (Path 1)
*   **Módulo 2:** Práctica Integral - Conexión Full-Stack (Path 2)
*   **Módulo 3:** Práctica Integral - Creación de un Flujo Reactivo (Path 3)
*   **Módulo 4:** Práctica Integral - Construcción de un Formulario Completo (Path 4)
*   **Módulo 5:** Práctica Integral - Implementación de un CRUD Completo (Path 5)
*   **Módulo 6:** Práctica Integral - Orquestación del Entorno (Path 6)

### Módulo 1: Práctica Integral - Diseño de un Agregado (Path 1)
*   **Objetivo:** Aplicar los patrones tácticos de DDD para diseñar un Agregado de negocio.
*   **Descripción:** En esta práctica, tomarás el caso de estudio del catering y diseñarás el Agregado `Pedido`.
    *   **Práctica Dirigida:**
        1.  Abre una herramienta de diagramación (como Miro o Excalidraw).
        2.  Dibuja el **Agregado `Pedido`** con su `Aggregate Root`.
        3.  Dentro del agregado, identifica qué propiedades deberían ser **Objetos de Valor** (ej: `DireccionEntrega`, `InformacionContacto`). Dibuja estos objetos y sus atributos.
        4.  Identifica si hay alguna **Entidad** hija dentro del agregado (ej: `ItemPedido`).
        5.  Define las **invariantes** del agregado (las reglas de negocio que siempre deben ser verdaderas). Por ejemplo: "El número de personas debe ser mayor que cero" o "La fecha de entrega no puede ser en el pasado".
    *   **Meta a lograr:** Tener un diagrama claro que represente el Agregado `Pedido`, sus componentes internos y las reglas que lo protegen. Este diagrama será la guía para tu implementación en el backend.

### Módulo 2: Práctica Integral - Conexión Full-Stack (Path 2)
*   **Objetivo:** Implementar un flujo de datos completo desde el frontend hasta el backend.
*   **Descripción:** Conectarás el formulario que creaste con la lógica de negocio del backend.
    *   **Práctica Dirigida:**
        1.  Asegúrate de que tienes una **mutación de GraphQL** en tu capa `api` para crear o actualizar tu entidad.
        2.  En el `onSubmit` de tu componente de formulario (Formik), utiliza Apollo Client para **ejecutar esa mutación**, pasando los valores del formulario como variables.
        3.  En el resolver de la mutación en la capa `api`, asegúrate de que se está **despachando el comando** correcto al backend.
        4.  En el manejador de comandos del `backend`, añade un `console.log` para verificar que el comando llega con los datos del formulario.
    *   **Meta a lograr:** Poder rellenar el formulario en la UI, hacer clic en enviar, y ver en la consola de tu servicio de backend que el comando ha sido recibido con los datos correctos.

### Módulo 3: Práctica Integral - Creación de un Flujo Reactivo (Path 3)
*   **Objetivo:** Aplicar tus conocimientos de RxJS para crear un flujo de datos simple.
*   **Descripción:** Refactorizarás una parte de tu lógica de backend para usar RxJS de manera más explícita.
    *   **Práctica Dirigida:**
        1.  Dentro de tu manejador de comandos en el `backend`, identifica la secuencia de operaciones (ej: validar, guardar en DB, publicar evento).
        2.  Crea un **flujo de RxJS** que modele esta secuencia. Puedes empezar con un `of(command)`.
        3.  Usa operadores como `mergeMap` para encadenar las operaciones asíncronas (como guardar en la base de datos).
        4.  Usa el operador `tap` para añadir `console.log` en cada paso del flujo y ver cómo los datos se transforman.
        5.  Asegúrate de manejar los errores con el operador `catchError`.
    *   **Meta a lograr:** Tener una lógica de comando en el backend que esté orquestada por un pipeline de RxJS, demostrando tu comprensión de cómo encadenar operadores para manejar flujos asíncronos.

### Módulo 4: Práctica Integral - Construcción de un Formulario Completo (Path 4)
*   **Objetivo:** Construir un formulario funcional y robusto con Material UI, Formik y Yup.
*   **Descripción:** Unirás todas las piezas del frontend para crear una experiencia de usuario completa para la creación de tu entidad.
    *   **Práctica Dirigida:**
        1.  Crea un nuevo componente de página en tu `frontend`.
        2.  En esta página, renderiza un formulario utilizando **Formik**.
        3.  Construye los campos del formulario utilizando componentes de **Material UI** (`<TextField>`, `<Select>`, etc.).
        4.  Crea un esquema de validación detallado con **Yup** que cubra todos los campos del formulario, incluyendo validaciones de tipo, requeridas y de formato.
        5.  Conecta el esquema de Yup a tu formulario de Formik.
        6.  Asegúrate de que los mensajes de error se muestren correctamente debajo de cada campo cuando la validación falla.
    *   **Meta a lograr:** Tener una página en tu aplicación con un formulario completo, visualmente atractivo, que valide la entrada del usuario en tiempo real y solo permita el envío cuando todos los datos son correctos.

### Módulo 5: Práctica Integral - Implementación de un CRUD Completo (Path 5)
*   **Objetivo:** Implementar y probar las cuatro operaciones CRUD desde tu aplicación Node.js.
*   **Descripción:** Crearás una pequeña aplicación de consola o un conjunto de scripts para interactuar con tu base de datos, demostrando tu dominio del driver de MongoDB.
    *   **Práctica Dirigida:**
        1.  Crea un nuevo archivo `test-db.js` en la raíz de tu proyecto.
        2.  En este archivo, importa el driver de MongoDB y establece la conexión a tu base de datos de Atlas.
        3.  Escribe y exporta cuatro funciones `async`: `createEntity`, `readEntity`, `updateEntity`, y `deleteEntity`.
        4.  Implementa cada función para que realice la operación CRUD correspondiente en tu colección.
        5.  Llama a estas funciones en secuencia para probar el ciclo de vida completo: crea una entidad, léela, actualízala y finalmente elimínala. Usa `console.log` para mostrar los resultados de cada paso.
    *   **Meta a lograr:** Poder ejecutar `node test-db.js` y ver en la consola la prueba exitosa de las cuatro operaciones CRUD contra tu base de datos en la nube.

### Módulo 6: Práctica Integral - Orquestación del Entorno (Path 6)
*   **Objetivo:** Utilizar Docker Compose para levantar y gestionar todo el entorno de desarrollo local.
*   **Descripción:** Aplicarás tus conocimientos de Docker Compose para gestionar la aplicación completa.
    *   **Práctica Dirigida:**
        1.  Navega al directorio que contiene tu archivo `docker-compose.yml` (`integrated-local-environment`).
        2.  Ejecuta `docker-compose up -d` para levantar todos los servicios en segundo plano.
        3.  Usa `docker-compose ps` para verificar que todos los contenedores (tu microservicio, la base de datos, etc.) están en ejecución.
        4.  Usa `docker-compose logs -f <nombre-del-servicio>` para ver los logs de tu microservicio en tiempo real.
        5.  Realiza una acción en el frontend (como enviar el formulario de tu práctica integral) y observa los logs del backend para ver la traza de la petición.
        6.  Cuando termines, usa `docker-compose down` para detener y eliminar todos los contenedores.
    *   **Meta a lograr:** Sentirte cómodo utilizando los comandos de Docker Compose para gestionar el ciclo de vida completo de tu entorno de desarrollo local, incluyendo la visualización de logs para la depuración.
