# Carrera al Vacío — APK para Android

Proyecto Android que abre el videojuego HTML/CSS/JavaScript en una WebView. Incluye la interfaz espacial, nave, La Sombra, puntuación, vidas, turbo, pulso EMP y cinco niveles.

## Estructura importante

- `app/src/main/java/.../MainActivity.java`: pantalla Android que abre el juego.
- `app/src/main/AndroidManifest.xml`: configuración de la aplicación.
- `app/src/main/assets/index.html`: interfaz del juego.
- `app/src/main/assets/css/style.css`: estilos.
- `app/src/main/assets/js/game.js`: funcionamiento del juego.
- `.github/workflows/build-apk.yml`: compilación automática en GitHub Actions.

## Cómo subirlo a GitHub

1. Descarga y descomprime este ZIP.
2. En el repositorio `CarreraAlVacio`, sube **el contenido** de esta carpeta a la raíz del repositorio; no subas el ZIP como único archivo.
3. Asegúrate de que la ruta `.github/workflows/build-apk.yml` se conserve exactamente así.
4. Confirma los cambios (`Commit changes`).
5. Abre `Actions` y selecciona `Build Carrera al Vacio APK`. Ejecuta `Run workflow` si no comenzó automáticamente.
6. Cuando el trabajo termine con marca verde, entra en la ejecución y descarga el artefacto `CarreraAlVacio-APK`.
7. El ZIP del artefacto contiene `app-debug.apk`.

## Requisitos y notas

- GitHub Actions necesita internet para descargar Gradle y los componentes Android.
- El archivo generado es un APK de depuración para pruebas, no un paquete firmado para publicar en Google Play.
- Si ya tienes archivos sueltos en la raíz del repositorio, reemplázalos por esta estructura correcta. No dejes `AndroidManifest.xml` o `MainActivity.java` sueltos en la raíz: deben quedar dentro de `app/src/main/`.
