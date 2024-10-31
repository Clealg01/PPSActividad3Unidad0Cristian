# README - PPS Unidad 0 Actividad 3

## Índice

1. [Introducción](#introducción)
2. [Pasos a Realizar](#pasos-a-realizar)
   - [Primeros Pasos](#Primeros-Pasos)
   - [Uso de Git](#uso-de-git)
   - [Creación de Contenedor GitLab](#creación-de-contenedor-gitlab)
3. [Contenidos del Repositorio](#contenidos-del-repositorio)
   - [Estructura del Repositorio](#estructura-del-repositorio)
   - [Descripción de Archivos](#descripción-de-archivos)
      - [README.md](#readmemd)
      - [Install.md](#installmd)
      - [UsoGit.md](#usogitmd)
      - [GitHub.md](#githubmd)
      - [GitLab.md](#gitlabmd)
4. [Pasos Detallados](#pasos-detallados)
   - [1. Crear Cuenta en GitHub](#1-crear-cuenta-en-github)
   - [2. Instalar Git y PHP](#2-instalar-git-y-php)
   - [3. Configurar Git y Añadir Clave SSH](#3-configurar-git-y-añadir-clave-ssh)
   - [4. Crear Repositorio Local](#4-crear-repositorio-local)
   - [5. Añadir y Modificar Archivos](#5-añadir-y-modificar-archivos)
   - [6. Realizar Commit y Push](#6-realizar-commit-y-push)
5. [Referencias y Recursos Adicionales](#referencias-y-recursos-adicionales)

---

## Introducción
En esta actividad, la tarea principal es crear un repositorio en GitHub para documentar el proceso de aprendizaje y práctica con Git y GitHub. El proyecto debe contener documentación en archivos .md que expliquen cada paso del proceso, junto con los archivos y recursos necesarios. 

Básicamente, se busca familiarizarse con el manejo de Git y GitHub, la documentación del trabajo técnico y la gestión de un repositorio, habilidades esenciales en entornos de desarrollo y colaboración.

---

## Pasos a Realizar


| 1. Primeros Pasos|
|:-----------------------:|
- **Paso 1**: Abre una cuenta en [GitHub](https://github.com) con tu correo personal, en mi caso será con el correo institucional: `@informatica.iesvalledeljerteplasencia.es`.
- **Paso 2**: Instala Git y PHP en tu equipo.

En las siguientes imágenes podemos visualizar los comandos que necesitamos para la instalación de las tecnologías y como comprobar si las hemos instalado correctamente:

![Descargar Git](./images/Descargar%20Git.png)
<p align="center"><em>Figura 2: Descarga de Git</em></p>

![Descargar PHP](./images/Descargar%20php.png)
<p align="center"><em>Figura 3: Descarga de PHP</em></p>


- **Paso 3**: Configura Git correctamente con tu cuenta.
  - Crea una clave SSH y añádela a tu configuración de Git.
  - Puedes consultar este [artículo de referencia](https://example.com) para más detalles sobre la creación de claves SSH.

| 2. Uso de Git|
|:-----------------------:|

- **Paso 1**: Clona el repositorio recién creado en tu equipo:
  ```bash
  git clone https://github.com/tuusuario/PPSActividad3Unidad0TuNombre.git
- **Paso 2**: Añade los archivos y carpetas necesarios al proyecto.
- **Paso 3**: Verifica el estado del repositorio:
  ```bash
  git status
- **Paso 4**: Añade los archivos al índice:
  ```bash
  git add .
- **Paso 5**: Haz un commit con un mensaje adecuado:
  ```bash
  git commit -m "Creación de archivos y estructura inicial"
- **Paso 6**: Sube los cambios al repositorio remoto:
  ```bash
  git push origin main
1. Creación de Contenedor GitLab
Paso 1: Levanta un contenedor Docker con una instancia de GitLab.
Utiliza el siguiente comando para ejecutar el contenedor:

Paso 2: Configura y accede a GitLab en tu máquina local mediante el navegador en http://localhost.

4. Contenidos del Repositorio
README.md:
Debe contener una introducción al proyecto.
Incluir enlaces a otros archivos .md dentro del repositorio para facilitar la navegación.
Install.md:
Incluir el proceso de instalación y configuración de Git en el equipo local.
Utilizar fragmentos de código en lugar de capturas de pantalla, por ejemplo:
bash
Copiar código
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
UsoGit.md:
Describir los comandos de Git que se usaron durante la actividad, con ejemplos prácticos.
GitHub.md:
Explicar el proceso de creación de una cuenta en GitHub.
Incluir los pasos para iniciar sesión y configurar el repositorio con claves SSH.
GitLab.md:
Documentar el proceso para levantar un contenedor Docker con GitLab y cómo configurarlo.
Pasos Finales
Realiza una comprobación con git status para asegurar que no hay archivos pendientes de añadir o subir.
Verifica que todos los archivos y recursos se visualizan correctamente en el repositorio de GitHub.
Asegúrate de que los enlaces internos de los archivos .md sean funcionales
Desglose de los pasos generales que se deben realizar para completar esta práctica. Incluye detalles sobre la configuración inicial de Git y la creación de un contenedor GitLab.

### Contenidos del Repositorio
Descripción de los archivos y carpetas esenciales que debe contener el repositorio, como `README.md`, `Install.md`, `UsoGit.md`, `GitHub.md`, y `GitLab.md`.

### Pasos Detallados
Explicación de cada uno de los pasos a seguir, incluyendo la creación de la cuenta en GitHub, instalación y configuración de Git, creación del repositorio local, y los comandos básicos de Git para realizar `commit` y `push`.

### Referencias y Recursos Adicionales
Enlaces a artículos y documentación relevante, incluyendo el artículo sobre la creación de la clave SSH.