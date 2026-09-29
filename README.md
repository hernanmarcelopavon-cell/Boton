# Botón de Pánico (Android, Kotlin)

1. Abrir la carpeta en Android Studio (Hedgehog o posterior) y dejar que sincronice Gradle.
2. Conectar el celular (depuración USB) y ejecutar, o Build > Build APK.
3. En el primer uso: aceptar permisos (SMS, llamadas, ubicación, estado del teléfono).
4. "Configurar contactos": cargar 3 números, mensaje y segundos de espera.

Flujo: botón AYUDA -> cuenta regresiva (cancelable) -> SMS con ubicación a los 3 -> llamada al contacto 1;
si corta antes de 20 s (no atendió), llama al 2, y luego al 3.

Notas: instalar por APK directo (sideload). Google Play restringe los permisos SMS/llamadas.
Sin plan de datos ni SMS/saldo, el envío falla. Probar antes con los contactos reales.

## Compilar sin Android Studio (GitHub Actions)
1. Crear cuenta gratis en github.com y un repositorio nuevo (privado está bien).
2. Subir TODO el contenido de esta carpeta (incluida la carpeta oculta .github) a la rama main.
3. Pestaña Actions > "Compilar APK" > esperar el tilde verde (5-10 min).
4. Entrar a esa ejecución y descargar "BotonPanico-APK" (zip que contiene app-debug.apk).
