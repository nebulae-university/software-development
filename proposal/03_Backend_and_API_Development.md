# Path 3: Desarrollo Backend y APIs con NodeJS y RxJS

## Objetivo del Path

Este path se sumerge en el corazón de nuestros microservicios: la lógica de negocio. Se enfoca en el desarrollo del lado del servidor con NodeJS, haciendo un uso intensivo de la programación asíncrona y reactiva. El objetivo es dominar la implementación de lógicas de negocio complejas y eficientes utilizando NodeJS y los operadores clave de RxJS, y exponerlas a través de APIs robustas, bien definidas con OpenAPI y construidas con Express.

### Descripción General del Path

Este Path te lleva al cuarto de máquinas de nuestros microservicios. Si en el Path 2 aprendiste a *ensamblar* un servicio usando el framework, aquí aprenderás a construir su **motor**. El propósito es que domines el arte del desarrollo backend moderno en NodeJS, no solo como un ejecutor de lógica, sino como un director de orquesta que maneja flujos de datos complejos de manera eficiente y resiliente.

**¿Qué se espera de ti?**
Se espera una inmersión profunda en el paradigma de **programación reactiva**. Deberás abandonar la mentalidad de petición-respuesta secuencial y empezar a "pensar en streams". Este cambio de paradigma es exigente pero transformador. Se requiere paciencia, mucha práctica con los operadores de RxJS y una voluntad de entender cómo los datos fluyen, se transforman, se combinan y se manejan a lo largo del tiempo.

**¿Qué vas a aprender?**
Este es un viaje intensivo en NodeJS y, sobre todo, en RxJS. Al finalizar, serás capaz de:

1.  **Dominar el Asincronismo en NodeJS:** Irás más allá del `async/await` básico para entender cómo y por qué la programación reactiva es la siguiente evolución para manejar operaciones concurrentes complejas, especialmente en un entorno basado en eventos como el nuestro.

2.  **Pensar en Streams con RxJS:**
    *   **Fundamentos:** Internalizarás los conceptos de `Observable`, `Observer` y `Subscription`. Entenderás la diferencia crucial entre observables "fríos" y "calientes".
    *   **Maestría en Operadores:** Construirás un arsenal de operadores de RxJS para filtrar (`filter`, `take`, `debounceTime`), transformar (`map`, `mergeMap`, `concatMap`) y combinar (`forkJoin`, `zip`, `withLatestFrom`) flujos de datos.
    *   **Manejo de Errores y Ciclo de Vida:** Aprenderás a construir pipelines de datos robustos que manejan errores con elegancia (`catchError`) y a gestionar la memoria para evitar fugas (`takeUntil`).

3.  **Diseñar y Construir APIs Profesionales:**
    *   Aprenderás a definir contratos de API claros y precisos usando la especificación **OpenAPI**, garantizando que tus servicios sean fáciles de entender y consumir.
    *   Implementarás estos contratos usando **Express**, el framework estándar de facto para APIs en NodeJS.

4.  **Comprender Tópicos Avanzados:** Profundizarás en temas de bajo nivel como la representación de datos (bits, bytes, endianness) para entender cómo se mueven los datos por la red, dándote una visión completa del stack.

Este Path te dará las habilidades para construir la lógica de negocio más compleja de nuestros sistemas, creando backends que no solo funcionan, sino que son eficientes, escalables y reactivos.

## Plan de Estudios

El plan se divide en 5 semanas, construyendo desde los fundamentos de NodeJS y paradigmas de programación, pasando por los fundamentos y operadores de RxJS, hasta el diseño e implementación de APIs basadas en especificaciones y tópicos avanzados.

---

### Semana 1: Fundamentos de NodeJS, Asincronismo y Paradigmas

