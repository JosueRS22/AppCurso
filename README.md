# Curso Electron

## settings.json
Modifica características de apariencia de VScode.

## Aplicación

La aplicación incluye la creación de:
-package.json 
-package-lock.json 
por medio del comando npm init, donde se agrega información acerca del proyecto.

### index.html

Este archivo HTML es la interfaz principal de una aplicación construida con Electron. Muestra un mensaje "Hello, World!" y, mediante un script externo (renderer.js), inserta dinámicamente las versiones de Node.js, Chromium y Electron utilizadas.

### main.js

Este archivo es el script principal de una aplicación Electron. 

Utiliza los módulos app y BrowserWindow para crear una ventana de la aplicación de escritorio. 

Cuando Electron está listo (app.whenReady()), se ejecuta la función crearVentanaPrincipal, que abre una ventana de 800x600 píxeles y carga el archivo index.html como interfaz. 

También configura un archivo de precarga (preload.js) que puede usarse para comunicar el backend de Node.js con el frontend. 

La función createWindow() parece un error, ya que no está definida, lo cual podría causar problemas si no se corrige.

### preload.js
Aquí se crea la función para obtener el id de los elementos span de los módulos deseados.

El archivo utiliza un evento que indica que el DOM se ha cargado correctamente. Según el id recuperado, obtiene el número de versión de módulo correspondiente.
