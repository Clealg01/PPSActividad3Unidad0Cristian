# Instalación y Configuración de Git

En esta guía aparece todo los pasos a llevar a cabo para la instalación y configuración de Git en nuestros equipos, para comenzar a gestionar tus proyectos de manera eficiente. Principalmente usaremos un entorno Linux para gestionar Git, pero se explicará la instalación en otros entornos.


## 1. Instalación de Git

### En Windows:
1. Descarga el instalador de Git desde [git-scm.com](https://git-scm.com/).
2. Ejecuta el instalador y sigue las instrucciones del asistente de instalación.
3. Acepta las opciones predeterminadas a menos que necesites una configuración específica.
4. Verifica la instalación abriendo el **Símbolo del sistema** o **PowerShell** y ejecutando:
   ```bash
   git --version

### En Linux (Ubuntu/Debian):
1. Actualiza el índice de paquetes de tu sistema:
   ```bash
   sudo apt update
2. Instala Git:
   ```bash
   sudo apt install git
3. Verifica la instalación:
   ```bash
   git --version

### En macOS:
1. Instala Homebrew si no lo tienes:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

2. Instala Git con Homebrew:
   ```bash
   brew install git
3. Verifica la instalación:
   ```bash
   git --version

---

## 2. Instalación de PHP

### En Windows:
1. Descarga la última versión de PHP desde la [página oficial](https://www.php.net/downloads).
2. Extrae el contenido del archivo ZIP en una carpeta de tu elección, por ejemplo, `C:\php`.
3. Agrega la ruta de la carpeta de PHP a las variables de entorno:
   - Ve a *Configuración > Sistema > Información del sistema > Configuración avanzada del sistema*.
   - Haz clic en Variables de entorno y edita la variable `Path`.
   - Agrega `C:\php` a la lista de rutas y guarda los cambios.
4. Verifica la instalación abriendo el **Símbolo del sistema** o **PowerShell** y ejecutando:
   ```bash
   php --version

### En Linux (Ubuntu/Debian):
1. Actualiza el índice de paquetes de tu sistema:
   ```bash
   sudo apt update
2. Instala PHP:
   ```bash
   sudo apt install php
3. Verifica la instalación:
   ```bash
   php --version

### En macOS:
1. Instala Homebrew si no lo tienes:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

2. Instala PHP con Homebrew:
   ```bash
   brew install php
3. Verifica la instalación:
   ```bash
   php --version

---

## 3. Configuración inicial de Git

Después de instalar Git, es importante configurarlo con nuestro nombre y correo electrónico para que los commits estén correctamente identificados.
### Configuración global:
1. Configura tu nombre de usuario:
   ```bash
   git config --global user.name "Tu Nombre"

2. Configura tu dirección de correo electrónico:
   ```bash
   git config --global user.email "tuemail@ejemplo.com"
3. Verifica la instalación:
   ```bash
   git config --list

### Configuraciones adicionales
<div style="background-color: #f9f9f9; border-left: 6px solid #ffcc00; padding: 10px;">
  <strong>Nota:</strong> Estas configuraciones no serán utilizadas para la práctica, por lo que no se incluirán ejemplos al final del documento pero servirán de guía para futuros requerimientos.
</div>

1. Configuración del Editor de Texto preferido para redactar mensajes de commit:
   ```bash
   git config --global core.editor "vim" # O reemplaza "vim" con tu editor favorito (nano, code, etc.)

2. Configurar la Rama Predeterminada:
   ```bash
   git config --global init.defaultBranch main

---

## 4. Resultados, Ejemplos y Capturas de pantalla

<p align="center">
  <img src="./images/Descargar%20Git.png" alt="Descarga de Git">
</p>
<p align="center"><em>Imagen 1: Descarga de Git</em></p>

<p align="center">
  <img src="./images/Descargar%20php.png" alt="Descarga de PHP">
</p>
<p align="center"><em>Imagen 2: Descarga de Git</em></p>

> ⚠️ **Nota Importante:** En este caso se han instalado paquetes que nos permiten:
> - Servir contenido PHP a través de Apache (`libapache2-mod-php`).
> - Ejecutar scripts de PHP desde la línea de comandos (`php-cli`).
> - Asegurarse de que los archivos comunes necesarios para PHP estén presentes (`php-common`).
> 
> Esto es típico en configuraciones de desarrollo web, donde puedes necesitar probar aplicaciones localmente que dependen de un servidor web y también ejecutar scripts de mantenimiento o automatización en PHP desde la terminal.

<p align="center">
  <img src="./images/configuración%20de%20usuario%20y%20gmail%20de%20Git.png" alt="Configuración inicial de usuarios e email">
</p>

<p align="center"><em>Imagen 3: Configuración inicial de usuarios e email</em></p>

<p align="center">
  <img src="./images/Verificación%20de%20la%20configuracion%20de%20Git.png" alt="Verificación de la configuración inicial">
</p>
<p align="center"><em>Imagen 4: Verificación de la configuración inicial</em></p>