* **Objetivo:** Establecer una base sólida en los patrones de asincronismo de NodeJS y en los paradigmas de programación declarativa e imperativa que guían nuestro estilo de código.
* **Recursos y Prácticas:**
  * [Guía de asincronismo en JS: Callbacks, Promises, Async/Await (MDN)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous) _(2h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=PoRJizFvM7s
      * https://www.youtube.com/watch?v=V_Kr9OSfDeU
  * [Programación Imperativa vs Declarativa](https://dev.to/siddharthshyniben/explained-imperative-vs-declarative-programming-577g) _(1h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=E7Fbf7R3x6I
  * [Práctica Declarativa: Métodos de Array (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) _(1.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=8MoElay6dWU
  * [Igualdad y Falsy Values en JS (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness) _(0.5h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=jD2BuBfxRn8
      * https://www.youtube.com/watch?v=5DVqAFhfSsE

### Semana 2: RxJS — Fundamentos, Creación de Streams y Utilidad

* **Objetivo:** Comprender los conceptos esenciales de la programación reactiva: `Observable`, `Observer`, `Subscription` y `Subject`, y aprender a crear flujos de datos desde diversas fuentes y aplicar operadores de utilidad.
* **Recursos y Prácticas:**
  * [Guía de Inicio Rápido de RxJS (rxjs.dev)](https://rxjs.dev/guide/overview) _(1.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=PhggNGsSQyg
  * [Operadores de Creación (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/creation) _(2h)_ — Incluye `of`, `from`, `range`, `interval`, `timer`, `create`.
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=BgHphtY8IPE
      * https://www.youtube.com/watch?v=xYiafdImxU8
      * https://www.youtube.com/watch?v=Niwo4bY1CU4
  * [Hot vs Cold Observables (Academind)](https://www.youtube.com/watch?v=zfQoleQEa4w) _(1h)_
  * [Subjects en RxJS (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/subjects) _(1h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=rdK92pf3abs
      * https://www.youtube.com/watch?v=s1oV2FMK1jc
  * [¿Por qué usar RxJS en el Backend de Node.js? (dev.to)](https://dev.to/this-is-learning/why-use-rxjs-in-node-js-backend-5eh1) _(1h)_
    * **Video sugerido (aplicación práctica en JS):**
      * https://www.youtube.com/watch?v=j6fY0QjLSYo
  * [Operador `tap` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/tap) _(1h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=2N9KA6UHjmw
      * https://www.youtube.com/watch?v=HcwPyzD4LXQ
  * [Operador `delay` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/delay) _(0.5h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=fzijXza_660
      * https://www.youtube.com/watch?v=tVVAvVd61zo
  * [Operador `timeout` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/timeout) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=Xi9w4GmbidM
  * [Operador `toPromise` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/utility/topromise) _(0.5h)_
    * **Video recomendado (deprecado — alternativas):**
      * https://www.youtube.com/live/3aeK5SfWBSU

### Semana 3: RxJS — Filtrado y Transformación

* **Objetivo:** Dominar los operadores de RxJS para manipular, transformar y seleccionar los datos que viajan a través de los flujos.
* **Recursos y Prácticas:**
  * [Operador `filter` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/filter) _(1h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=tk5x8By3yYk
      * https://www.youtube.com/watch?v=w44c1VXtRKc
  * [Operador `debounceTime` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/debouncetime) _(0.5h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=VmBKiLqeSPo
      * https://www.youtube.com/watch?v=QbNUD5ca99A
  * [Operador `throttleTime` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/throttletime) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=lDPcJxSsYZY
  * [Operador `first` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/first) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=d8RQs9ZXieE
  * [Operador `last` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/last) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=XNWdxPK9zZs
  * [Operador `take` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/take) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=FAZRFXg80k0
  * [Operador `takeUntil` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/filtering/takeuntil) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=KkgE3Ct3Djc
  * [Operador `mergeMap` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/mergemap) _(1h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=Ar_hCJBEG2E
  * [Operador `concatMap` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/concatmap) _(1h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=lM16-E-uCWc
  * [Operador `groupBy` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/groupby) _(1h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=JLYznawrX-8
  * [Operador `map` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/map) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=-nYQJkMpOHU
  * [Operador `reduce` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/reduce) _(0.5h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=96KUjeiNfX8
      * https://www.youtube.com/watch?v=uZplLJU9yZU
  * [Operador `toArray` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/toarray) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=_8g2XfXaalI
  * [Operador `pluck` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/transformation/pluck) _(0.5h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=IVBJ3-M_YsQ
      * https://www.youtube.com/watch?v=gPWibhLl1Fc

### Semana 4: RxJS — Combinación y Manejo de Errores

* **Objetivo:** Aprender a combinar múltiples flujos de datos y a manejar los errores de forma robusta en pipelines complejos.
* **Recursos y Prácticas:**
  * [Operador `forkJoin` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/combination/forkjoin) _(1h)_
  * [Operador `race` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/combination/race) _(1h)_
  * [Operador `zip` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/combination/zip) _(1h)_
  * [Operador `withLatestFrom` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/combination/withlatestfrom) _(1h)_
    * **Videos recomendados (comparativos y prácticos):**
      * https://www.youtube.com/watch?v=heAbcedeIQY
      * https://www.youtube.com/watch?v=FI3R07Zt6NI
  * [Manejo de Errores con `catchError` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/error_handling/catcherror) _(1h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=5APbAespiuo
  * [Operador `bufferTime` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/combination/buffertime) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=KD3hE6JKAg0
  * [Operador `bufferCount` (LearnRxJS)](https://www.learnrxjs.io/learn-rxjs/operators/combination/buffercount) _(0.5h)_
    * **Video recomendado:**
      * https://www.youtube.com/watch?v=kRNiSIAK1zs

### Semana 5: Diseño e Implementación de APIs y Tópicos Avanzados

* **Objetivo:** Diseñar e implementar APIs robustas con OpenAPI y Express, y comprender conceptos avanzados de representación de datos y debugging.
* **Recursos y Prácticas:**
  * [Referencia de la Especificación OpenAPI 3.1 (Swagger.io)](https://spec.openapis.org/oas/v3.1.0) _(2.5h)_
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=Sflpzh_cAcA
      * https://www.youtube.com/watch?v=vcS9WdFLCbw
  * **Representación Numérica (bits, bytes, entero/sin signo, endianness, hex, ASCII):** _(1h)_
    * **Guías (lectura):**
      * https://www.tutorialspoint.com/computer_logical_organization/number_systems.htm
      * https://www.tutorialspoint.com/computer_logical_organization/data_representation.htm
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=NcaiHcBvDR4
      * https://www.youtube.com/watch?v=y45v5SLjxaM
      * https://www.youtube.com/watch?v=DntKZ9xJ1sM
  * **Debugging y Memory Leaks en RxJS:** _(1.5h)_
    * **Artículos (lectura):**
      * https://medium.com/@benlesh/rxjs-dont-unsubscribe-6753ed4fda87
      * https://medium.com/@matthew.mccullough/memory-leaks-in-rxjs-and-how-to-avoid-them-3d96d26d1b6b
    * **Videos recomendados:**
      * https://www.youtube.com/watch?v=OhuRvfcw3Tw
      * https://www.youtube.com/watch?v=ZxVN4597RX8
      * https://www.youtube.com/watch?v=oFFV-bXcP4A
