# Path 4: Desarrollo Frontend con React

## Objetivo del Path

Este path cubre cómo construir interfaces de usuario modernas, eficientes y responsivas que se integran con nuestros microservicios. El objetivo es capacitar al desarrollador para construir componentes de React performantes y reutilizables, gestionar el estado de la aplicación de forma eficaz y aplicar nuestros estándares de UI/UX.

## Plan de Estudios

El plan se divide en 5 semanas, progresando desde los fundamentos de React hasta la optimización del rendimiento, la gestión avanzada del estado y la creación de Progressive Web Apps.

---

### Semana 1: Fundamentos de React y Componentes

*   **Objetivo:** Comprender los conceptos básicos de React, cómo crear componentes funcionales y utilizar los hooks esenciales para manejar el estado y los efectos secundarios.
*   **Recursos y Prácticas:**
    *   [Introducción a React (React.dev)](https://react.dev/learn) (2h) - La documentación oficial es el mejor punto de partida para entender los componentes, JSX y el renderizado.
    *   [Introducción a React (componentes, props, estado, fetching)](https://www.youtube.com/watch?v=LDB4uaJ87e0) (1h)
    *   [Hooks: `useState` y `useEffect` (React.dev)](https://react.dev/reference/react/useState) (1.5h) - Guías detalladas sobre cómo añadir estado a los componentes funcionales y manejar efectos secundarios.
    *   [Introducción a Hooks – useState y useEffect](https://www.youtube.com/watch?pp=0gcJCfwAo7VqN5tD&v=P5p3vMeJ6LQ) (0.5h)
    *   [useState en 15 minutos (React Hooks explicados)](https://www.youtube.com/watch?v=O6P86uwfdR0) (0.25h)
    *   [Redux: Conceptos Fundamentales (Redux.js.org)](https://redux.js.org/introduction/getting-started) (1.5h) - Introducción a los principios de Redux: Store, Actions, Reducers.
    *   [React Redux: Conectando Redux con React (React-Redux.js.org)](https://react-redux.js.org/introduction/getting-started) (1h) - Cómo usar `Provider`, `useSelector` y `useDispatch` para integrar Redux en componentes de React.
    *   [Crash Course React completo](https://www.youtube.com/watch?pp=0gcJCfwAo7VqN5tD&v=CgkZ7MvWUAA) (2h)

### Semana 2: Estilizado y Formularios

*   **Objetivo:** Aprender a estilizar componentes con bibliotecas de UI y a construir formularios robustos con validación.
*   **Recursos y Prácticas:**
    *   [Introducción a Material UI (MUI.com)](https://mui.com/material-ui/getting-started/overview/) (1.5h) - Guía para empezar a usar la biblioteca de componentes de Material Design.
    *   [Curso React con Tailwind, Redux y MUI](https://www.youtube.com/watch?v=LdomMuzp6jM)
    *   [Formularios con Material UI y Formik](https://www.youtube.com/watch?v=MV9NC3FoCmM)
    *   [Formularios con Material UI, Formik y Yup](https://www.youtube.com/watch?v=aeU2nU45sw4)
    *   [Guía de Tailwind CSS (Tailwindcss.com)](https://tailwindcss.com/docs) (1.5h) - Documentación oficial para el framework CSS utility-first.
    *   [Formik: Construyendo Formularios en React (Formik.org)](https://formik.org/docs/overview) (2h) - Tutorial oficial para manejar el estado de formularios, validación y envío.
    *   [Yup: Validación de Esquemas (GitHub)](https://github.com/jquense/yup) (1h) - Documentación para definir esquemas de validación de datos.
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

### Semana 5: Experiencia de Usuario Avanzada y Persistencia Local

*   **Objetivo:** Mejorar la experiencia del usuario con Progressive Web Apps, Service Workers y Web Workers, y entender las opciones de persistencia de datos en el navegador.
*   **Recursos y Prácticas:**
    *   [Introducción a Progressive Web Apps (web.dev)](https://web.dev/learn/pwa/) (1.5h) - Entiende los beneficios y fundamentos de las PWAs.
    *   [Service Workers: Habilitando Offline (MDN)](https://developer.mozilla.org/es/docs/Web/API/Service_Worker_API) (1.5h) - Aprende a cachear recursos y habilitar funcionalidades offline.
    *   [Web Workers: Ejecución en Segundo Plano (MDN)](https://developer.mozilla.org/es/docs/Web/API/Web_Workers_API) (1h) - Para delegar tareas pesadas y mantener la UI fluida.
    *   [Hooks personalizados + Web Workers](https://www.youtube.com/watch?v=yPAp1h0vk-s) (1h)
    *   [Almacenamiento Local: `localStorage` vs `sessionStorage` (MDN)](https://developer.mozilla.org/es/docs/Web/API/Web_Storage_API) (0.5h) - Comprende cómo y cuándo usar el almacenamiento del navegador para persistir datos.
    *   [Introducción a WebAssembly (MDN)](https://developer.mozilla.org/es/docs/WebAssembly/Concepts) (1.5h) - Conceptos clave de WebAssembly y su integración con JavaScript para tareas de alto rendimiento.
