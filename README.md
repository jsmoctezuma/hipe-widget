# 🎮 Hipe Widget

> Overlay configurable para OBS y Streamer.bot, creado para streamers que quieren mostrar metas, eventos, redes, patrocinadores, categoría actual y estado del directo sin tocar código.

<p align="center">
  <a href="https://jsmoctezuma.github.io/hipe-widget/admin.html">
    <img src="https://img.shields.io/badge/Abrir%20panel-GitHub%20Pages-7c3aed?style=for-the-badge&logo=github" alt="Abrir panel">
  </a>
  <img src="https://img.shields.io/badge/Compatible-Streamer.bot-9146FF?style=for-the-badge" alt="Streamer.bot">
  <img src="https://img.shields.io/badge/Compatible-OBS%20Studio-111111?style=for-the-badge&logo=obsstudio" alt="OBS Studio">
</p>

---

## ✨ ¿Qué es Hipe Widget?

**Hipe Widget** es un overlay para streams que se configura desde un panel web y se usa en **OBS Studio** como una **Fuente de navegador**.

No necesitas saber programar.  
Solo abres el panel, eliges tus opciones, copias el enlace generado y lo pegas en OBS.

🔗 **Panel de configuración:**  
https://jsmoctezuma.github.io/hipe-widget/admin.html

---

## 🚀 Inicio rápido

```text
1. Abre el panel de configuración.
2. Importa la acción "Hipe Widget" en Streamer.bot.
3. Activa el WebSocket Server en Streamer.bot.
4. Configura tu canal, metas, colores, redes, sonidos y eventos.
5. Copia el enlace para OBS.
6. Pega ese enlace en OBS como Fuente de navegador.
```

---

## ✅ Qué puede mostrar el widget

| Función | Descripción |
|---|---|
| 🟢 Estado del canal | Muestra si estás EN VIVO, OFFLINE o SIN SEÑAL. |
| 👤 Identidad del canal | Nombre del streamer y foto/logo del canal. |
| 🎯 Meta de subs | Muestra el progreso de suscriptores de Twitch. |
| ❤️ Meta de follows | Muestra el progreso de seguidores de Twitch. |
| 💎 Meta de bits | Soporta meta por stream y meta mensual. |
| 🎉 Celebración de metas | Muestra una animación cuando se alcanza una meta. |
| 🔊 Sonidos | Sonidos para eventos y sonido especial de celebración. |
| ⏱️ Cronómetro | Muestra el tiempo real que llevas en directo. |
| 🎮 Categoría actual | Muestra el juego/categoría de Twitch con portada. |
| 📢 Ticker de eventos | Muestra follows, subs, bits, raids, donaciones y más. |
| 🤝 Patrocinadores | Rotación de logos, imágenes o videos. |
| 🌐 Redes sociales | Muestra tus redes con rotación automática. |
| 🧾 Código de creador | Muestra un código promocional o de afiliado. |
| 🎨 Personalización visual | Colores, bordes, opacidad, tipografía y formato. |

---

## 🧩 Requisitos

Antes de usarlo necesitas:

- **OBS Studio**
- **Streamer.bot**
- Una cuenta de **Twitch** conectada a Streamer.bot
- El WebSocket Server de Streamer.bot activado
- El enlace del panel de configuración del widget

---

## 📦 Archivos principales del proyecto

```text
admin.html              Panel de configuración
widget.html             Overlay que se pega en OBS
streamerbot-import.txt  Código de importación para Streamer.bot
codigosb.txt            Código C# de referencia
assets/                 Imágenes, favicon y sonidos
TESTING.md              Lista de pruebas recomendadas
```

---

## 🛠️ Instalación paso a paso

### 1. Abrir el panel

Abre este enlace en tu navegador:

```text
https://jsmoctezuma.github.io/hipe-widget/admin.html
```

Desde ahí podrás configurar todo el widget sin editar archivos.

---

### 2. Importar la acción en Streamer.bot

La acción le indica a Streamer.bot qué eventos enviar al widget.

#### Código de importación actualizado

<details>
<summary>Ver código de importación (haz clic para expandir)</summary>

```text
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
```

</details>

#### Pasos para importar

1. Abre **Streamer.bot**.
2. Ve a **Actions**.
3. Pulsa **Import**.
4. Usa **Import from Clipboard** si tu versión lo permite.
5. Si no, guarda el código de importación en un archivo `.sbaction` e impórtalo desde archivo.
6. Verifica que la acción **Hipe Widget** quede habilitada.

La acción final debe incluir estas sub-actions en este orden:

```text
Get Twitch Subscriber Count
Get Twitch Follower Count
Add Twitch Broadcaster Information
Execute C# Code
```

Para que la categoría cambie en vivo cuando actualices el juego/categoría en Twitch, agrega también este trigger a la acción:

