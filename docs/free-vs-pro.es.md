# Free vs Pro

[English](free-vs-pro.md) · [Versión web](https://stalmas.app/es/docs/free-pro/)

> **Las funciones disponibles dependen del hardware de tu equipo.**

**STALMAS Free** cubre la administración diaria completa de hasta **3 servidores en total** (Portainer y SSH, repartidos como quieras), sin anuncios ni límite de tiempo.

**STALMAS Pro** es un **pago único de $14.99 USD** de referencia en Google Play, **sin suscripciones ni renovaciones** (el precio varía por país y Google Play muestra el importe final en tu moneda). Quienes ya tienen Pro pueden dejar además una propina opcional desde *Acerca de* (no desbloquea funciones adicionales).

## Conexiones

| Función | Free | Pro |
|---|---|---|
| Servidores Portainer y Linux por SSH (contraseña o llave `.pem`/`.key`) | 3 en total, repartidos como quieras | Ilimitados |
| Estado UP/DOWN de cada servidor | Sí | Sí |
| Aceptar certificado TLS auto-firmado (por servidor Portainer) | Sí | Sí |

## Portainer: panel, contenedores y stacks

| Función | Free | Pro |
|---|---|---|
| Panel por tarjetas (fijo): Salud, Recursos en vivo (CPU/RAM/imágenes), Más consumo, Almacenamiento (espacio recuperable), Accesos rápidos | Sí | Sí |
| Panel a tu medida: editar (subir/bajar, quitar, añadir), plantillas Salud/Operaciones, tarjeta «Contenedores por stack» | Candado | Sí |
| Tarjetas Pro del panel: «Todos tus servidores» (salud de cada servidor guardado) y «Diagnóstico IA» | Candado | Sí |
| Tarjetas Pro «Últimas 24 h» (CPU/RAM del host con pico), «Actividad» (lo que detectó la vigilancia incluso con la app cerrada), «Tendencia» (contenedor que llegará antes a su límite de memoria); plantilla «Actividad» | Candado | Sí |
| Historial de uso: guardar CPU/RAM de hasta 30 contenedores por entorno en cada revisión (7 días, cifrado, opcional en Vigilancia) | Candado | Sí |
| Historial en el detalle del contenedor: CPU y RAM de las últimas 6 h / 24 h / 7 días con mín., media y máx. (sigue al contenedor aunque se recree) | Candado | Sí |
| Iniciar, parar, reiniciar, pausar y reanudar contenedores | Sí | Sí |
| Detalle de contenedor: cabecera con estado en color, enlace a su stack y acciones Reiniciar · Detener/Iniciar · Consola · Procesos; pestañas Resumen · Logs · Uso · Config | Sí | Sí |
| Resumen: motivo del fallo (salida del healthcheck, *Out of memory* con límite, código de salida explicado) con Reiniciar / Ver errores; IP para copiar, puertos, reinicios y política, creado hace…, CPU/RAM | Sí | Sí |
| Resumen: «Avisarme si falla» de un solo contenedor (avisa aunque la vigilancia general esté apagada; se gestiona en Vigilancia) | Candado | Sí |
| Resumen: «Añadir a la pantalla de inicio» (widget de ese contenedor ya configurado) | Candado | Sí |
| Config: General, Recursos, Healthcheck, Red y puertos (nombre de red pulsable → Redes), Volúmenes, Entorno (secretos ocultos) y Etiquetas | Sí | Sí |
| Renombrar contenedor | Sí | Sí |
| Actualizar un contenedor a la última imagen: descarga, compara y recrea con la misma configuración; si es de un stack de Portainer, ofrece redesplegar todo el stack con imágenes nuevas | Sí | Sí |
| Matar (*kill*) y eliminar contenedor, confirmando por nombre | Sí | Sí |
| Uso en vivo: gráficas de CPU/RAM, red, disco y PIDs; lista de procesos | Sí | Sí |
| Selección múltiple: iniciar, reiniciar o detener varios contenedores | Sí | Sí |
| Contenedores: cifras tocables como filtro (Todos / Sanos / Problemas / Detenidos), búsqueda por nombre, imagen o puerto, vistas Prioridad («Necesitan atención») y Por stack, CPU/RAM por fila | Sí | Sí |
| Contenedores: botón «Explicar» en cada problema (abre el diagnóstico IA con sus logs) | Candado | Sí |
| Alertas en segundo plano: avisa si un contenedor se detiene, se reinicia de forma inesperada, queda *unhealthy* o se reinicia sin parar, y si cae un entorno (revisión cada 15–60 min, no en tiempo real) | Candado | Sí |
| Widgets de inicio: Resumen (en ejecución / detenidos / con problemas; servidor activo) | Sí | Sí |
| Widgets de inicio: un contenedor con botones Reiniciar y Refrescar, hora de actualización y elegir cualquier servidor | Candado | Sí |
| Logs: ANSI, búsqueda, líneas de error y aviso resaltadas; barra de iconos: en vivo, filtros (20 a 10.000 líneas, periodo o rango de fechas, marcas de tiempo), Todos / Errores / Avisos con cifra, copiar, exportar `.log` / compartir, ir al primer error | Sí | Sí |
| Consola dentro del contenedor (`exec`) | Sí | Sí |
| Analizar logs con IA en 1 toque: envía SOLO las líneas del filtro actual (máx. 100) y dice qué se envió; «Explicar» en Resumen y listas filtra Errores y analiza | Candado (en Free se pegan a mano) | Sí |
| Ver stacks y su compose/ENV (solo lectura) | Sí | Sí |
| Stacks: salud real por contenedores (barra de estado), cifras tocables como filtro (Todos / Problemas / Sanos / Inactivos), acción en el sitio que arregla el fallo, redesplegar (con confirmación), iniciar, detener (con confirmación) y eliminar stack (pidiendo el nombre), logs y «Contenedores sin stack» | Sí | Sí |
| Stacks: botón «¿Por qué falla X?» (abre el diagnóstico IA del contenedor con problema) | Candado | Sí |
| Detalle de stack: Resumen / Compose / Variables; Git (traer cambios, configuración) | Sí | Sí |
| Crear stacks nuevos (Editor) | Sí | Sí |
| Crear stack desde Git (Source en Portainer 2.45+, URL y token en antiguas) | Sí | Sí |
| Nuevo stack desde plantilla (Portainer y personalizadas) | Sí | Sí |
| Analizar el compose con IA y aplicar mejoras al editor | Candado | Sí |
| Almacenamiento: imágenes y volúmenes (ver, quién los usa, eliminar, liberar espacio, descargar última versión) | Sí | Sí |
| «¿Qué es seguro borrar?» (IA) | Candado | Sí |
| Pestaña Recursos: tarjeta de espacio, Limpiar (*prune* de imágenes, volúmenes, redes y caché) y entradas a Imágenes, Volúmenes y Redes | Sí | Sí |
| Redes (solo lectura): búsqueda por red o contenedor, filtro Todas / Sin uso, subred (copiar), gateway, ámbito y contenedores miembros (también desde Config del contenedor) | Sí | Sí |

## Terminal (SSH y consola de contenedores)

| Función | Free | Pro |
|---|---|---|
| Emulador `xterm-256color` con teclas Esc/Tab/Ctrl y flechas | Sí | Sí |
| Copiar el último resultado | Sí | Sí |
| Historial de comandos por servidor (se guardan hasta 500) | Ve los 50 más recientes | Ve los 500 |
| Snippets guardados | Hasta 10, sin variables | Ilimitados, con variables `{{nombre}}` |
| Fila de teclas personalizable con cruceta de cursor | Candado | Sí |
| Mantener pantalla encendida | Sí | Sí |
| La IA lee tu pantalla de terminal | Hasta 4.000 caracteres | Hasta 16.000 (nube) · 1.500 (local) |

## Asistente de IA

### Base común (Free y Pro)
| Función | Límite / detalle |
|---|---|
| Asistente flotante STALMAS (personaje): burbuja movible visible por defecto que sube sobre el teclado; panel anclado no modal que se amplía y cambia de alto; historial dentro del panel; vista previa con ▶ / Aplicar; se recoge solo al ejecutar o aplicar | Hasta 6 mensajes de memoria reciente (3 intercambios) |
| Chat con Gemini en la nube con tu propia clave (BYOK), en streaming, con botón de parar y estado de reintentos | Según cuota de tu clave |
| Elegir modelo de Gemini con insignia gratis/de pago, lista dinámica de tu clave, estimado de capa y uso de hoy | Conteo local de 7 días |
| Portero de privacidad «ocultar y enviar»: IPv4/IPv6, dominios, contraseñas, claves, cadenas de conexión; aviso con número de datos ocultos y «ver qué se ocultó» | Incluido |
| Copiar respuesta y bloques de código; regenerar; editar la última pregunta; reintentar tras error | Incluido |
| Etiqueta del motor que generó cada respuesta | `CLOUD:` o `LOCAL:` |
| Chat temporal (no se guarda) | Incluido |
| Historial de chats, búsqueda por título y retención automática configurable | Solo título en Free |
| Cada chat queda ligado a su servidor o entorno y no se mezcla con otros | Incluido |
| Confirmación obligatoria de comandos peligrosos (`rm -rf`, `docker system prune`…), aun con autoejecución | Incluido |
| Reportar una respuesta | Botón de bandera en cada respuesta |
| Pegar el stack o los logs a mano en el chat | Incluido |

### Funciones exclusivas de Pro en IA
| Función | Límite / detalle |
|---|---|
| IA local en el teléfono y descarga de modelos (catálogo y Hugging Face), con precarga y acelerador **Auto** por defecto (sondeo único GPU vs CPU por teléfono y modelo) o GPU/CPU manual | 4.000 caracteres totales compartidos (`maxNumTokens <= 4.000`); RAM mín. 6/8 GB según modelo |
| Modo Auto: si hay datos privados y hay modelo local, desvía la consulta al teléfono; opción «IA Local primero» | Incluido |
| Seudónimos reversibles en la nube: Gemini ve `[IP_1]`, tú recibes tus valores reales (**los secretos nunca vuelven**) | Incluido |
| Notas por servidor o entorno y regla «Solo IA local» | Máx. 1.500 caracteres de notas |
| Skills propias (`SKILL.md`) | Incluido |
| Lectura automática del stack o los logs de la pantalla (chip «Ve esta pantalla») y análisis en 1 toque | Stacks: máx. 16.000 chars (principio); logs: últimas 100 líneas y máx. 16.000 chars (final) en nube; local máx. 1.500 chars; aviso si se recorta |
| 20 mensajes de memoria en la nube (Free: 6) | 20 mensajes en nube (10 intercambios); local hasta 6 mensajes dentro del 40 % del presupuesto |
| Historial completo: búsqueda dentro de los mensajes, filtro por servidor, fijar, renombrar, exportar a Markdown | Incluido |
| Chats, notas y reglas dentro del respaldo cifrado | Incluido |

## Ajustes, seguridad y datos

| Función | Free | Pro |
|---|---|---|
| Bienvenida de 3 hojas en la primera apertura (saltable; se vuelve a ver en Acerca de) | Sí | Sí |
| Idioma (español / inglés) | Sí | Sí |
| Tema Nord (por defecto) | Sí | Sí |
| Temas OLED, Catppuccin y de marca (STALMAS) | Candado | Sí |
| Bloqueo con PIN y biometría | Sí | Sí |
| Respaldo y sincronización cifrados (AES-256) en Google Drive | Candado | Sí |
| Centro de informes: fallos legibles y agrupados, detalle técnico, «Preguntar a la IA qué significa» y envío revisable por correo | Sí | Sí |
| Acerca de, licencias de código abierto, avisos legales y soporte | Sí | Sí |
| Apoyar el desarrollo (propina opcional, 3 importes; no desbloquea funciones) | — | Sí |

## Requisitos del equipo

| Función | Requisito del equipo | Qué hace la app si falta |
|---|---|---|
| Aplicación STALMAS | **Android 12+** (API 31 o superior) | Google Play solo ofrece la instalación en dispositivos compatibles. |
| IA local (motor y modelos) | **CPU de 64 bits** (`arm64-v8a` o `x86_64`), **6 GB de RAM** mín. (Gemma 4 E2B) u **8 GB de RAM** (Gemma 4 E4B) y espacio libre (tamaño del modelo + 500 MB) | Sin 64 bits desactiva catálogo, búsqueda, importación y activación con aviso; bloquea descargas incompatibles o revierte al modelo válido anterior. |
| Bloqueo con biometría | Sensor biométrico y huella o desbloqueo facial configurado | Interruptor de biometría desactivado con motivo; el acceso con PIN sigue activo. |
| Respaldo en Google Drive | **Servicios de Google Play (GMS)** | Acciones de vincular, subir y restaurar en Drive desactivadas con aviso; el respaldo en archivo local cifrado sigue disponible. |
| Alertas en segundo plano | Permiso de notificaciones (`POST_NOTIFICATIONS`) y ajustes de batería sin restricciones agresivas del fabricante | Solicita el permiso al activar; si el fabricante limita tareas en segundo plano, las revisiones pueden retrasarse. |
| Widgets en pantalla de inicio | Launcher compatible con fijar widgets | Oculta o desactiva el acceso si el launcher no lo soporta. |
