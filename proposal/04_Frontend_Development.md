# Path 4: Desarrollo Frontend con React

## Objetivo del Path

Este path cubre cómo construir interfaces de usuario modernas, eficientes y responsivas que se integran con nuestros microservicios. El objetivo es capacitar al desarrollador para construir componentes de React performantes y reutilizables, gestionar el estado de la aplicación de forma eficaz y aplicar nuestros estándares de UI/UX.

### Descripción General del Path

Este Path te sumerge en el arte y la ciencia de la **experiencia de usuario (UX)**. Aquí es donde el backend y la arquitectura se encuentran con el mundo real a través de una interfaz. El propósito de este camino es convertirte en un desarrollador frontend que no solo consume APIs, sino que construye aplicaciones web completas, interactivas y de alto rendimiento con React. Aprenderás a crear interfaces que sean intuitivas para los usuarios y mantenibles para los desarrolladores.

**¿Qué se espera de ti?**
Se espera que desarrolles un ojo para el detalle y una empatía por el usuario final. Deberás pensar en cómo fluyen los datos a través de la UI, cómo responde la aplicación a la interacción del usuario y cómo se siente su rendimiento. Este Path requiere una combinación de lógica para la gestión del estado y la comunicación con APIs, y de creatividad para la composición de componentes y el estilizado.

**¿Qué vas a aprender?**
Este es un recorrido completo por el ecosistema de React moderno, que te equipará con las siguientes habilidades:

1.  **Fundamentos y Componentes de React:**
    *   Dominarás la creación de **componentes funcionales** reutilizables, el pilar de cualquier aplicación React.
    *   Aprenderás a manejar el estado local de los componentes con `useState` y a gestionar efectos secundarios (como el fetching de datos) con `useEffect`.

2.  **Gestión de Estado (Local y Global):**
    *   Utilizarás la **Context API** de React para compartir estado entre componentes de forma sencilla.
    *   Implementarás **Redux** para gestionar el estado global de la aplicación, creando una fuente de verdad única y predecible para escenarios complejos.

3.  **Comunicación con el Backend:**
    *   Te convertirás en un experto consumiendo APIs de **GraphQL** usando **Apollo Client**, realizando tanto consultas (`queries`) para leer datos como `mutations` para modificarlos.

4.  **UI, Estilizado y Formularios:**
    *   Construirás interfaces pulidas y consistentes utilizando librerías de componentes como **Material UI** y frameworks de CSS como **Tailwind CSS**.
    *   Crearás formularios robustos y con validaciones complejas utilizando **Formik** y **Yup**.

5.  **Optimización y Experiencia Avanzada:**
    *   Aprenderás a diagnosticar y solucionar cuellos de botella de rendimiento usando herramientas de React como `React.memo`, `useCallback` y la **virtualización de listas**.
    *   Llevarás tus aplicaciones al siguiente nivel convirtiéndolas en **Progressive Web Apps (PWA)**, capaces de funcionar offline gracias a los **Service Workers** y de realizar tareas pesadas en segundo plano con **Web Workers**.

Al finalizar este Path, serás capaz de liderar el desarrollo de cualquier interfaz de usuario en NebulaE, creando experiencias rápidas, fiables y visualmente atractivas.

## Plan de Estudios

El plan se divide en 5 semanas, progresando desde los fundamentos de React hasta la optimización del rendimiento, la gestión avanzada del estado y la creación de Progressive Web Apps.

---

### Semana 1: Fundamentos de React y Componentes

