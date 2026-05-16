# Hipe Widget · Eventos en pantalla para Streamer.bot

> Overlay de eventos para streamers: follows, subs, donaciones y más, directo en OBS — sin instalar nada.

[![GitHub Pages](https://img.shields.io/badge/Demo-GitHub%20Pages-blue?logo=github)](https://jsmoctezuma.github.io/hipe-widget/admin.html)
[![Streamer.bot](https://img.shields.io/badge/Compatible-Streamer.bot-purple)](https://streamer.bot)
[![OBS Studio](https://img.shields.io/badge/Compatible-OBS%20Studio-black?logo=obsstudio)](https://obsproject.com)

---

## ¿Qué es Hipe Widget?

Un ticker de eventos para tu stream que muestra en pantalla follows, suscripciones, donaciones y más. Se conecta a **Streamer.bot** vía WebSocket y se añade a **OBS** como fuente de navegador. No requiere instalación: todo está alojado en GitHub Pages.

**Panel de administración →** https://jsmoctezuma.github.io/hipe-widget/admin.html

---

## Inicio rápido

```
1. Abre el panel de administración
2. Importa la acción en Streamer.bot
3. Configura el widget a tu gusto
4. Copia el enlace del widget
5. Pégalo en OBS como Browser Source
```

---

## Instalación paso a paso

### 1 · Abrir el panel de administración

Visita https://jsmoctezuma.github.io/hipe-widget/admin.html en tu navegador. Verás el formulario de configuración completo.

---

### 2 · Importar la acción en Streamer.bot

La acción le indica a Streamer.bot qué eventos enviar al widget.

**Código de importación (Base64):**

<details>
<summary>Ver código (haz clic para expandir)</summary>

```
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
```

</details>

**Pasos para importar:**

1. Copia el código de arriba.
2. Abre **Streamer.bot** → pestaña **Actions** → botón **Import**.
3. Si tienes **"Import from Clipboard"**, pégalo directamente.
   Si no, guarda el código en un archivo `.sbaction` e impórtalo desde archivo.
4. Verifica que la acción aparezca en la lista y esté **habilitada** (ícono verde).

> **Nota para YouTube:** La acción ya incluye triggers de Twitch y StreamElements. Para YouTube, añade manualmente: `YouTube → New Member`, `YouTube → Member Milestone`, `YouTube → Super Chat`.

---

### 3 · Configurar el widget

En el panel de administración ajusta cada sección según tus preferencias:

| Sección | Descripción |
|---|---|
| **Diseño** | Compacto (recomendado) u Horizontal |
| **Tu Canal** | Nombre de usuario y puerto de Streamer.bot (8080 por defecto) |
| **Imágenes** | URLs públicas de [Imgur](https://imgur.com) — no subas archivos locales |
| **Patrocinadores / Redes** | Logos y links de tus patrocinadores y redes sociales |
| **Código de creador** | Tu código de afiliado o creador |
| **Sonidos** | Activa/desactiva y ajusta el volumen |
| **Colores** | Personaliza la paleta del widget |

> Todos los cambios se guardan automáticamente en `localStorage`. Puedes cerrar el panel y volver a abrirlo cuando quieras.

---

### 4 · Generar el enlace para OBS

Haz clic en el botón **"📋 Copiar enlace del widget"** (verde, debajo del título). Se copiará un enlace que contiene toda tu configuración codificada. Guárdalo.

---

### 5 · Añadir el widget a OBS Studio

1. Abre OBS Studio.
2. En tu escena, añade una nueva fuente → **Browser Source**.
3. Pega el enlace copiado en el campo **URL**.
4. Configura el tamaño según el diseño elegido:

| Diseño | Ancho | Alto |
|---|---|---|
| Compacto (con patrocinadores y redes) | 1200 | 204 |
| Compacto (sin patrocinadores ni redes) | 800 | 204 |
| Horizontal (una fila ancha) | 1920 | 116 |

5. Activa **"Refresh browser when scene becomes active"** (recomendado).
6. Haz clic en **Aceptar**.

---

### 6 · Verificar la conexión con Streamer.bot

- En Streamer.bot: **General → WebSocket Server** → debe estar **activado** en el puerto **8080**.
- En OBS, el widget debe mostrar: **"Bienvenido ✓ — Sistema en línea"**.
- Simula un evento desde Streamer.bot (follow, sub, etc.) para probar que el ticker reacciona.

---

## Solución de problemas

| Problema | Solución |
|---|---|
| Widget muestra "⚠ Señal perdida" | Verifica que Streamer.bot esté abierto, el WebSocket Server activo y el puerto sea 8080. |
| Las imágenes no se ven | Confirma que las URLs de Imgur sean públicas y directas (deben terminar en `.png`, `.gif`, etc.). |
| El sonido no suena | Revisa que el volumen en el admin no sea 0 %. En OBS el audio funciona siempre. |
| El texto se corta en el ticker | Aumenta el ancho del Browser Source en OBS. |
| No aparecen eventos de YouTube | Agrega los triggers manualmente en Streamer.bot: New Member, Member Milestone, Super Chat. |
| El panel no guarda la configuración | El panel usa `localStorage`. Si limpias los datos del navegador, deberás configurarlo de nuevo. |

---

## Notas

- **Sin instalación:** todo está alojado en GitHub Pages; no necesitas descargar nada.
- **Configuración portable:** el enlace generado contiene toda tu configuración. Puedes compartirlo con otros streamers; ellos verán tus mismos colores e imágenes, pero los eventos vendrán de su propio Streamer.bot.
- **Autoalojamiento:** clona el repositorio, activa GitHub Pages en tu cuenta y usa `https://tusuario.github.io/hipe-widget/admin.html` como tu panel.

---

## Créditos

Desarrollado por [jsmoctezuma](https://github.com/jsmoctezuma).
Iconos por [Iconify](https://iconify.design) · Fuentes: [Rajdhani y Barlow Condensed](https://fonts.google.com) (Google Fonts).
