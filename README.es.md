<p align="center"><img src="screenshots/banner.png" alt="STALMAS — Tus servidores, en tu bolsillo" width="100%"></p>

# STALMAS

> Este es el **repositorio de la comunidad** de STALMAS: reportes de fallos, ideas y notas de versión. La app es de código cerrado, hecha por un desarrollador independiente (**Peter Magno**).

**Gestiona Portainer y servidores Linux por SSH desde Android, con IA privada.**

![Plataforma](https://img.shields.io/badge/Android-12%2B-3DDC84?logo=android&logoColor=white)
![Estado](https://img.shields.io/badge/estado-prueba%20cerrada-orange)
![Licencia](https://img.shields.io/badge/licencia-propietaria-lightgrey)

[English](README.md) · [Web](https://stalmas.app/es/) · [Manuales](https://stalmas.app/es/docs/) · [Quiero ser tester](https://stalmas.app/es/testers/)

> 🧪 **La prueba cerrada en Google Play está abierta: 40 plazas.** Durante la prueba tienes Pro gratis, y si completas los 14 días y cuentas al menos 2 fallos o ideas, **te quedas STALMAS Pro de por vida**. [Apúntate aquí](https://stalmas.app/es/testers/).

<p align="center">
  <img src="screenshots/phone-1-dashboard.jpg" width="24%" alt="Panel">
  <img src="screenshots/phone-2-containers.jpg" width="24%" alt="Contenedores que necesitan atención">
  <img src="screenshots/phone-3-ai.jpg" width="24%" alt="La IA explica el error">
  <img src="screenshots/phone-6-terminal.jpg" width="24%" alt="Terminal SSH">
</p>

## Índice
- [Qué hace](#qué-hace)
- [Pruébala sin servidor propio](#pruébala-sin-servidor-propio)
- [Free vs Pro](#free-vs-pro)
- [Privacidad de un vistazo](#privacidad-de-un-vistazo)
- [Programa de testers](#programa-de-testers)
- [Este repositorio y enlaces](#este-repositorio-y-enlaces)
- [Requisitos](#requisitos)

## Qué hace
- **La salud de un vistazo:** contenedores sanos, con problemas y detenidos, CPU, RAM y espacio recuperable por entorno.
- **Contenedores:** iniciar, detener, reiniciar, pausar, renombrar, actualizar a la última imagen, consola y acciones en grupo.
- **Registros** con colores, búsqueda, filtros de errores y avisos, rango de fechas y exportación.
- **Stacks:** crea desde el editor, Git o plantillas; edita el compose y las variables, redespliega y ve qué contenedor falla.
- **Recursos:** imágenes, volúmenes y redes, con limpieza segura.
- **Terminal SSH** (xterm-256color) con teclas Esc, Tab, Ctrl y flechas, historial y snippets.
- **Un asistente de IA que conoce la app:** explica errores, analiza registros y te guía paso a paso dentro de STALMAS. Funciona en la nube con tu propia clave de Gemini, o en el propio teléfono con modelos locales (Pro).
- **Privacidad primero:** sin cuentas, sin servidores intermedios, sin analíticas ni publicidad. Antes de que nada llegue a la IA en la nube, se ocultan IPs, dominios, contraseñas y claves.

## Pruébala sin servidor propio
Añade en la app el servidor Portainer de demostración: URL `demo.stalmas.app`, usuario `demo`, contraseña `stalmas-demo`. Todos los datos son ficticios y las acciones son simuladas.

Lee la [Guía de la demo](docs/demo.es.md) paso a paso.

## Free vs Pro

El plan gratuito incluye hasta 3 servidores, todas las acciones sobre contenedores y stacks, los registros y la terminal SSH. **Pro** es un pago único de **$14.99 USD** de referencia en Google Play (sin suscripción; el precio varía por país). *Las funciones disponibles dependen del hardware de tu equipo.*

Para ver requisitos de equipo y notas completas, consulta [Free vs Pro](docs/free-vs-pro.es.md) o la [comparativa en la web](https://stalmas.app/es/docs/free-pro/).

### Conexiones
| Función | Free | Pro |
|---|---|---|
| Servidores Portainer y Linux por SSH (contraseña o llave `.pem`/`.key`) | 3 en total, repartidos como quieras | Ilimitados |
| Estado UP/DOWN de cada servidor | Sí | Sí |
| Aceptar certificado TLS auto-firmado (por servidor Portainer) | Sí | Sí |

### Portainer: panel, contenedores y stacks
| Función | Free | Pro |
|---|---|---|
| Panel por tarjetas (fijo): Salud, Recursos en vivo (CPU/RAM/imágenes), Más consumo, Almacenamiento (espacio recuperable), Accesos rápidos | Sí | Sí |
| Panel a tu medida: editar (subir/bajar, quitar, añadir), plantillas Salud/Operaciones, tarjeta «Contenedores por stack» | Candado | Sí |
| Tarjetas Pro del panel: «Todos tus servidores» (salud de cada servidor guardado) y «Diagnóstico IA» | Candado | Sí |
| Tarjetas Pro «Últimas 24 h» (CPU/RAM del host con pico), «Actividad» (hallazgos de vigilancia incluso con la app cerrada), «Tendencia» (contenedor que llegará antes a su límite de memoria); plantilla «Actividad» | Candado | Sí |
| Historial de uso: guardar CPU/RAM de hasta 30 contenedores por entorno en cada revisión (7 días, cifrado, opcional en Vigilancia) | Candado | Sí |
| Historial en el detalle del contenedor: CPU y RAM de las últimas 6 h / 24 h / 7 días con mín, media y máx (sigue al contenedor aunque se recree) | Candado | Sí |
| Iniciar, parar, reiniciar, pausar, reanudar contenedores | Sí | Sí |
| Detalle de contenedor: cabecera con estado en color, enlace a su stack y acciones Reiniciar · Detener/Iniciar · Consola · Procesos; pestañas Resumen · Logs · Uso · Config | Sí | Sí |
| Resumen: motivo del fallo (salida del healthcheck, *Out of memory* con límite, código de salida explicado) con Reiniciar / Ver errores; IP para copiar, puertos, reinicios y política, creado hace…, CPU/RAM | Sí | Sí |
| Resumen: «Avisarme si falla» de un solo contenedor (avisa aunque la vigilancia general esté apagada) | Candado | Sí |
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
| Logs: ANSI, búsqueda, líneas de error y aviso resaltadas; en vivo, filtros (20 a 10.000 líneas, periodo o rango de fechas, marcas de tiempo), Todos / Errores / Avisos con cifra, copiar, exportar `.log` / compartir, ir al primer error | Sí | Sí |
| Consola dentro del contenedor (`exec`) | Sí | Sí |
| Analizar logs con IA en 1 toque: envía solo las líneas del filtro actual (máx. 100) y dice qué se envió; «Explicar» filtra Errores y analiza | Candado (en Free se pegan a mano) | Sí |
| Ver stacks y su compose/ENV (solo lectura) | Sí | Sí |
| Stacks: salud real por contenedores, cifras tocables como filtro, acción en el sitio que arregla el fallo, redesplegar (con confirmación), iniciar, detener (con confirmación) y eliminar (confirmando por nombre), logs y «Contenedores sin stack» | Sí | Sí |
| Stacks: botón «¿Por qué falla X?» (abre el diagnóstico IA del contenedor con problema) | Candado | Sí |
| Detalle de stack: Resumen, Compose, Variables; Git (traer cambios, configuración) | Sí | Sí |
| Crear stacks nuevos (Editor) | Sí | Sí |
| Crear stack desde Git (Source en Portainer 2.45+, URL y token en antiguas) | Sí | Sí |
| Nuevo stack desde plantilla (Portainer y personalizadas) | Sí | Sí |
| Analizar el compose con IA y aplicar mejoras al editor | Candado | Sí |
| Almacenamiento: imágenes y volúmenes (ver, quién los usa, eliminar, liberar espacio, descargar última versión) | Sí | Sí |
| «¿Qué es seguro borrar?» (IA) | Candado | Sí |
| Pestaña Recursos: tarjeta de espacio, Limpiar (*prune* de imágenes, volúmenes, redes y caché) y entradas a Imágenes, Volúmenes y Redes | Sí | Sí |
| Redes (solo lectura): búsqueda por red o contenedor, filtro Todas / Sin uso, subred (copiar), gateway, ámbito y contenedores miembros | Sí | Sí |

### Terminal (SSH y consola de contenedores)
| Función | Free | Pro |
|---|---|---|
| Emulador `xterm-256color` con teclas Esc/Tab/Ctrl y flechas | Sí | Sí |
| Copiar el último resultado | Sí | Sí |
| Historial de comandos por servidor (se guardan hasta 500) | Ve los 50 más recientes | Ve los 500 |
| Snippets guardados | Hasta 10, sin variables | Ilimitados, con variables `{{nombre}}` |
| Fila de teclas personalizable con cruceta de cursor | Candado | Sí |
| Mantener pantalla encendida | Sí | Sí |
| La IA lee tu pantalla de terminal | Hasta 4.000 caracteres | Hasta 16.000 (nube) · 1.500 (local) |

### Asistente de IA
**Base común (Free y Pro)**
| Función | Límite / detalle |
|---|---|
| Asistente flotante STALMAS (personaje): burbuja movible que sube sobre el teclado, panel anclado no modal redimensionable, historial en el panel y vista previa con ▶ / Aplicar | Hasta 6 mensajes de memoria reciente (3 intercambios) |
| Chat con Gemini en la nube con tu propia clave (BYOK), en streaming, con botón de parar y estado de reintentos | Según cuota de tu clave |
| Elegir modelo de Gemini con insignia gratis/de pago, lista de la clave, estimado de capa y uso de hoy | Conteo local de 7 días |
| Portero de privacidad «ocultar y enviar»: IPs (v4/v6), dominios, contraseñas, claves, cadenas de conexión; aviso con número de datos ocultos y «ver qué se ocultó» | Incluido |
| Copiar respuesta y bloques de código; regenerar; editar la última pregunta; reintentar tras error | Incluido |
| Etiqueta del motor que generó cada respuesta | `CLOUD:` o `LOCAL:` |
| Chat temporal (no se guarda) | Incluido |
| Historial de chats, búsqueda por título y retención automática configurable | Solo por título en Free |
| Cada chat queda ligado a su servidor o entorno y no se mezcla con otros | Incluido |
| Confirmación obligatoria de comandos peligrosos (`rm -rf`, `docker system prune`…), aun con autoejecución | Incluido |
| Reportar una respuesta | Botón de bandera en cada respuesta |
| Pegar el stack o los logs a mano en el chat | Incluido |

**Solo Pro**
| Función | Límite / detalle |
|---|---|
| IA local en el teléfono y descarga de modelos (catálogo y Hugging Face), con precarga y acelerador **Auto** (sondeo GPU/CPU) o manual | 4.000 caracteres totales compartidos (`maxNumTokens <= 4.000`); RAM mín. 6/8 GB según modelo |
| Modo Auto: si hay datos privados y hay modelo local, desvía la consulta al teléfono; opción «IA Local primero» | Incluido |
| Seudónimos reversibles en la nube: Gemini ve `[IP_1]`, tú recibes tus valores reales (los secretos nunca vuelven) | Incluido |
| Notas por servidor o entorno y regla «Solo IA local» | Máx. 1.500 caracteres de notas |
| Skills propias (`SKILL.md`) | Incluido |
| Lectura automática del stack o los logs de la pantalla (chip «Ve esta pantalla») y análisis en 1 toque | Stacks: máx. 16.000 chars (principio); logs: últimas 100 líneas y máx. 16.000 chars (final) en nube; local máx. 1.500 chars; aviso si se recorta |
| 20 mensajes de memoria en la nube (Free: 6) | 20 mensajes en nube (10 intercambios); local hasta 6 mensajes dentro del 40 % del presupuesto |
| Historial completo: búsqueda dentro de los mensajes, filtro por servidor, fijar, renombrar, exportar a Markdown | Incluido |
| Chats, notas y reglas dentro del respaldo cifrado | Incluido |

### Ajustes, seguridad y datos
| Función | Free | Pro |
|---|---|---|
| Bienvenida de 3 hojas en la primera apertura (saltable; repetible en Acerca de) | Sí | Sí |
| Idioma (español / inglés) | Sí | Sí |
| Tema Nord (por defecto) | Sí | Sí |
| Temas OLED, Catppuccin y de marca (STALMAS) | Candado | Sí |
| Bloqueo con PIN y biometría | Sí | Sí |
| Respaldo y sincronización cifrados (AES-256) en Google Drive | Candado | Sí |
| Logcat de la app | Sí | Sí |
| Reportar un problema / recogida de errores | Sí | Sí |
| Acerca de, licencias de código abierto, avisos legales y soporte | Sí | Sí |
| Apoyar el desarrollo (propina opcional, 3 importes; no desbloquea funciones) | — | Sí |

## Privacidad de un vistazo
- **Sin cuentas ni servidores propios:** STALMAS se conecta directamente desde tu teléfono a tus servidores Portainer y SSH.
- **Todo cifrado en tu dispositivo:** credenciales, llaves, historial y ajustes se guardan en local con SQLCipher (AES-256) y preferencias cifradas (AES-256-GCM) protegidas por el Android Keystore, con la copia automática de Android desactivada.
- **Cero rastreo:** sin analíticas, sin publicidad, sin perfiles ni venta de datos.
- **Portero de privacidad:** antes de enviar nada a Gemini (con tu propia clave), oculta IPs, dominios, contraseñas y claves; en Pro ofrece seudónimos reversibles de IP/host o IA local sin conexión.
- **Tú decides qué sale:** copia de seguridad cifrada opcional en tu Google Drive (`drive.appdata` con tu contraseña) y borradores de correo revisables cuando reportas un problema o escribes a soporte.

Lee el [Resumen de privacidad](docs/privacy.es.md) o la [Política de privacidad completa](https://stalmas.app/es/privacy/).

## Programa de testers
- **40 plazas** para la prueba cerrada en Google Play (Pro gratis durante la prueba).
- Usa la app durante **14 días** y comparte al menos **2 fallos o ideas** para quedarte **STALMAS Pro de por vida** (código promocional al publicar en producción).
- Solo se pide tu correo de Google y un alias en [stalmas.app/es/testers/](https://stalmas.app/es/testers/), y los correos de la prueba se borran al terminar.

Consulta los detalles y la tarea sugerida de la semana 1 en la [Guía del programa de testers](docs/testers.es.md).

## Este repositorio y enlaces
STALMAS es de código cerrado. Este repositorio es el lugar público para:
- 🐞 **Reportar fallos:** [abre un issue](https://github.com/PeterMagno/stalmas/issues/new/choose) con la versión de la app y tu teléfono.
- 💡 **Proponer ideas:** usa la plantilla de ideas o [Discussions](https://github.com/PeterMagno/stalmas/discussions).
- 📦 **Seguir las versiones:** en [Releases](https://github.com/PeterMagno/stalmas/releases) y [CHANGELOG.md](CHANGELOG.md) verás qué cambia en cada una.
- 🔒 **Problemas de seguridad:** repórtalos en privado; mira [SECURITY.es.md](SECURITY.es.md).

Documentos del repositorio y comunidad:
- [Guía de demo](docs/demo.es.md) · [Free vs Pro](docs/free-vs-pro.es.md) · [FAQ](docs/faq.es.md) · [Privacidad](docs/privacy.es.md) · [Programa de testers](docs/testers.es.md)
- [Hoja de ruta](ROADMAP.es.md) · [Changelog](CHANGELOG.md) · [Notas v1.0.0-beta](docs/releases/v1.0.0-beta.es.md)
- [Cómo contribuir](CONTRIBUTING.es.md) · [Código de conducta](CODE_OF_CONDUCT.md) · [Soporte](SUPPORT.es.md) · [Manuales web](https://stalmas.app/es/docs/)

## Requisitos
Android 12 o superior y un servidor con Portainer o acceso SSH. La IA local necesita un teléfono de 64 bits con 6 a 8 GB de RAM según el modelo.

---

STALMAS es un producto independiente de **Peter Magno** y no está afiliado a Portainer.io, Docker, Inc. ni Google. Las marcas pertenecen a sus dueños. © 2026 — Todos los derechos reservados.
