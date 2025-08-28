# Path 6: DevOps, Cloud y Herramientas

## Objetivo del Path

Este path familiariza al desarrollador con el ecosistema de DevOps, las herramientas de desarrollo y la infraestructura cloud de NebulaE. El objetivo es maximizar la productividad, asegurar despliegues fiables y capacitar al desarrollador para interactuar eficientemente con el entorno de producción y las herramientas de IA.

### Descripción General del Path

Este Path es el que hace que todo lo demás sea posible. Es el puente entre el código que escribes en tu máquina y el valor que entregas a los usuarios en producción. El propósito de este camino es inculcar una **mentalidad DevOps**, donde el desarrollo y las operaciones no son mundos separados, sino una disciplina unificada. Aprenderás a manejar las herramientas y la infraestructura que nos permiten construir, probar y desplegar software de manera rápida, automatizada y fiable.

**¿Qué se espera de ti?**
Se espera que te conviertas en un desarrollador autosuficiente. Deberás sentirte tan cómodo en la línea de comandos como en tu editor de código. Se requiere una curiosidad por entender cómo funcionan las cosas "debajo del capó": cómo se empaqueta una aplicación en un contenedor, cómo se orquesta en la nube y cómo fluye a través de un pipeline de CI/CD. La meta es que veas la infraestructura no como un obstáculo, sino como una herramienta poderosa que puedes y debes controlar.

**¿Qué vas a aprender?**
Este recorrido te convertirá en un maestro de la navaja suiza del desarrollador moderno, cubriendo:

1.  **Maestría en la Línea de Comandos (CLI):**
    *   Irás más allá de los comandos básicos para dominar la composición de herramientas (`grep`, `find`, `|`, `>`), permitiéndote realizar tareas complejas de manipulación y búsqueda de archivos directamente desde la terminal.

2.  **Contenerización con Docker:**
    *   Aprenderás a empaquetar tus aplicaciones y todas sus dependencias en **contenedores Docker** portátiles y reproducibles.
    *   Orquestarás entornos de desarrollo locales complejos que simulan la producción usando **Docker Compose**, definiendo redes y volúmenes para aplicaciones multi-servicio.

3.  **Orquestación en la Nube con Kubernetes (GKE):**
    *   Darás el salto a la nube, aprendiendo a provisionar y gestionar clústeres de **Kubernetes** en Google Kubernetes Engine (GKE) usando la CLI de `gcloud`.
    *   Interactuarás con tus clústeres usando `kubectl` para desplegar, inspeccionar y depurar aplicaciones.

4.  **Automatización con CI/CD:**
    *   Entenderás los principios de la Integración Continua y el Despliegue Continuo (CI/CD).
    *   Aprenderás los fundamentos de **GitLab CI/CD** para automatizar el proceso de construcción, prueba y despliegue de tus contenedores en Kubernetes.

5.  **Servicios Cloud y Automatización:**
    *   Utilizarás servicios esenciales de **Google Cloud Platform (GCP)** como Pub/Sub para mensajería y Cloud Storage para almacenamiento de objetos.
    *   Aprenderás a monitorear tus aplicaciones con Google Monitoring y a automatizar tareas repetitivas con **scripts de Bash**.

Al finalizar este Path, tendrás una visión completa del ciclo de vida del software, desde un `git commit` hasta una aplicación funcionando a escala en la nube, y poseerás las habilidades para mantener ese ciclo funcionando de manera eficiente y robusta.

## Plan de Estudios

El plan se divide en 5 semanas, progresando desde el dominio de la línea de comandos y el entorno local hasta la gestión de infraestructura cloud y la automatización.

---

### Semana 1: Entorno y Línea de Comandos (CLI)

