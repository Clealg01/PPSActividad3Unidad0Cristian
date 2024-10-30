| UTILIZACIÓN DE KEEPASS |
|:-----------------------:|

<h1 style="text-align: center; text-decoration: underline;">UTILIZACIÓN DE KEEPASS</h1>

# UTILIZACIÓN DE KEEPASS
---


<h3 style="text-align: center;">Paso 1: Descarga de la plicación</h3>

==================
UTILIZACIÓN DE KEEPASS
==================

Para comenzar debemos instalar la aplicación de keepass en nuestro sistema. En este caso, utillizaremos un sistema Windows para poder realizar la práctica, puesto que en Linux el plugin que utilizaremos para sincronizar las bases de datos con el Drive no funciona correctamente y genera problemas. 

![Imagen 1: Creación de carpetas](./keepass_caps/descarga%20de%20plugin.PNG)
# UTILIZACIÓN DE KEEPASS
---
<p align="center">
  <img src="./keepass_caps/descarga%20de%20plugin.PNG" alt="Texto alternativo">
</p>
<div style="text-align: center;">
  <em>Imagen 1: Creación de carpetas</em>
</div>

<h3 style="text-align: center;">Paso 2: Crear archivo "docker-compose.yaml"</h3>

He creado una carpeta en documentos llamada PPS, para actividades de la asignatura. Creamos una carpeta para docker y dentro creamos una carpeta específica para codiMD.

Dentro de la carpeta codimd, creamos un archivo llamado docker-compose.yaml para descargar los repositorios y levantar el contenedor para la práctica, con el siguiente código, utilizando la herramienta nano para modificar el archivo:
    
```yaml
version: '3'
services:
  database:
    image: postgres:9.6
    environment:
      POSTGRES_DB: hackmd
      POSTGRES_USER: hackmd
      POSTGRES_PASSWORD: password
    volumes:
      - database:/var/lib/postgresql/data
  codimd:
    image: quay.io/codimd/server:latest
    depends_on:
      - database
    environment:
      CMD_DB_URL: postgres://hackmd:password@database:5432/hackmd
      CMD_USECDN: "true"
    ports:
      - "3000:3000"
    volumes:
      - uploads:/codimd/public/uploads
volumes:
  database:
  uploads:
```

![](/uploads/upload_a7e888f7e0d12bd2ffbc02d893f16ddd.png)
<div style="text-align: center;">
  <em>Imagen 2: Creación de archivo docker-compose.yaml</em>
</div>

<h3 style="text-align: center;">Paso 3: Descargar y levantar repositorio</h3>

Una vez hemos creado el archivo descargamos el repositorio y levantamos el repositorio de docker mediante el comando ```docker-compose up -d```:

![](/uploads/upload_fcf76516c73d0394f8513f16e6abe6cb.png)
<div style="text-align: center;">
  <em>Imagen 3: Descargar y levantar repositorio</em>
</div>

<h3 style="text-align: center;">Paso 4: Acceder al repositorio y crear cuenta de codiMD</h3>

Una vez levantado, entramos en el repositorio por el puerto 3000 y nos creamos una cuenta para codiMD

![](/uploads/upload_de6e601134919952ec66cb50bdb4f2ec.png)
<div style="text-align: center;">
  <em>Imagen 4: Creación de cuenta para codeMC</em>
</div>

<h3 style="text-align: center;">Paso 5: Crear documentación</h3>
    
Por último, procedemos a realizar la documentación del informe mediante el uso de etiquetado con codiMC. Es importante ayudarse de guías para aprender la sintaxis del lenguaje

    
| ![](/uploads/upload_930f782caf98db7c4e616bb9720a4b61.png) | ![](/uploads/upload_e52271116bde81accc1676c2551cdfba.png) |
|:---------------------------------------------------------:|:---------------------------------------------------------:|
<div style="text-align: center;">
  <em>Imagen 5: Creación de docimentación con codeMC y uso de guías</em>
</div> <p>

A continuación, dejo algunas de las etiquetas más usadas para esta práctica, como ejemplos:
    
**1. Inclusión de imágenes en la documentación:**
   - <u>Incluir imágenes:</u>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`![Imagen 1](ruta/de/imagen1.png)`

   - <u>Juntar imagenes, una tras otra:</u>
```
    | ![Imagen 1](ruta/de/imagen1.png) | ![Imagen 2](ruta/de/imagen2.png) |
    | :---------------------------------: | :---------------------------------: |
```        
**2. Inclusión de leyendas para las imágenes:**
   - <u>Centrado de leyendas:</u>
```
    <div style="text-align: center;">
       Leyenda centrada de la imagen
    </div>
```
     
**3. Inclusión de encabezados**
   - <u>Título principal</u>
       `# Título principal`
       
   - <u>Subtítulos</u>
       `### Título secundario`

**4. Uso de <em>Italics</em>**
   - <u><em>Cursiva</em></u>
       `<em>texto en cursiva</em>`
       
   - <u>**Negrita**</u>
       `**Texto en Negrita**`

   - <u>`Código`</u>
       `'Texto en código'`
   - <u>Subrayado</u>
       `<u>Texto subrayado</u>`