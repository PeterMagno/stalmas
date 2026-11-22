# Preguntas frecuentes (FAQ)

[English](faq.md)

### 1. ¿Es gratis?
Sí. **STALMAS Free** no tiene anuncios ni límite de tiempo. Incluye hasta **3 servidores** en total (Portainer y Linux por SSH, repartidos como quieras), todas las acciones sobre contenedores y stacks, registros (logs), terminal SSH (`xterm-256color`), widget Resumen en pantalla de inicio, bloqueo con PIN o biometría y el asistente de IA en la nube con Gemini (usando tu propia clave de API).

### 2. ¿Qué incluye Pro? ¿Es suscripción?
**No: STALMAS Pro es un pago único** ($14.99 USD de referencia en Google Play; el precio varía por país), sin suscripción ni renovaciones.

Pro desbloquea:
- **Servidores ilimitados**;
- **IA local en el teléfono** (modelos Gemma sin conexión) + modo Auto / IA Local primero, seudónimos reversibles de IP/host, notas por servidor, skills propias, 20 mensajes de memoria en la nube e historial completo buscable y exportable;
- **Diagnóstico IA en 1 toque** para contenedores con problemas, logs filtrados, archivos compose (aplicando mejoras al editor) y almacenamiento;
- **Alertas en segundo plano** por servidor o por contenedor individual («Avisarme si falla»);
- **Panel a tu medida e historial de uso** (gráficas CPU/RAM de 6 h / 24 h / 7 días, tarjetas Todos tus servidores, Diagnóstico IA, Últimas 24 h, Actividad y Tendencia);
- **Widget de un contenedor** con botón Reiniciar en tu pantalla de inicio;
- **Terminal Pro**: ver los 500 comandos del historial, snippets ilimitados con variables `{{nombre}}`, fila de teclas personalizable con cruceta de cursor y 16.000 caracteres de contexto para la IA;
- **Respaldo cifrado AES-256 en Google Drive** y **temas OLED, Catppuccin y STALMAS**.

Consulta el desglose completo en [Free vs Pro](free-vs-pro.es.md).

### 3. ¿Funciona con Portainer CE y BE?
Sí. STALMAS se conecta tanto a **Portainer CE** como a **Portainer BE** mediante la API pública de Portainer. En Portainer 2.45+ soporta *Git Sources* al crear stacks desde Git; en versiones anteriores usa URL de repositorio y token.

### 4. ¿Necesito abrir puertos?
No. La app se conecta **directamente desde tu teléfono** a tu Portainer o servidor SSH, sin servidores intermedios. Para acceder desde fuera de tu red local sin abrir puertos a internet, usa una **VPN** (como WireGuard o Tailscale) o un túnel cifrado.

Ten en cuenta que `http://` sin cifrar está bloqueado para direcciones públicas y solo se permite en redes privadas o locales (`localhost`, `.local`, `10.x.x.x`, `172.16.x.x–172.31.x.x`, `192.168.x.x`).

### 5. ¿Dónde se guardan mis credenciales?
Solo en tu teléfono, cifradas. STALMAS no tiene cuentas de usuario ni servidores propios. Tus credenciales, llaves SSH, tokens de Portainer, historial y tu clave de Gemini se guardan localmente en una base de datos **SQLCipher (AES-256)** y preferencias cifradas con **AES-256-GCM**, con claves protegidas por el Android Keystore. La copia automática de Android está desactivada.

### 6. ¿La IA ve mis datos?
Antes de enviar nada a Gemini en la nube, STALMAS pasa el texto por un **portero de privacidad** que oculta automáticamente direcciones IPv4/IPv6, dominios, URLs, contraseñas, tokens, claves y cadenas de conexión (y te avisa cuántos datos se ocultaron). En **Pro**, los seudónimos reversibles hacen que Gemini solo vea etiquetas como `[IP_1]` mientras tú ves tus IP reales en pantalla (los secretos nunca vuelven), o puedes usar **IA local** para que nada salga del teléfono.

*Importante:* la ocultación automática es una protección, no una garantía; evita escribir secretos directamente en el chat.

### 7. ¿Necesito una clave de Gemini?
Sí, si quieres usar la **IA en la nube** (tanto en Free como en Pro funciona con tu propia clave —**BYOK**— de Google AI Studio, según la cuota de tu clave). Si tienes **Pro** y usas un modelo de **IA local** en un teléfono compatible, no necesitas clave de Gemini ni conexión a internet para la inferencia.

### 8. ¿Qué teléfono necesito para la IA local?
Necesitas **Android 12+** y un procesador de **64 bits** (`arm64-v8a` o `x86_64`), además de:
- **6 GB de RAM** como mínimo para Gemma 4 E2B, u **8 GB de RAM** para Gemma 4 E4B;
- **Espacio libre** suficiente (tamaño del modelo + 500 MB).

*Las funciones disponibles dependen del hardware de tu equipo.* Si falta soporte de 64 bits, RAM o espacio, la app desactiva o bloquea las descargas incompatibles explicando el motivo.

### 9. ¿Hay versión iOS?
No por ahora. STALMAS está disponible únicamente para **Android 12 o superior**.

### 10. ¿Es de código abierto?
No. STALMAS es software comercial de código cerrado desarrollado por **Peter Magno**. Este repositorio público existe para que la comunidad pueda reportar fallos, proponer ideas, resolver dudas y seguir las notas de cada versión.

### 11. ¿Cómo reporto un fallo?
Tienes dos formas:
1. Abre un [Reporte de fallo](../../../issues/new?template=bug_report.yml) en este repositorio indicando versión de la app, teléfono, versión de Android y pasos para reproducirlo. **Nunca pegues contraseñas, tokens de API, llaves SSH, IPs reales ni dominios privados.**
2. Desde la propia app, ve a **Ajustes → Acerca de y legal → Reportar un problema**. STALMAS prepara un borrador revisable hacia `report@stalmas.app` con los datos sensibles ocultos automáticamente.

### 12. ¿Cómo pido borrar mis datos?
No hay cuentas ni base de datos central que borrar:
- **En tu teléfono:** desinstala STALMAS o ve en Android a **Ajustes → Aplicaciones → STALMAS → Almacenamiento → Borrar datos**.
- **Copia en Google Drive (Pro):** bórrala desde los ajustes de copia en la nube en la app, o desde tu cuenta de Google (**Administrar datos de apps → STALMAS → Eliminar datos**).
- **Correos, reportes o inscripción de testers:** escribe a **support@stalmas.app** desde la misma dirección que usaste.

Instrucciones completas: [stalmas.app/es/delete-data/](https://stalmas.app/es/delete-data/).
