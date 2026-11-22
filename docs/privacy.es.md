# Resumen de privacidad

[English](privacy.md) · [Política de privacidad completa](https://stalmas.app/es/privacy/) · [Eliminación de datos](https://stalmas.app/es/delete-data/)

STALMAS **no tiene cuentas de usuario** ni **servidores propios que guarden tus datos**. Todo vive en tu teléfono, cifrado, y el desarrollador (**Peter Magno**) no puede verlo.

## Dónde va cada dato

| Dato | Dónde está | ¿Lo recibe el desarrollador? |
|---|---|---|
| Servidores, claves SSH, contraseñas, tokens, historial, chats de IA | Tu teléfono, cifrado (SQLCipher AES-256 y preferencias AES-256-GCM con Android Keystore; copia automática de Android desactivada) | **No** |
| Copia en Google Drive (opcional, Pro) | Carpeta privada de la app en tu Drive (`drive.appdata`), cifrada con tu contraseña | **No** (si olvidas la contraseña, no se puede recuperar) |
| Consultas a Gemini (opcional) | Servidores de Google, con tu propia clave de API (BYOK) | **No** |
| Descarga de modelos de IA local (opcional, Pro) | Descarga directa desde Hugging Face (catálogo anónimo desde `stalmas.app`) | **No** |
| Correos de soporte, informes de problemas y reportes de IA | Nuestro buzón (`support@stalmas.app` / `report@stalmas.app`) | **Sí, solo lo que tú eliges enviar** (borrador revisable desde tu app de correo) |
| Inscripción como tester (correo + alias) | Nuestro buzón (`testers@stalmas.app`) y la lista de Google Play | **Sí, solo para la prueba cerrada** (se borra máx. 30 días después de terminar) |
| Pagos | Google Play | **No** (nunca vemos tu tarjeta) |

## Garantías clave
- **Sin analíticas, sin publicidad, sin rastreo, sin perfiles ni venta de datos.**
- **Conexión directa a tus servidores:** tu teléfono habla directamente con tus instancias Portainer y SSH; el HTTP sin cifrar solo se permite en redes privadas o locales.
- **Portero de privacidad:** antes de enviar consultas a Gemini, STALMAS oculta IPs, dominios, URLs, contraseñas, claves y cadenas de conexión (también al preparar borradores de reportes). Es una medida de mitigación, no una garantía: revisa siempre el texto antes de enviar.
- **Permisos mínimos de Android:** Internet y estado de red, notificaciones (descarga de modelos y alertas de contenedores) y servicio en primer plano `dataSync` (completar descargas de modelos locales). Sin acceso a ubicación, contactos, fotos, cámara ni micrófono.

Para conocer los detalles legales completos, plazos de conservación y tus derechos, consulta la [Política de privacidad](https://stalmas.app/es/privacy/).
