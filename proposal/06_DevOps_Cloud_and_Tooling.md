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

* **Objetivo:** Configurar el entorno de desarrollo y dominar los comandos esenciales de la terminal para la manipulación de archivos, búsqueda y encadenamiento de operaciones.
* **Lecturas y Videos:**    
    * **Navegación y Gestión de Archivos (1.5h):**
        * Comandos: `ls`, `cd`, `pwd`, `mkdir`, `rm`, `cp`, `mv`, `chmod`.
        * **Recursos web oficiales / técnicos:**
            * Español: [Comandos Bash – Wikipedia](https://es.wikipedia.org/wiki/Comandos_Bash)
            * Inglés: [GNU Coreutils – ls, cd, etc.](https://www.gnu.org/software/coreutils/)
        * **Videos verificados:**
            * Español: [Comandos LINUX Básicos Desde Cero – DeciLearn](https://www.youtube.com/watch?v=_KCc-tvpPRM) (2022)
            * Inglés: [Linux Command Line for Beginners – freeCodeCamp](https://www.youtube.com/watch?v=sWbUDq4S6Y8) (2021)
    * **Manipulación y Búsqueda de Texto (2.5h):**
        * Comandos: `cat`, `less`, `head`, `tail`, `grep`, `find`.
        * **Recursos web oficiales / técnicos:**
            * Español: [Comandos Bash – Wikipedia](https://es.wikipedia.org/wiki/Comandos_Bash)
            * Inglés: [grep – man7.org](https://man7.org/linux/man-pages/man1/grep.1.html)
        * **Videos verificados:**
            * Español: [Domina grep y find en Linux](https://www.youtube.com/watch?v=UaV5y1wsSqk) (2021)
            * Inglés: [Linux Text Search – grep & find](https://www.youtube.com/watch?v=VGgTmxXp7xQ) (2022)
    * **Encadenamiento de Comandos y Redirección (2h):**
        * Pipes (`|`), Redirección (`>`, `>>`), Operadores de control (`;`, `&&`).
        * **Recursos web oficiales / técnicos:**
            * Español: [Guía de Redirección y Pipes en Linux – Tecmint](https://www.tecmint.com/use-linux-pipes-to-connect-commands/)
            * Inglés: [Bash Reference Manual – Pipelines](https://www.gnu.org/software/bash/manual/html_node/Pipelines.html)
        * **Videos verificados:**
            * Español: [Pipes y Redirecciones en Linux](https://www.youtube.com/watch?v=Hsno6279tik) 
            * Inglés: [Linux Pipes and Redirection](https://www.youtube.com/watch?v=mV_8GbzwZMM) (2022)
    * **Prerrequisitos de Instalación herramientas de desarrollo (2h):**
        * **Git:**
            * Español: [Instalación de Git – git-scm.com](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)
            * Inglés: [Installing Git – git-scm.com](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
        * **nvm:** 
            * Inglés: [nvm-sh/nvm – GitHub](https://github.com/nvm-sh/nvm#installing-and-updating)
        * **Node.js y Paquetes Globales:**
            * Español: [Node.js en Español](https://nodejs.org/es)
            * Inglés: [Node.js Official](https://nodejs.org/en)

---

### Semana 2: Docker y Docker Compose

* **Objetivo:** Dominar la creación y gestión de contenedores con Docker y orquestar aplicaciones multi-servicio con Docker Compose.
* **Lecturas y Videos:**
    * **Docker: Fundamentos y Gestión de Contenedores (2.5h):**
        * **Recursos web oficiales / técnicos:**
            * Español: [Introducción a Docker – Docker Docs ES](https://docs.docker.com/get-started/overview/?lang=es)
            * Inglés: [Docker Overview – Docker Docs](https://docs.docker.com/get-started/overview/)
        * **Videos verificados:**
            * Inglés: [Docker Tutorial for Beginners – TechWorld](https://www.youtube.com/watch?v=3c-iBn73dDE) (2021)
    * **Imágenes y Dockerfile (1.5h):**
        * **Recursos web oficiales / técnicos:**
            * Español: [Dockerfile – Docker Docs ES](https://docs.docker.com/engine/reference/builder/?lang=es)
            * Inglés: [Dockerfile reference – Docker Docs](https://docs.docker.com/engine/reference/builder/)
    * **Docker Compose (2.5h):**
        * **Recursos web oficiales / técnicos:**
            * Español: [Docker Compose – Docker Docs ES](https://docs.docker.com/compose/?lang=es)
            * Inglés: [Docker Compose – Docker Docs](https://docs.docker.com/compose/)
        * **Videos verificados:**
            * Inglés: [Docker Compose in 12 Minutes](https://www.youtube.com/watch?v=HG6yIjZapSA) (2022)
    * **Redes y Volúmenes en Compose (1.5h):**
        * **Recursos web oficiales / técnicos:**
            * Español: [Redes en Docker Compose](https://docs.docker.com/compose/networking/?lang=es)
            * Inglés: [Docker Compose Networking](https://docs.docker.com/compose/networking/)

---

### Semana 3: Google Cloud y Fundamentos de Kubernetes (GKE)

* **Objetivo:** Familiarizarse con la CLI de Google Cloud (`gcloud`), configurar un proyecto y crear un clúster de Kubernetes (GKE) para interactuar con él.
* **Lecturas y Videos:**
    * **Google Cloud CLI (1.5h):**
        * Inglés: [Google Cloud CLI Overview](https://cloud.google.com/sdk/docs/overview)
    * **Gestión de Proyectos en GCP (1h):**
        * Español: [Creación y gestión de proyectos](https://cloud.google.com/resource-manager/docs/creating-managing-projects?hl=es)
        * Inglés: [Creating and Managing Projects](https://cloud.google.com/resource-manager/docs/creating-managing-projects)
    * **Creación de Clúster GKE (1.5h):**
        * Español: [Crear clúster de GKE](https://cloud.google.com/kubernetes-engine/docs/how-to/creating-a-zonal-cluster?hl=es)
        * Inglés: [Creating a Zonal Cluster](https://cloud.google.com/kubernetes-engine/docs/how-to/creating-a-zonal-cluster)
    * **kubectl básico (2h):**
        * Español: [Acceso al clúster con kubectl](https://cloud.google.com/kubernetes-engine/docs/how-to/cluster-access-for-kubectl?hl=es)
        * Inglés: [Cluster Access for kubectl](https://cloud.google.com/kubernetes-engine/docs/how-to/cluster-access-for-kubectl)
        * Videos:
            * Inglés: [Kubectl Basic Commands ](https://www.youtube.com/watch?v=azuwXALfyRg) 
    * **Port Forwarding (1h):**
        * Inglés: [Port Forwarding in Kubernetes](https://kubernetes.io/docs/tasks/access-application-cluster/port-forward-access-application-cluster/)

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
