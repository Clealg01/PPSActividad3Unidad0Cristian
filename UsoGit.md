# Comandos principales de Git

## Introducción
GitHub es una plataforma de desarrollo colaborativo que permite a los desarrolladores almacenar, gestionar y colaborar en proyectos de software a través del control de versiones de Git. En este documento, aprenderás cómo crear una cuenta en GitHub, iniciar sesión y usar sus funciones básicas para gestionar tus proyectos y colaborar con otros desarrolladores de manera eficiente. 

## 1. Funciones Básicas de GitHub
GitHub proporciona una variedad de funciones para gestionar y colaborar en proyectos. Se debe aclarar que los comandos `git` te permiten gestionar y subir tu código, pero para tareas más específicas de GitHub (como issues y pull requests), `gh` es más apropiado. A continuación, se detallan algunas de las funciones más utilizadas:
####
| 1.1 Crear un Repositorio|
|:-----------------------:|

Para crear un repositorio desde la terminal, primero debemos autenticarnos con GitHub CLI (GitHub Command Line Interface) interactuar con GitHub desde la terminal:

1. Instalar GitHub CLI.
   ```bash
   sudo apt install gh  # Para sistemas basados en Debian/Ubuntu
   ```
- `sudo`: Ejecuta el comando con privilegios de superusuario.
- `apt`: Herramienta de gestión de paquetes para sistemas basados en Debian/Ubuntu.
- `install`: Indica que se instalará un paquete.
- `gh`: La herramienta de línea de comandos GitHub CLI para interactuar con GitHub.
2. Autenticarse con GitHub
   ```bash
   gh auth login  # Para sistemas basados en Debian/Ubuntu
   ```
- ``gh``: GitHub CLI.
- ``auth``: Subcomando para gestionar la autenticación.
- ``login``: Inicia el proceso de autenticación en GitHub.
3. Crear un repositorio.
   ```bash
   gh repo create nombre-del-repositorio --public  # --private para un repositorio privado
   ```
- `gh`: GitHub CLI.
- `repo`: Subcomando para trabajar con repositorios.
- `create`: Crea un nuevo repositorio.
- `nombre-del-repositorio`: Nombre del repositorio que se creará.
- `--public`: Opción que indica que el repositorio será público.
- `--private`: Opción que indica que el repositorio será privado.
####
| 1.2 Clonar un Repositorio|
|:-----------------------:|

1. Usar el comando git clone para clonar un repositorio:
   ```bash
   gh repo create nombre-del-repositorio --public  # --private para un repositorio privado
   ```
- `git`: Comando principal de Git.
- `clone`: Crea una copia local de un repositorio remoto.
- `https://github.com/usuario/repositorio.git`: URL del repositorio que se clonará
####
| 1.3 Subir Archivos a un Repositorio|
|:-----------------------:|
1. Añadir los archivos al área de preparación.
   ```bash
   git add .
   ```
- `git`: Comando principal de Git.
- `add`: Añade archivos al área de preparación.
- `.`: Indica que se deben añadir todos los archivos en el directorio actual.
2. Hacer un commit.
   ```bash
   git commit -m "Descripción de los cambios"
   ```
- `git`: Comando principal de Git.
- `commit`: Registra los cambios en el repositorio local.
- `-m`: Opción para añadir un mensaje de commit.
- `"Descripción de los cambios"`: Mensaje que describe los cambios realizados.

3. Subir los cambios al repositorio remoto.
   ```bash
   git push origin main  # Cambiar 'main' por el nombre de la rama que se desee
   ```
- `git`: Comando principal de Git.
- `push`: Envía los cambios al repositorio remoto.
- `origin`: Nombre del repositorio remoto (por defecto).
- `main`: Rama a la que se enviarán los cambios.
####
| 1.4 Crear y Gestionar Issues|
|:-----------------------:|

Los issues permiten rastrear tareas, mejoras y errores en tu proyecto.

1. Creación de issue. 
   ```bash
   gh issue create --title "Título del Issue" --body "Descripción del issue"
   ```
