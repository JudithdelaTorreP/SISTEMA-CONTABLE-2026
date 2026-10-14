DESPACHO CONTABLE PWA · VERSIÓN 0.29

1. Publique todos los archivos y la carpeta icons en el mismo directorio de su hosting.
2. El sitio debe abrir mediante HTTPS. Para pruebas locales también puede utilizar localhost.
3. Abra index.html en Chrome, Edge o Safari.
4. Use la invitación flotante o ingrese a Configuración > PWA y alertas.
5. Autorice las notificaciones por separado en cada dispositivo.

ARCHIVOS NECESARIOS
- index.html: sistema contable.
- manifest.webmanifest: información de instalación.
- sw.js: servicio PWA, caché básica y apertura de notificaciones.
- icons/: iconos de la aplicación.

COMPORTAMIENTO DE ALERTAS
- Apagadas: no presenta avisos automáticos.
- Solo una al día: agrupa los pendientes en un resumen diario.
- Solo ventana: muestra el centro de alertas dentro del sistema.
- Todo encendido: muestra la ventana interna y una notificación del dispositivo.

La revisión automática se ejecuta mientras el sistema está abierto. Para enviar avisos con
la aplicación completamente cerrada será necesario agregar Firebase Cloud Messaging y un
servicio servidor que genere las notificaciones push.

La invitación automática de instalación aparece hasta tres veces por huella anónima de IP.
Si no es posible obtenerla, el límite se aplica al navegador actual. Cuando el usuario inicia
sesión, el contador anónimo también se sincroniza con los demás datos de su cuenta.