```text
Twitch → General → Stream Update
```

---

### 3. Activar WebSocket Server en Streamer.bot

Ve a:

```text
Streamer.bot → General → WebSocket Server
```

Usa estos valores recomendados:

| Campo | Valor |
|---|---|
| Host | `127.0.0.1` |
| Puerto | `8080` |

Después, en el panel del widget, revisa que el host y puerto sean los mismos.

---

### 4. Configurar el widget

En el panel encontrarás varias secciones. Estas son las más importantes:

| Sección | Para qué sirve |
|---|---|
| **Formato del widget** | Elige si quieres modo compacto o barra horizontal. |
| **Conexión con Streamer.bot** | Configura host, puerto y prueba la conexión. |
| **Identidad del canal** | Coloca nombre, logo o foto de perfil. |
| **Metas y progreso** | Activa subs, follows, bits y celebración. |
| **Patrocinadores y directo** | Agrega patrocinadores, cronómetro y categoría. |
| **Redes sociales** | Muestra Twitch, YouTube, TikTok, Instagram, X, Discord y más. |
| **Eventos y sonidos** | Decide qué eventos se muestran y qué sonidos usan. |
| **Apariencia** | Cambia colores, opacidad, bordes y estilo visual. |

> Los cambios se guardan automáticamente en tu navegador.

---

### 5. Copiar el enlace para OBS

Cuando termines de configurar el panel:

1. Haz clic en **Copiar enlace para OBS**.
2. Abre OBS.
3. Crea una nueva **Fuente de navegador**.
4. Pega el enlace en el campo **URL**.

Cada vez que cambies metas, colores, redes, imágenes o eventos, vuelve a copiar el enlace y actualízalo en OBS.

---

## 🖥️ Medidas recomendadas para OBS

Usa estas medidas en la Fuente de navegador:

| Diseño | Tamaño recomendado |
|---|---|
| Compacto completo | `1200 x 204` |
| Compacto sin patrocinadores/redes | `800 x 204` |
| Horizontal / barra inferior | `1920 x 116` |

También se recomienda activar en OBS:

```text
Refresh browser when scene becomes active
```

---

## 🎯 Cómo funcionan las metas

### Meta de suscriptores

La meta de suscriptores usa el conteo real de Twitch obtenido desde Streamer.bot.

El widget calcula la siguiente meta automáticamente:

| Rango de subs | Salto de meta |
|---|---|
| 0 a 99 | De 10 en 10 |
| 100 a 999 | De 50 en 50 |
| 1000 o más | De 100 en 100 |

Ejemplos:

```text
21 subs    → meta 30
64 subs    → meta 70
134 subs   → meta 150
1340 subs  → meta 1400
```

Cuando alcanzas la meta, el widget muestra una celebración y después sube a la siguiente meta.

Si las subs bajan bastante, la meta también se reajusta al siguiente objetivo lógico para que no se quede demasiado alta.

---

### Meta de follows

La meta de follows funciona de forma similar a la meta de subs.

| Rango de follows | Salto de meta |
|---|---|
| 0 a 99 | De 10 en 10 |
| 100 a 999 | De 50 en 50 |
| 1000 o más | De 100 en 100 |

Ejemplo:

```text
86 follows   → meta 90
101 follows  → meta 150
940 follows  → meta 950
1020 follows → meta 1100
```

Si el conteo de follows baja, el widget puede reajustar la meta para mantenerla cerca del progreso real.

---

### Meta de bits

La meta de bits tiene dos modos:

#### Por stream

- Cuenta los bits recibidos durante el directo.
- Puede iniciar desde una cantidad base configurada en el panel.
- Al llegar a la meta, se muestra la celebración.
- Se reinicia cuando termina el stream.

#### Mensual

- Guarda el acumulado mensual en Streamer.bot.
- Al alcanzar la meta, el widget se congela visualmente en la meta lograda.
- Streamer.bot sigue guardando los bits reales.
- Para continuar, vuelve al panel, sube el objetivo y copia un nuevo enlace.
- El acumulado mensual se reinicia al cambiar de mes.

> El panel protege el acumulado mensual para evitar bajarlo por accidente.

---

## 🎉 Celebraciones y sonidos

Cuando una meta se alcanza, el widget puede mostrar una celebración visual y reproducir un sonido.

El sonido de celebración usa este archivo:

```text
assets/goal.mp3
```

Desde el panel puedes controlar:

- Sonido global activado/desactivado
- Sonido de celebración de metas
- Sonido por tipo de evento
- Volumen general
- Duración de la celebración

---

## 📢 Eventos soportados

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

## 🖼️ Imágenes, GIFs y videos

Para logos, patrocinadores, GIFs o imágenes personalizadas, usa enlaces públicos directos.

