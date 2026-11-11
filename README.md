# Music para Android

Reproductor de música local. Funciona sin internet.

[Descargar Music.apk](https://github.com/Terwal912/music-updates/releases/latest/download/Music.apk) · [Versiones](https://github.com/Terwal912/music-updates/releases)

## Actualizaciones

La app comprueba nuevas versiones al abrirse, recuperar conexión o volver a primer plano, con un intervalo automático de 30 minutos. El botón de descarga de la biblioteca permite comprobar manualmente.

Descarga con progreso en segundo plano, verifica tamaño, SHA-256, paquete, versión y firma, y abre la confirmación del instalador de Android.

## Publicar una versión

1. Aumentar versionCode y versionName en android/version.properties del proyecto local.
2. Actualizar release-notes.txt y ejecutar tools/build-release.ps1.
3. Crear una Release con etiqueta v seguida de versionName, por ejemplo v1.2.0.
4. Adjuntar Music.apk y update.json generados juntos en releases/versionName, sin renombrarlos.
5. Publicar como última versión estable, sin marcar prerelease.

Manifiesto: https://github.com/Terwal912/music-updates/releases/latest/download/update.json

## Firma permanente

Mantener el paquete com.surco.musica y la misma clave de firma en todas las versiones. Guardar una copia privada de la clave y sus contraseñas. Nunca subir jks, keystore ni signing.properties.

La versión 1.1.0 inicia la firma permanente. Los APK anteriores de prueba tienen otra firma y no aceptan esta actualización directamente. No desinstalarlos sin guardar primero listas y favoritos.

Este repositorio contiene publicaciones e instrucciones. El código fuente y las credenciales de firma permanecen en el proyecto local.
