## 1. Funciones Básicas de GitHub
En este archivo se explicará el proceso completo para comenzar a usar la plataforma GitHub. Iniciaremos con la apertura de una cuenta y el proceso de inicio de sesión, detallando los pasos necesarios para registrarse y acceder de forma segura.

También se incluirá una sección dedicada a las claves SSH, explicando qué son, por qué son importantes para la autenticación sin contraseñas y cómo generar y agregar una clave SSH a tu cuenta de GitHub para asegurar tus interacciones desde la línea de comandos
####
| 1.1 Crear una Cuenta en GitHub|
|:-----------------------:|
1. Accede a la página de registro de GitHub:
   - Visita [github.com](https://github.com) y haz clic en **Sign up** (Registrarse).
2. Rellena el formulario de registro:
   - Introduce tu dirección de correo electrónico, elige un nombre de usuario y crea una contraseña segura.
   - Sigue las instrucciones de verificación para confirmar que no eres un robot y haz clic en **Create account** (Crear cuenta).
3. Verifica tu correo electrónico:
   - Revisa tu bandeja de entrada y haz clic en el enlace de verificación enviado por GitHub para confirmar tu dirección de correo.
####
| 1.2 Iniciar sesión en la cuenta de GitHub|
|:-----------------------:|
1. Accede a la página de inicio de sesión de GitHub:
   - Ve a [github.com](https://github.com) y haz clic en **Sign in** (Iniciar sesión).
2. Introduce tus credenciales:
   - Escribe tu nombre de usuario o correo electrónico y tu contraseña.
   - Haz clic en **Sign in**.
3. **Recomendación**: Habilitar la autenticación de dos factores (2FA) 
   - Ve a **Settings** > **Security** > **Enable two-factor authentication** para añadir una capa extra de seguridad a tu cuenta.
####
| 1.3 Crear un Repositorio|
|:-----------------------:|
1. Haz clic en el botón **+** en la esquina superior derecha y selecciona **New repository** (Nuevo repositorio).
2. Completa los campos con la siguiente información:
   - **Repository name** (Nombre del repositorio).
   - **Description** (Descripción) opcional.
   - Elige si el repositorio será **Public** (público) o **Private** (privado).
3. Haz clic en **Create repository** para finalizar.
####
| 1.4 Clonar un Repositorio|
|:-----------------------:|

Para trabajar con un repositorio localmente:
1. Copia la URL del repositorio desde la página principal del mismo.
2. En tu terminal, ejecuta:
   ```bash
   git clone https://github.com/usuario/repositorio.git
   ```
###
| 1.5 Subir Archivos a un Repositorio|
|:-----------------------:|
1. Ve al repositorio y selecciona **Add file** > **Upload files**.
2. Arrastra y suelta los archivos o selecciona los archivos desde tu equipo.
3. Haz clic en **Commit changes** para confirmar.
###
| 1.6 Crear y Gestionar Issues|
|:-----------------------:|

Los issues permiten rastrear tareas, mejoras y errores en tu proyecto.

1. Ve a la pestaña **Issues** y haz clic en **New issue**.
2. Escribe un título y una descripción del problema o tarea.
3. Asigna etiquetas y personas responsables si es necesario.
4. Haz clic en **Submit new** issue para crearla.
###
| 1.7 Crear un Pull Request|
|:-----------------------:|

Los pull requests permiten colaborar en proyectos mediante la propuesta de cambios.

1. Ve a la pestaña **Pull requests** y haz clic en **New pull request**.
2. Selecciona la rama con tus cambios y la rama en la que deseas fusionarlos
3. Revisa los cambios y haz clic en **Create pull request**.
4. Añade una descripción y envía el pull request.
###
| 1.8 Revisar y Aceptar Pull Requests|
|:-----------------------:|
1. Ve al pull request creado.
2. Haz clic en **Files changed** para revisar los cambios.
3. Usa **Review changes** para comentar, aprobar o solicitar cambios.
4. Una vez aprobado, haz clic en **Merge pull request** y luego en **Confirm merge** para fusionar los cambios.
###
|1.9 Configuración de Claves SSH|
|:-----------------------:|
1. Verificar si Ya Tienes Claves SSH.
   ```bash
   ls -al ~/.ssh
- `ls`: Comando para listar el contenido de un directorio.
- `-al`: Opción combinada que muestra todos los archivos (incluidos los ocultos) en formato de lista detallada.
- `~/.ssh`: Ruta al directorio .ssh en el directorio de inicio del usuario, donde se almacenan las claves SSH.
2. Generar un par de claves SSH.
   ```bash
   ssh-keygen -t rsa -b 4096 -C "tuemail@ejemplo.com"
   ```
- `ssh-keygen`: Comando para generar un par de claves SSH.
- `-t`: Opción para especificar el tipo de clave.
- `rsa`: Tipo de algoritmo de cifrado para la clave.
- `-b`: Opción para especificar el tamaño en bits de la clave.
- `4096`: Tamaño de la clave en bits, lo que la hace más segura.
- `-C`: Opción para añadir un comentario a la clave (usualmente un correo electrónico).
- `"tuemail@ejemplo.com"`: Comentario que ayuda a identificar la clave, generalmente es un correo electrónico.
3. Iniciar el agente SSH y añadir la clave privada.
   ```bash
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_rsa
- `eval`: Ejecuta el comando que se pasa como argumento.
- `"$(ssh-agent -s)"`: Comando que inicia el agente SSH en segundo plano.
- `ssh-agent -s`: Comando que devuelve el proceso del agente SSH en ejecución.
- `ssh-add`: Comando que añade la clave privada al agente SSH.
- `~/.ssh/id_rsa`: Ruta al archivo de la clave privada.
4. Copiar la clave pública.
   ```bash
   cat ~/.ssh/id_rsa.pub
- `cat`: Comando que muestra el contenido de un archivo.
- `~/.ssh/id_rsa.pub`: Ruta al archivo de la clave pública.

5. Agregar la Clave SSH a Tu Cuenta de GitHub
   - En la página de GitHub, ir a **Configuración** > **SSH and GPG keys**.
   - Clic en **New SSH key**.
   - Pegar la clave pública copiada en el paso anterior en el campo **Key**.
   - Dar un título a la clave (por ejemplo, "Clave SSH de mi PC") y dar clic en **Add SSH key**.
6. Verificar la Conexión con GitHub.
   ```bash
   ssh -T git@github.com
- `ssh`: Comando para iniciar una conexión SSH.
- `-T`: Opción que evita la ejecución de comandos remotos, útil para verificar conexiones.
- `git@github.com`: Dirección del servidor GitHub para la autenticación.

## 2. Capturas y ejemplos

<p align="center">
  <img src="./images/Dar%20alta%20en%20github.png" alt="Dar alta en github">
</p>
<p align="center"><em>Imagen 1: Crear una Cuenta en GitHub</em></p>

<p align="center">
  <img src="./images/Iniciar%20sesion%20en%20github.png" alt="Iniciar sesion en github">
</p>
<p align="center"><em>Imagen 2: Iniciar sesion en github</em></p>

<p align="center">
  <img src="./images/Crear%20repositorio%20Github.png" alt="Crear repositorio Github">
</p>

<p align="center"><em>Imagen 3: Crear repositorio Github</em></p>

<p align="center">
  <img src="./images/Configurar%20repositorio%20Github.png" alt="Configurar repositorio Github">
</p>

<p align="center"><em>Imagen 4: Configurar el respositorio desde la interfaz gráfica Github</em></p>

<p align="center">
  <img src="./images/Comprobar%20claves%20SSH%20y%20crearlas.png" alt="Comprobar claves SSH y crearlas">
</p>

<p align="center"><em>Imagen 5: Comprobar (clave pública) y crear (clave privada) claves SSH</em></p>

<p align="center">
  <img src="./images/Agregar%20SSH%20publica.png" alt="Agregar SSH publica">
</p>

<p align="center"><em>Imagen 6: Agregar SSH pública</em></p>

<p align="center">
  <img src="./images/Verificar%20cuenta%20SSH%20agregada.png" alt="Verificar cuenta SSH agregada">
</p>

<p align="center"><em>Imagen 7: Verificar estado de las claves</em></p>

<p align="center">
  <img src="./images/Añadir%20un%20nuevo%20archivo%20al%20repositorio.png" alt="Añadir un nuevo archivo al repositorio">
</p>

<p align="center"><em>Imagen 8: Añadir un nuevo archivo al repositorio remoto desde interfaz</em></p>

<p align="center">
  <img src="./images/Crear%20pull%20Request%20entre%20ramas.png" alt="Crear pull Request entre ramas">
</p>

<p align="center"><em>Imagen 9: Crear pull Request entre ramas</em></p>