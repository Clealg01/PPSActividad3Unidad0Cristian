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

## 2. Configuración inicial de Git

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

### Resultados, Ejemplos y Capturas de pantalla
<p align="center">
  <img src="./images/Descargar%20php.png" alt="Descarga de PHP">
</p>