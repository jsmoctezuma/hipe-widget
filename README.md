# Hipe Widget · Overlay configurable para Streamer.bot

> Widget para OBS que muestra estado del canal, metas, categoría actual, patrocinadores, redes sociales y eventos del stream usando Streamer.bot.

[![GitHub Pages](https://img.shields.io/badge/Panel-GitHub%20Pages-blue?logo=github)](https://jsmoctezuma.github.io/hipe-widget/admin.html)
[![Streamer.bot](https://img.shields.io/badge/Compatible-Streamer.bot-purple)](https://streamer.bot)
[![OBS Studio](https://img.shields.io/badge/Compatible-OBS%20Studio-black?logo=obsstudio)](https://obsproject.com)

---

## ¿Qué es Hipe Widget?

**Hipe Widget** es un overlay configurable para streamers. Se configura desde una página web, genera un enlace y ese enlace se pega en **OBS Studio** como **Fuente de navegador**.

No necesitas programar. Solo necesitas abrir el panel, importar la acción en Streamer.bot, configurar tu diseño y copiar el enlace para OBS.

**Panel de administración →** https://jsmoctezuma.github.io/hipe-widget/admin.html

---

## Inicio rápido

```text
1. Abre el panel de administración
2. Importa la acción en Streamer.bot
3. Activa el WebSocket Server de Streamer.bot
4. Configura colores, metas, eventos, patrocinadores y redes
5. Copia el enlace para OBS
6. Pégalo en OBS como Browser Source / Fuente de navegador
```

---

## Funciones principales

- Dos diseños: **compacto** y **horizontal**.
- Estado del canal: **EN VIVO**, **OFFLINE** o **SIN SEÑAL**.
- Foto/logo del canal y nombre del streamer.
- Meta de suscriptores de Twitch con avance automático por rangos.
- Meta de follows de Twitch con avance automático por rangos.
- Meta de bits por stream.
- Meta de bits mensual con acumulado persistente en Streamer.bot.
- Celebración visual de metas.
- Patrocinadores con rotación, duración personalizada e indicadores.
- Cronómetro del directo basado en el tiempo real de Twitch.
- Tarjeta de categoría actual del directo con portada, nombre y fallback visual si no hay imagen disponible.
- Redes sociales con rotación e indicadores por color.
- Código de creador con etiqueta, código e imagen.
- Ticker de eventos en pantalla.
- Sonido global y sonido por tipo de evento.
- Formato visual de números grandes en metas, por ejemplo `11900/12000` se muestra como `11,900/12,000`.
- Ajuste automático de texto para evitar que números largos, categorías largas y textos del ticker se salgan del contenedor.
- Personalización de colores, opacidad, tipografía y bordes.
- Host y puerto configurables para Streamer.bot.
- Prueba de conexión desde el panel.

---

## Instalación paso a paso

### 1 · Abrir el panel de administración

Visita el panel en tu navegador:

```text
https://jsmoctezuma.github.io/hipe-widget/admin.html
```

Ahí encontrarás el formulario completo de configuración.

---

### 2 · Importar la acción en Streamer.bot

El código de importación actualizado está en:

```text
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
```

**Pasos para importar:**

1. Abre **Streamer.bot**.
2. Ve a **Actions**.
3. Pulsa **Import**.
4. Usa **Import from Clipboard** si tu versión lo permite.
5. Si no, guarda el código de importación en un archivo `.sbaction` e impórtalo desde archivo.
6. Verifica que la acción **Hipe Widget** quede habilitada.

---

### 3 · Configurar Streamer.bot

Activa el servidor WebSocket:

```text
Streamer.bot → General → WebSocket Server
```

Valores recomendados:

| Campo | Valor recomendado |
|---|---|
| Host | `127.0.0.1` |
| Puerto | `8080` |

En el panel del widget puedes cambiar host y puerto si tu configuración es diferente.

---

### 4 · Configurar el widget

En el panel de administración ajusta cada sección según tus preferencias:

| Sección | Descripción |
|---|---|
| **Formato del widget** | Elegir compacto u horizontal |
| **Conexión con Streamer.bot** | Host, puerto y prueba de conexión |
| **Identidad del canal** | Nombre y foto/logo del streamer |
| **Metas y progreso** | Meta de subs, follows, bits y celebración |
| **Patrocinadores y directo** | Logos/videos, cronómetro y categoría actual |
| **Redes sociales y código de creador** | Cuentas sociales y código promocional |
| **Eventos y sonidos** | Eventos visibles, sonidos y duración del ticker |
| **Apariencia** | Colores, opacidad, tipografía y bordes |

> Todos los cambios se guardan automáticamente en el navegador usando `localStorage`.

---

### 5 · Generar el enlace para OBS

Pulsa el botón para copiar el enlace del widget desde el panel de administración.

Ese enlace contiene tu configuración codificada, por eso si cambias metas, colores, redes o eventos, debes copiar de nuevo el enlace y actualizarlo en OBS.

---

### 6 · Añadir el widget a OBS Studio

1. Abre OBS Studio.
2. En tu escena, añade una nueva fuente → **Browser Source** / **Fuente de navegador**.
3. Pega el enlace generado por el panel en el campo **URL**.
4. Configura el tamaño según el diseño elegido:

| Diseño | Medida recomendada |
|---|---|
| Compacto con patrocinadores y redes | `1200 x 204` |
| Compacto sin patrocinadores ni redes | `800 x 204` |
| Horizontal | `1920 x 116` |

5. Activa **Refresh browser when scene becomes active**.
6. Guarda la fuente.

---

## Eventos soportados

### Twitch

- Follow
- Subscription
- Resubscription
- Gift Subscription
- Gift Bomb
- Raid
- Cheer / Bits
- Reward Redemption
- Stream Online
- Stream Offline
- Stream Update

### YouTube

- Nuevo suscriptor
- Nuevo miembro
- Membership milestone
- Regalo de membresía
- Super Chat

### StreamElements

- Donation / Tip

---

## Metas de suscriptores

La meta de suscriptores usa los datos reales de Twitch obtenidos por Streamer.bot.

La meta se calcula por rangos:

| Rango | Salto de meta |
|---|---|
| 0 a 99 | 10 |
| 100 a 999 | 50 |
| 1000 en adelante | 100 |

Ejemplos:

```text
21 subs    → meta 30
134 subs   → meta 150
1340 subs  → meta 1400
```

Al llegar a la meta, el widget espera unos segundos, muestra la celebración y luego actualiza a la siguiente meta.

---

## Meta de follows

La meta de follows usa una lógica similar a la meta de suscriptores.

| Rango | Salto de meta |
|---|---|
| 0 a 99 | 10 |
| 100 a 999 | 50 |
| 1000 en adelante | 100 |

Si Streamer.bot envía el total de followers, el widget usa ese número. Si solo llega un evento de follow, Streamer.bot suma 1 al acumulado guardado.

---

## Meta de bits

La meta de bits tiene dos modos.

### Por stream

- Empieza desde los bits actuales configurados en el admin.
- Suma cheers/bits recibidos durante el directo.
- Al llegar a la meta, se congela visualmente en `objetivo/objetivo`.
- Se reinicia al terminar el directo.
- También suma al acumulado mensual interno.

### Mensual

- Usa la variable mensual persistente de Streamer.bot.
- Al llegar a la meta, el widget se congela visualmente en `objetivo/objetivo`.
- Streamer.bot sigue acumulando bits reales internamente.
- Si quieres una meta más grande, vuelve al admin, sube el objetivo y copia un nuevo enlace.
- Los bits mensuales solo se reinician al cambiar de mes.

> El admin no permite bajar los bits mensuales guardados en Streamer.bot. Esto protege el acumulado real.

---

## Cronómetro y categoría actual

El cronómetro usa el tiempo real del directo de Twitch.  
Si recargas OBS o cambias el enlace durante un directo, el cronómetro no empieza desde cero: se sincroniza con el tiempo real que lleva el stream.

La tarjeta de categoría muestra:

- Portada de la categoría actual.
- Nombre de la categoría.
- Fallback visual si no hay imagen disponible.
- Actualización usando el trigger `Twitch → General → Stream Update`.

---

## Estados del canal

| Estado | Significado |
|---|---|
| **EN VIVO** | Twitch está online |
| **OFFLINE** | Twitch está offline |
| **SIN SEÑAL** | El widget perdió conexión con Streamer.bot |

Si aparece **SIN SEÑAL**, revisa que Streamer.bot esté abierto y que el WebSocket Server esté activo.

---

## Solución de problemas

| Problema | Solución |
|---|---|
| El widget muestra **SIN SEÑAL** | Abre Streamer.bot y revisa el WebSocket Server |
| No conecta con Streamer.bot | Verifica host `127.0.0.1` y puerto `8080` |
| No aparecen eventos | Revisa que la acción **Hipe Widget** esté habilitada |
| No suenan eventos | Revisa sonido global, sonido por evento y volumen |
| No se ven imágenes | Usa enlaces públicos directos a imagen/video |
| El cronómetro no coincide | Verifica triggers Twitch Stream Online/Offline |
| La categoría no cambia en vivo | Agrega el trigger `Twitch → General → Stream Update` |
| Bits mensuales no bajan | Es intencional; Streamer.bot protege el acumulado real |

---

## Archivos principales

```text
admin.html              Panel de configuración
widget.html             Overlay para OBS
codigosb.txt            Código C# de Streamer.bot para referencia
streamerbot-import.txt  Código de importación de la acción
TESTING.md              Checklist de pruebas
assets/                 Imágenes, audio y favicon
```

---

## Notas

- **Sin instalación:** el panel funciona desde GitHub Pages.
- **Configuración portable:** el enlace generado contiene la configuración del widget.
- **Streamer.bot debe estar abierto** para recibir eventos en tiempo real.
- **localStorage:** el panel guarda tus preferencias en el navegador.
- **Celebración visual:** la celebración de metas actualmente es visual. Los sonidos pertenecen a los eventos del ticker, no a la celebración como sonido independiente.
- **Autoalojamiento:** puedes clonar el repositorio, activar GitHub Pages en tu cuenta y usar tu propia URL del panel.

---

## Créditos

Desarrollado por [jsmoctezuma](https://github.com/jsmoctezuma).  
Iconos por [Iconify](https://iconify.design) · Fuentes: [Rajdhani y Barlow Condensed](https://fonts.google.com) (Google Fonts).