*   **Objetivo:** Configurar un entorno de desarrollo profesional y dominar la línea de comandos. El desarrollador instalará y configurará las herramientas esenciales (Git, nvm, Node.js) y obtendrá fluidez en la navegación, manipulación de archivos, búsqueda de texto (`grep`, `find`) y el encadenamiento de operaciones mediante pipes y redirección. Se introducirán los fundamentos de la automatización con scripts de Bash.
*   **Recursos y Prácticas:**
    *   **Git:**
        *   [Instalación de Git (Español)](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)
        *   [Installing Git (Inglés)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
    *   **nvm:** 
        *   [nvm-sh/nvm – GitHub](https://github.com/nvm-sh/nvm#installing-and-updating)
    *   **Node.js:**
        *   [Node.js en Español](https://nodejs.org/es)
        *   [Node.js Official](https://nodejs.org/en)
    *   **Comandos Bash:**
        *   [Comandos Bash – Wikipedia (Español)](https://es.wikipedia.org/wiki/Comandos_Bash)
        *   [GNU Coreutils – ls, cd, etc. (Inglés)](https://www.gnu.org/software/coreutils/)
    *   **Pipes y Redirección:**
        *   [Guía de Redirección y Pipes en Linux – Tecmint (Español)](https://www.tecmint.com/use-linux-pipes-to-connect-commands/)
        *   [Bash Reference Manual – Pipelines (Inglés)](https://www.gnu.org/software/bash/manual/html_node/Pipelines.html)
    *   **Videos:**
        *   [Configuración básica del entorno de desarrollo](https://youtu.be/RzYQwp_6UKs)
        *   [Comandos LINUX Básicos Desde Cero – DeciLearn (Español)](https://www.youtube.com/watch?v=_KCc-tvpPRM) (2022)
        *   [Linux Command Line for Beginners – freeCodeCamp (Inglés)](https://www.youtube.com/watch?v=sWbUDq4S6Y8) (2021)
        *   [Comando find](https://www.youtube.com/watch?v=Au9OM5-RgIM)
        *   [Comando GREP](https://www.youtube.com/watch?v=MfDVUemyQOo)
        *   [Linux Text Search – grep & find (Inglés)](https://www.youtube.com/watch?v=VGgTmxXp7xQ) (2022)
        *   [Pipes y Redirecciones en Linux (Español)](https://www.youtube.com/watch?v=Hsno6279tik)
        *   [Linux Pipes and Redirection (Inglés)](https://www.youtube.com/watch?v=mV_8GbzwZMM) (2022)
        *   [Bash Scripting Crash Course (Inglés)](https://www.youtube.com/watch?v=tK9Oc6AEnR4) (2022)

---

### Semana 2: Docker y Docker Compose

*   **Objetivo:** Dominar los fundamentos de la contenerización con Docker. El desarrollador aprenderá a empaquetar una aplicación y sus dependencias en una imagen de Docker escribiendo un `Dockerfile`. Posteriormente, orquestará una aplicación multi-servicio (ej: aplicación + base de datos) utilizando Docker Compose, definiendo servicios, redes para la comunicación y volúmenes para la persistencia de datos.
*   **Recursos y Prácticas:**
    *   [Introducción a Docker – Docker Docs ES](https://docs.docker.com/get-started/overview/?lang=es)
    *   [Referencia de Dockerfile – Docker Docs](https://docs.docker.com/engine/reference/builder/)
    *   [Docker Compose – Docker Docs](https://docs.docker.com/compose/)
    *   [Redes en Docker Compose](https://docs.docker.com/compose/networking/)
    *   [Volúmenes en Docker](https://docs.docker.com/storage/volumes/)
    *   **Videos:**
        *   [Docker Tutorial for Beginners – TechWorld](https://www.youtube.com/watch?v=3c-iBn73dDE) (2021)
        *   [Docker Compose in 12 Minutes](https://www.youtube.com/watch?v=HG6yIjZapSA) (2022)

---

### Semana 3: Operación de Servicios en un Entorno Cloud Existente (GCP y GKE)

*   **Objetivo:** El desarrollador aprenderá a conectarse y operar sobre un entorno de Google Cloud Platform (GCP) y Kubernetes (GKE) pre-existente. El enfoque será dominar las herramientas de línea de comandos (`gcloud`, `kubectl`) para realizar tareas esenciales de DevOps, como la inspección de logs, la ejecución de comandos remotos, el reenvío de puertos para acceso a bases de datos, y la publicación/consumo de mensajes a través de Pub/Sub.

*   **Recursos y Prácticas:**

    1.  **Conexión al Entorno GCP y GKE:**
        *   **Lectura:** [Instalación y Configuración de Google Cloud CLI](https://cloud.google.com/sdk/docs/install)
        *   **Práctica:** Conectarse a la cuenta de NebulaE y configurar el proyecto `nebulae-lab` usando `gcloud auth login` y `gcloud config set project nebulae-lab`.
        *   **Práctica:** Configurar `kubectl` para apuntar al clúster del proyecto con `gcloud container clusters get-credentials`.

    2.  **Inspección y Depuración de Cargas de Trabajo en Kubernetes:**
        *   **Lectura:** [Hoja de Referencia (Cheat Sheet) de `kubectl`](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
        *   **Práctica:** Usar `kubectl logs <nombre-del-pod-mongo> -f` para ver los logs en tiempo real y `kubectl exec -it <nombre-del-pod-mongo> -- /bin/bash` para obtener una shell interactiva.

    3.  **Acceso a Servicios Internos del Clúster:**
        *   **Lectura:** [Documentación Oficial de `kubectl port-forward`](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#port-forward)
        *   **Práctica:** Usar `kubectl port-forward <nombre-del-pod-mongo> 27017:27017` para conectar una herramienta de base de datos local al pod de MongoDB.

    4.  **Interacción con Google Cloud Pub/Sub desde CLI:**
        *   **Lectura:** [Guía de Inicio Rápido de `gcloud pubsub`](https://cloud.google.com/pubsub/docs/quickstart-cli)
        *   **Práctica:** Publicar un mensaje de prueba en un tópico de `nebulae-lab` y luego consumirlo desde una suscripción.

---

### Semana 4: Despliegue en Kubernetes y CI/CD con GitLab

* **Objetivo:** Aprender a desplegar y gestionar aplicaciones en Kubernetes usando archivos YAML y comprender su integración en un pipeline de CI/CD.
* **Lecturas y Videos:**
    * **Manifiestos de Kubernetes (2.5h):**
        * Español: [Deployments – Kubernetes Docs ES](https://kubernetes.io/es/docs/concepts/workloads/controllers/deployment/)
        * Inglés: [Deployments – Kubernetes Docs](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
        * Videos:
            * Inglés: [Kubernetes Deployments](https://www.youtube.com/watch?v=Sulw5ndbE88) 
    * **kubectl apply (1.5h):**
        * Inglés: [kubectl apply – Kubernetes Docs](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#apply)
    * **Introducción a GitLab CI/CD (2h):**
        * Inglés: [Introduction to CI/CD – GitLab Docs](https://docs.gitlab.com/ci/)
        * Videos:
            * Inglés: [GitLab CI/CD Tutorial](https://www.youtube.com/watch?v=PGyhBwLyK2U) (2021)
    * **Container Registry y Variables (1h):**
        * Inglés: [Container Registry – GitLab Docs](https://docs.gitlab.com/ee/user/packages/container_registry/)

---

### Semana 5: Servicios de GCP, Monitoreo y Automatización

* **Objetivo:** Utilizar servicios clave de GCP, monitorear aplicaciones con Google Monitoring y automatizar tareas con scripts y asistentes de IA.
* **Lecturas y Videos:**
    * **Google Pub/Sub (1.5h):**
        * Español: [Introducción a Pub/Sub](https://cloud.google.com/pubsub/docs/overview?hl=es)
        * Inglés: [Pub/Sub Overview](https://cloud.google.com/pubsub/docs/overview)
    * **Cloud Storage (1.5h):**
        * Español: [Introducción a Cloud Storage](https://cloud.google.com/storage/docs/introduction?hl=es)
        * Inglés: [Cloud Storage Overview](https://cloud.google.com/storage/docs/introduction)
    * **Logging y Monitoring (2h):**
        * Español: [Logging – Google Cloud](https://cloud.google.com/logging/docs/overview?hl=es)
        * Inglés: [Logging Overview](https://cloud.google.com/logging/docs/overview)
    * **Dashboards en Monitoring (1h):**
        * Español: [Creación de dashboards](https://cloud.google.com/monitoring/charts/dashboards?hl=es)
        * Inglés: [Creating Dashboards](https://cloud.google.com/monitoring/charts/dashboards)
    * **Automatización con Bash(2h):**
        * Español: [programación de Bash](https://www.freecodecamp.org/espanol/news/tutorial-de-programacion-de-bash-script-de-shell-de-linux-y-linea-de-comandos-para-principiantes/)
        * Videos:
            * Inglés: [Bash Scripting Crash Course](https://www.youtube.com/watch?v=tK9Oc6AEnR4) (2022)