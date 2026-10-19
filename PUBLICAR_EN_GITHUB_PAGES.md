# Publicar Japanese Mastery en GitHub Pages

La app es estática y no necesita servidor propio. GitHub Pages la publica con HTTPS; el service worker guarda la app para abrirla sin conexión después de la primera visita online. El avance queda en el almacenamiento local del navegador de cada dispositivo y no se sube a GitHub.

## A. Crear un repositorio

1. Inicia sesión en [github.com](https://github.com/) y elige **+ → New repository**.
2. Usa el nombre `japanese-mastery` (o uno disponible de tu preferencia).
3. Selecciona **Public**. Con GitHub Free, Pages normalmente requiere que el repositorio sea público; el código y el sitio quedarán visibles para cualquiera con el enlace.
4. No añadas README, licencia ni `.gitignore`; pulsa **Create repository**.

## B. Subir solo los archivos de la app

1. En el Explorador abre `D:\DOCUMENTOS\JAPON 2027\MEXT Japanese\App`.
2. Selecciona los archivos que están directamente dentro de esa carpeta: `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png`, `.nojekyll` y los archivos `.md` de guía.
3. En GitHub, dentro del repositorio nuevo, elige **Add file → Upload files** y arrastra los archivos seleccionados.
4. Comprueba que `index.html` quede en la raíz del repositorio, no dentro de otra carpeta.
5. Pulsa **Commit changes**.

No subas toda la carpeta `MEXT Japanese`, tus libros PDF, los documentos de la beca ni materiales privados. Solo hace falta el contenido de `App`.

## C. Activar Pages

1. En el repositorio abre **Settings → Pages**.
2. En **Build and deployment**, elige **Deploy from a branch**.
3. Selecciona la rama `main` y la carpeta `/(root)`; pulsa **Save**.
4. En **Actions**, espera a que termine el despliegue con marca verde.
5. Vuelve a **Settings → Pages** y abre la URL que GitHub muestra. Tendrá una forma parecida a `https://TU-USUARIO.github.io/japanese-mastery/`.
6. Abre esa URL y confirma que aparece Japanese Mastery. Si GitHub ofrece **Enforce HTTPS**, déjalo activado.

## D. Instalar en el teléfono

Primero abre la URL publicada con internet y deja que termine de cargar una vez.

**Android (Chrome):** toca **⋮ → Instalar aplicación** o **Añadir a pantalla de inicio** y confirma. Luego abre la app desde su icono.

**iPhone (Safari):** toca **Compartir → Añadir a pantalla de inicio** y confirma. Luego abre la app desde su icono.

## E. Uso sin conexión y datos

Tras la primera carga online, el service worker almacena la interfaz y permite abrir las secciones principales sin conexión. Las voces dependen de las voces japonesas instaladas en el teléfono y pueden no estar disponibles offline. La grabación de voz requiere permiso de micrófono y HTTPS; lectura, tarjetas y ejercicios principales funcionan sin micrófono.

El progreso, la racha y los minutos se guardan en el almacenamiento local del navegador. En **Reporte → Respaldar** descarga el JSON antes de cambiar de teléfono, borrar datos del navegador o reinstalar la app. En el dispositivo nuevo usa **Importar** para recuperar el progreso. No existe sincronización en la nube.

## F. Publicar una actualización

Sube los archivos actualizados al mismo repositorio y confirma los cambios. Al abrir la app con internet, el service worker consulta la versión nueva de la página y la guarda para el siguiente uso sin conexión. Si la PWA mantiene una pantalla antigua, ciérrala por completo y vuelve a abrirla con internet.

## Si algo falla

- **404:** verifica que `index.html` está en la raíz y Pages usa `main` + `/(root)`.
- **No aparece instalar:** abre el sitio en HTTPS, recarga y prueba el menú del navegador; iPhone requiere Safari.
- **No abre offline:** visita el sitio online al menos una vez y vuelve a abrirlo desde el icono.
- **No se oye japonés:** activa una voz japonesa en el sistema o navegador; síntesis de voz puede depender de conexión.
- **Cambios antiguos:** cierra la PWA y vuelve a abrirla con internet.