*   **Objetivo:** Construir una base sólida en React y la gestión de estado. El desarrollador aprenderá a crear componentes funcionales, manejar el estado local con los hooks `useState` y `useEffect`, y comprenderá los principios del estado global con Redux (Store, Actions, Reducers). La semana culmina con la integración de React y Redux para leer estado y despachar acciones desde los componentes.
*   **Recursos y Prácticas:**
    *   [Introducción a React (React.dev)](https://react.dev/learn) (2h)
    *   [Hooks: `useState` y `useEffect` (React.dev)](https://react.dev/reference/react/useState) (1.5h)
    *   [Redux: Conceptos Fundamentales (Redux.js.org)](https://redux.js.org/introduction/getting-started) (1.5h)
    *   [React Redux: Conectando Redux con React (React-Redux.js.org)](https://react-redux.js.org/introduction/getting-started) (1h)
    *   **Videos:**
        *   [Introducción a React (componentes, props, estado, fetching)](https://www.youtube.com/watch?v=LDB4uaJ87e0) (1h)
        *   [Introducción a Hooks – useState y useEffect](https://www.youtube.com/watch?v=P5p3vMeJ6LQ) (0.5h)
        *   [useState en 15 minutos](https://www.youtube.com/watch?v=O6P86uwfdR0) (0.25h)
        *   [Redux Tutorial](https://www.youtube.com/watch?v=poQXNp9ItL4) (1.75h)
        *   [Crash Course React completo](https://www.youtube.com/watch?v=CgkZ7MvWUAA) (2h)

### Semana 2: Estilizado y Formularios

*   **Objetivo:** Dominar la construcción de interfaces de usuario y formularios robustos en React. El desarrollador aprenderá a estilizar componentes utilizando la librería de componentes Material UI y el framework utility-first Tailwind CSS. Se enfocará en la creación de formularios complejos, manejando su estado con Formik y aplicando validaciones a prueba de errores mediante esquemas definidos con Yup.
*   **Recursos y Prácticas:**
    *   [Introducción a Material UI (MUI.com)](https://mui.com/material-ui/getting-started/overview/) (1.5h)
    *   [Guía de Tailwind CSS (Tailwindcss.com)](https://tailwindcss.com/docs) (1.5h)
    *   [Formik: Construyendo Formularios en React (Formik.org)](https://formik.org/docs/overview) (2h)
    *   [Yup: Validación de Esquemas (GitHub)](https://github.com/jquense/yup) (1h)
    *   **Videos:**
        *   [React Material UI Tutorial](https://www.youtube.com/playlist?list=PLC3y8-rFHvwh-K9mDlrrcDywl7CeVL2rO)
        *   [Curso React con Tailwind, Redux y MUI](https://www.youtube.com/watch?v=LdomMuzp6jM)
        *   [Formularios con Material UI y Formik](https://www.youtube.com/watch?v=MV9NC3FoCmM)
        *   [Formularios con Material UI, Formik y Yup](https://www.youtube.com/watch?v=aeU2nU45sw4)
        *   [Validación de formularios con Yup](https://www.youtube.com/watch?v=RQ1E2EjyqY4)

### Semana 3: Fetching de Datos y Gestión de Estado Local

*   **Objetivo:** Conectar el frontend con el backend utilizando GraphQL para queries y mutations, y gestionar el estado de la aplicación de forma eficiente con el Context API.
*   **Recursos y Prácticas:**
    *   [Queries con Apollo Client (Apollo GraphQL Docs)](https://www.apollographql.com/docs/react/data/queries/) (1.5h) - Aprende a obtener datos de tu API GraphQL.
    *   [Crash Course React con GraphQL y Apollo Client](https://www.youtube.com/watch?v=gAbIQx26wSI)
    *   [Usando GraphQL, React y Apollo Client](https://www.youtube.com/watch?v=vy9x1Rn0arY)
    *   [Mutations con Apollo Client (Apollo GraphQL Docs)](https://www.apollographql.com/docs/react/data/mutations/) (1.5h) - Guía para enviar datos y modificar el estado en el backend.
    *   [Context API y `useContext` (React.dev)](https://react.dev/reference/react/useContext) (1.5h) - Para compartir estado entre componentes sin "prop drilling".
    *   [React Context API y useContext](https://www.youtube.com/watch?v=NT8_dQ954lE)

### Semana 4: Rendimiento y Estado Global

*   **Objetivo:** Optimizar el rendimiento de los componentes de React y gestionar el estado global de la aplicación para escenarios complejos.
*   **Recursos y Prácticas:**
    *   [Optimizando el Rendimiento con `React.memo` (React.dev)](https://react.dev/reference/react/memo) (1h) - Aprende a prevenir re-renders innecesarios.
    *   [Hooks de Rendimiento: `useCallback` y `useRef` (React.dev)](https://react.dev/reference/react/useCallback) (1.5h) - Para memoizar funciones y valores, y acceder a elementos del DOM.
    *   [Virtualización de Listas con `react-window` (react-window.dev)](https://react-window.dev/) (1.5h) - Para renderizar grandes cantidades de datos de forma eficiente.
    *   [Implementación de estrategias de rendimiento en FrontEnd NebulaE](https://www.youtube.com/watch?v=dummy_video) - Demostración de uso de `React.memo`,  `useCallback`, `useRef` y `react-window` en EMI NebulaE.

### Semana 5: Experiencia de Usuario Avanzada y Persistencia Local

*   **Objetivo:** Mejorar la experiencia del usuario con Progressive Web Apps, Service Workers y Web Workers, y entender las opciones de persistencia de datos en el navegador.
*   **Recursos y Prácticas:**
    *   [Introducción a Progressive Web Apps (web.dev)](https://web.dev/learn/pwa/) (1.5h) - Entiende los beneficios y fundamentos de las PWAs.
    *   [Service Workers: Habilitando Offline (MDN)](https://developer.mozilla.org/es/docs/Web/API/Service_Worker_API) (1.5h) - Aprende a cachear recursos y habilitar funcionalidades offline.
    *   [Web Workers: Ejecución en Segundo Plano (MDN)](https://developer.mozilla.org/es/docs/Web/API/Web_Workers_API) (1h) - Para delegar tareas pesadas y mantener la UI fluida.
    *   [Hooks personalizados + Web Workers](https://www.youtube.com/watch?v=yPAp1h0vk-s) (1h)
    *   [Almacenamiento Local: `localStorage` vs `sessionStorage` (MDN)](https://developer.mozilla.org/es/docs/Web/API/Web_Storage_API) (0.5h) - Comprende cómo y cuándo usar el almacenamiento del navegador para persistir datos.
    *   [Introducción a WebAssembly (MDN)](https://developer.mozilla.org/es/docs/WebAssembly/Concepts) (1.5h) - Conceptos clave de WebAssembly y su integración con JavaScript para tareas de alto rendimiento.