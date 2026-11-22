# Guía de la demo

[English](demo.md)

Prueba STALMAS sin poner tus propias credenciales ni exponer tus servidores. Ofrecemos un servidor Portainer público de demostración con datos ficticios y acciones simuladas: no afecta a ningún sistema real.

## Credenciales

| Campo | Valor |
|---|---|
| **Tipo de servidor** | Portainer |
| **URL del servidor** | `demo.stalmas.app` (mantén `https://` seleccionado) |
| **Método de autenticación** | Usuario / contraseña |
| **Usuario** | `demo` |
| **Contraseña** | `stalmas-demo` |

## Cómo añadir la demo paso a paso

1. Abre STALMAS. En las pantallas de bienvenida, pulsa **Saltar** (o avanza hasta pulsar **Empezar**).
2. En **Servidores**, pulsa **Añadir servidor** (o `+`) y elige **Portainer**.
3. Rellena el formulario de conexión:
   - **Alias:** el nombre que prefieras (por ejemplo, `Demo`).
   - **URL del servidor:** `demo.stalmas.app` (mantén seleccionado el prefijo `https://`).
   - **Método de autenticación:** elige **Usuario / contraseña**.
   - **Usuario:** `demo`
   - **Contraseña:** `stalmas-demo`
4. Pulsa **Guardar y conectar**.
5. Toca el servidor de demostración para ver sus entornos.

## Qué hay en la demo

- **2 entornos** (entre ellos **`homelab`**) con stacks, contenedores, imágenes, volúmenes y redes ficticias.
- Un contenedor llamado **`worker`** **falla a propósito** para que puedas probar un caso real de diagnóstico.
- Todas las acciones son simuladas: iniciar, detener o inspeccionar contenedores no toca ningún equipo real.

> Nota: la terminal SSH requiere un servidor Linux propio. Por motivos de seguridad no ofrecemos un acceso SSH público de demostración.

## Qué probar

1. **Recorre las vistas principales:** abre el entorno **`homelab`** y explora **Panel**, **Contenedores**, **Stacks** y **Recursos** (Imágenes, Volúmenes y Redes).
2. **Inspecciona el contenedor `worker` que falla:**
   - Entra en **Contenedores** (filtra por **Problemas** o mira en **Necesitan atención**), o búscalo en **Stacks**.
   - Toca `worker` para ver su **Resumen** (motivo del fallo, reinicios, puertos) y pasa a la pestaña **Logs** para buscar o filtrar **Solo errores**.
3. **Pregúntale a la IA por qué falla `worker`:**
   - Toca la burbuja flotante de **STALMAS** en cualquier momento para preguntar por `worker`.
   - Si tienes **Pro** activo (por ejemplo, durante la prueba cerrada), pulsa **Explicar** en el contenedor con problemas o **¿Por qué falla worker?** en **Stacks** para diagnosticar sus logs directamente.
   - En **Free**, entra en **Logs**, copia las líneas de error y pégalas en el chat de la IA.
   - *Consejo:* La IA en la nube usa tu propia clave de API de Gemini (**Ajustes → Integración con IA**). Con Pro, en un teléfono compatible de 64 bits (6–8 GB de RAM), también puedes descargar un modelo local Gemma 4 y analizar sin conexión.

¿Encontraste algún fallo o tienes una idea? Mira [Cómo contribuir](../CONTRIBUTING.es.md) o [abre un issue](https://github.com/PeterMagno/stalmas/issues/new/choose).