- `gh`: GitHub CLI.
- `issue`: Subcomando para trabajar con issues.
- `create`: Crea un nuevo issue.
- `--title`: Especifica el título del issue.
- `"Título del Issue"`: Título del issue.
- `--body`: Especifica el contenido del cuerpo del issue.
- `"Descripción del issue"`: Descripción del issue.
####
| 1.5 Crear un Pull Request|
|:-----------------------:|
1. Crear un pull request usando gh.
   ```bash
   gh pr create --base main --head rama-con-cambios --title "Título del Pull Request" --body "Descripción"
   ```
- `gh`: GitHub CLI.
- `pr`: Subcomando para trabajar con pull requests.
- `create`: Crea un nuevo pull request.
- `--base`: Indica la rama base a la que se hará el merge.
- `main`: Nombre de la rama base.
- `--head`: Especifica la rama con los cambios.
- `rama-con-cambios`: Nombre de la rama con los cambios.
- `--title`: Especifica título del pull request.
- `"Título del Pull Request"`: Título del pull request.
- `--body`: Especifica descripción del pull request.
- `"Descripción"`: Descripción de los cambios propuestos.

2. Crear un pull request desde el repositorio remoto mediante comandos de Git
   ```bash
   git pull origin main # Cambiar 'main' por el nombre de la rama que se desee
   ```
- `git`: Comando principal de Git.
- `pull`: Descarga cambios de un repositorio remoto y los fusiona con la rama actual.
- `origin`: Nombre del repositorio remoto.
- `main`: Rama de la que se descargan los cambios.
3. Realizar un commit de los cambios que se encuentran en el área de preparación de tu repositorio local
   ```bash
   git commit -m "Pull de actualización de prueba"
   ```
####
| 1.6 Revisar y Aceptar Pull Requests|
|:-----------------------:|
1. Listar pull requests
   ```bash
   gh pr list
   ```
- `gh`: GitHub CLI.
- `pr`: Subcomando para trabajar con pull requests.
- `list`: Lista los pull requests abiertos.
2. Revisar un pull request específico
   ```bash
   gh pr checkout número-o-id-del-pr
   ```
- `gh`: GitHub CLI.
- `pr`: Subcomando para trabajar con pull requests.
- `checkout`: Cambia a la rama asociada al pull request especificado.
- `número-o-id-del-pr`: ID del pull request.
3. Añadir comentarios o aprobar un pull request
   ```bash
   gh pr review --approve --body "Comentario opcional"
   ```
- `gh`: GitHub CLI.
- `pr`: Subcomando para trabajar con pull requests.
- `review`: Inicia una revisión de pull request.
- `--approve`: Aprueba el pull request.
- `--body`: Agrega un comentario a la revisión.
- `"Comentario opcional"`: Comentario de la revisión.
4. Fusionar un pull request
   ```bash
   gh pr merge número-o-id-del-pr
   ```
- `gh`: GitHub CLI.
- `pr`: Subcomando para trabajar con pull requests.
- `merge`: Fusiona el pull request especificado.
- `número-o-id-del-pr`: ID del pull request a fusionar.
## 2. Resultados, Ejemplos y Capturas de pantalla

<p align="center">
  <img src="./images/Clonar%20repositorio.png" alt="Clonar repositorio">
</p>
<p align="center"><em>Imagen 1: Clonar repositorio</em></p>

<p align="center">
  <img src="./images/Comprobar%20sincronia%20y%20actualizar%20repositorio.png" alt="Comprobar sincronia y actualizar repositorio">
</p>
<p align="center"><em>Imagen 2: Comprobar sincronía y actualizar repositorio local</em></p>

<p align="center">
  <img src="./images/Realizar%20cambios%20en%20repositorio%20local%20y%20actualizarlo.png" alt="Realizar cambios en repositorio local, actualizarlo y realizar pull requests">
</p>

<p align="center"><em>Imagen 3: Realizar cambios en repositorio local, actualizarlo y realizar pull requests</em></p>