Ejemplos válidos:

```text
https://i.imgur.com/archivo.png
https://i.imgur.com/archivo.gif
https://tusitio.com/video.mp4
https://tusitio.com/imagen.webp
```

Evita rutas locales como:

```text
C:\Users\TuUsuario\Desktop\imagen.png
```

OBS necesita poder leer la imagen desde el navegador. Por eso lo más recomendable es usar una URL pública o subir los archivos al propio repositorio en la carpeta `assets/`.

---

## 🎮 Cronómetro y categoría actual

El cronómetro usa el tiempo real del directo de Twitch.

Si reinicias OBS o recargas el widget, el cronómetro no empieza desde cero: se sincroniza con el tiempo real del stream.

La categoría actual puede mostrar:

- Nombre del juego o categoría
- Portada de Twitch
- Fallback visual si no hay imagen
- Actualización automática con `Stream Update`

---

## 🟢 Estados del widget

| Estado | Significado |
|---|---|
| **EN VIVO** | Twitch está online. |
| **OFFLINE** | Twitch está offline. |
| **SIN SEÑAL** | El widget perdió conexión con Streamer.bot. |

Si aparece **SIN SEÑAL**, normalmente significa que Streamer.bot está cerrado o que el WebSocket Server no está activo.

---

## 🧪 Cómo probar que todo funciona

1. Abre Streamer.bot.
2. Activa WebSocket Server.
3. Abre el panel del widget.
4. Usa el botón **Probar conexión**.
5. Copia el enlace para OBS.
6. Pégalo como Fuente de navegador.
7. Simula un evento desde Streamer.bot.
8. Revisa que el ticker, metas y sonidos reaccionen.

---

## 🆘 Solución de problemas

| Problema | Qué revisar |
|---|---|
| El widget dice **SIN SEÑAL** | Streamer.bot debe estar abierto y WebSocket Server activo. |
| No conecta | Revisa host `127.0.0.1` y puerto `8080`. |
| No aparecen eventos | Confirma que la acción **Hipe Widget** esté habilitada. |
| No aparecen subs o follows | Revisa que las sub-actions de conteo estén en la acción. |
| No suenan eventos | Revisa sonido global, sonido por evento y volumen. |
| No suena la celebración | Revisa que exista `assets/goal.mp3` y que el sonido esté activado. |
| No se ven imágenes | Usa enlaces públicos directos que terminen en `.png`, `.jpg`, `.gif`, `.webp` o `.mp4`. |
| La categoría no cambia | Agrega el trigger `Twitch → General → Stream Update`. |
| El cronómetro no coincide | Revisa los triggers Stream Online y Stream Offline. |
| Los bits mensuales no bajan | Es normal; el acumulado mensual está protegido. |
| El texto se corta | Aumenta el ancho de la Fuente de navegador o usa el tamaño recomendado. |

---

## ❓ Preguntas frecuentes

### ¿Necesito saber programar?

No. El widget se configura desde el panel. Solo necesitas importar la acción en Streamer.bot y pegar el enlace en OBS.

### ¿Puedo cambiar colores y estilo?

Sí. Desde el panel puedes ajustar colores, bordes, opacidad y otros detalles visuales.

### ¿Puedo usar mis propias imágenes?

Sí. Usa URLs públicas directas o sube tus archivos a `assets/`.

### ¿Puedo usarlo con otro streamer?

Sí. El enlace guarda la configuración visual, pero los eventos dependen del Streamer.bot de quien lo esté usando.

### ¿Streamer.bot debe estar abierto?

Sí. Si Streamer.bot está cerrado, el widget no recibirá eventos en tiempo real.

### ¿Tengo que copiar de nuevo el enlace si cambio algo?

Sí. Si cambias configuración en el panel, copia otra vez el enlace y actualízalo en OBS.

---

## 🧾 Notas importantes

- El panel funciona desde GitHub Pages.
- La configuración se guarda en el navegador usando `localStorage`.
- El enlace generado contiene la configuración del widget.
- Streamer.bot debe estar abierto para recibir eventos.
- El WebSocket Server debe estar activo.
- Para imágenes y sonidos, usa rutas accesibles para el navegador.
- Puedes clonar el repositorio y usar tu propia versión en GitHub Pages.

---

## Créditos

<p align="center">
  Desarrollado por <a href="https://github.com/jsmoctezuma">jsmoctezuma</a>
  &nbsp;•&nbsp;
  Iconos por <a href="https://iconify.design">Iconify</a>
  &nbsp;•&nbsp;
  Fuentes: <a href="https://fonts.google.com">Rajdhani y Barlow Condensed</a>
</p>

---

<p align="center">
  Hecho con 💜 para streamers que quieren un overlay limpio, personalizable y fácil de usar.
</p>
