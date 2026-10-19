# Japanese Mastery · Lizeth

App web progresiva para celular, con el plan inicial del 19 al 25 de octubre de 2026. Reúne el repaso de Weeks 1–3 de Minna no Nihongo (capítulos 1–6), vocabulario contextual, gramática, lectura, escucha con voz del dispositivo, speaking, escritura breve, racha, tiempo de estudio y reporte exportable.

## Cómo abrir e instalar

- En PC: abre `index.html` en un navegador actual.
- En teléfono: publica la carpeta en HTTPS (por ejemplo GitHub Pages) y selecciona **Añadir a pantalla de inicio** desde el navegador. El modo PWA y el funcionamiento sin conexión requieren HTTPS o localhost.
- Las actividades también pueden usarse abriendo el HTML localmente, pero el modo PWA/micrófono depende del navegador y el origen.

## Progreso

El progreso queda en `localStorage` del dispositivo y navegador actual. En **Reporte** se puede descargar el registro o hacer/importar respaldo JSON. No hay cuentas ni sincronización en la nube.

## Alcance y siguientes semanas

La primera versión incluye un conjunto semilla de 31 palabras, gramática de vistazo y ejercicios de muestra para capítulos 1–6; es un reinicio utilizable, no un banco completo de preguntas JLPT. El contenido se puede ampliar en los arrays `vocab`, `grammar`, `kanji` y `questions` de `index.html`. Las preguntas son de práctica y no reproducen material protegido del examen.

La Web App no puede cambiar automáticamente el fondo real de bloqueo del teléfono y algunos móviles suspenden el audio con pantalla apagada. Las tarjetas permiten avance automático mientras la página permanece activa; para fondos hay que exportarlas o guardarlas como imágenes por separado.
