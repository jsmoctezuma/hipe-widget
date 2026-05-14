# 🎮 Hipe Widget – Eventos en pantalla para Streamer.bot

Widget profesional y elegante para mostrar en tu stream (OBS) los eventos de la comunidad: seguidores, suscriptores, raids, bits, donaciones, miembros de YouTube, etc. Incluye un **panel de administración** para que personalices colores, imágenes, sonidos y más, sin tocar código.

## ✨ Características

- **Dos diseños**: Compacto (dos filas) u Horizontal (una fila ancha).
- **Eventos compatibles**:
  - Twitch: follows, subs, resubs, gift subs, gift bombs, raids, bits (cheers), canjes de puntos.
  - YouTube: nuevos miembros, hitos de membresía, superchats.
  - StreamElements: donaciones (tips).
- **Meta de suscriptores** con barra de progreso y celebración al alcanzarla.
- **Patrocinadores**: imágenes o videos que rotan automáticamente.
- **Redes sociales**: muestra tus cuentas de Twitch, YouTube, Instagram, TikTok, X, Facebook, Discord (rotación).
- **Código de creador**: texto y logo personalizable.
- **Sonidos**: activa/desactiva el sonido globalmente o por cada tipo de evento. Ajusta el volumen.
- **Ticker inteligente**: el tamaño del texto se ajusta automáticamente al espacio disponible (sin desbordes).
- **Configuración guardada**: el panel recuerda tus ajustes en el navegador (localStorage).
- **Enlace único**: genera un enlace que pegas en OBS y el widget se carga con tu configuración.

## 📦 Requisitos previos

- Tener instalado **Streamer.bot** (gratuito) y conectado a tus cuentas de Twitch, YouTube y/o StreamElements.
- Tener **OBS Studio** (gratuito).
- Una cuenta de **GitHub** (opcional, si quieres alojar los archivos en la nube; también puedes usar un servidor web local).

## 🚀 Instalación y primeros pasos

### 1. Obtén los archivos del widget

Puedes descargarlos de dos formas:

- **Opción A (recomendada)**: Visita el repositorio oficial en GitHub:  
  `https://github.com/TU_USUARIO/hipe-widget`  
  Haz clic en el botón verde **"Code"** y luego **"Download ZIP"**. Extrae la carpeta en tu computadora.

- **Opción B (si tienes conocimientos de Git)**: Clona el repositorio con:  
  `git clone https://github.com/TU_USUARIO/hipe-widget.git`

### 2. Sube los archivos a un servidor web (o usa GitHub Pages)

El widget necesita estar alojado en un servidor web para que OBS pueda cargarlo. La forma más fácil es usar **GitHub Pages** (gratuito):

- Crea un repositorio público en GitHub (por ejemplo, `hipe-widget`).
- Sube los archivos `admin.html`, `widget.html` y la carpeta `assets` (con sus imágenes y sonido).
- En la configuración del repositorio, activa **GitHub Pages** (rama `main`, carpeta raíz).
- Obtendrás una URL como: `https://tuusuario.github.io/hipe-widget/`

También puedes usar cualquier otro hosting estático (Netlify, Vercel, o incluso un servidor local con `http-server`).

### 3. Importa la acción de Streamer.bot

Dentro de la carpeta que descargaste, encontrarás un archivo llamado `Hipe_Widget.sbaction` (o el código Base64 en el README). Sigue estos pasos:

1. Abre **Streamer.bot**.
2. Ve a la pestaña **Actions** (Acciones).
3. Haz clic en **Import** (Importar) y selecciona el archivo `Hipe_Widget.sbaction`.
4. Asegúrate de que la acción aparezca en la lista y esté **habilitada** (ícono verde).

> **Nota**: La acción ya incluye los disparadores para Twitch y StreamElements. Para que funcionen los eventos de **YouTube**, debes añadir manualmente los siguientes triggers:
> - YouTube → New Member
> - YouTube → Member Milestone
> - YouTube → Super Chat

### 4. Configura tu widget

Abre el panel de administración en tu navegador usando la URL que obtuviste en el paso 2. Por ejemplo:
Verás un formulario con varias secciones:

- **Diseño del Widget**: elige entre Compacto (dos filas) o Horizontal (una fila ancha).
- **Tu Canal**: ingresa el nombre de tu canal, el puerto de Streamer.bot (normalmente 8080) y las URLs de tu logo e imagen del corazón (puedes dejarlas vacías para usar las imágenes por defecto de la carpeta `assets`).
- **Meta de Suscriptores**: ajusta los segundos de celebración y cuánto tiempo se ve el cronómetro.
- **Patrocinadores y tiempo en vivo**: activa/desactiva los patrocinadores y el cronómetro. Puedes añadir patrocinadores con nombre, duración y URL de la imagen (recomendamos usar Imgur).
- **Redes sociales y código de creador**: activa las redes que quieras, escribe tus usuarios y configura el código de creador (texto, etiqueta y logo).
- **Mensajes en pantalla (eventos)**: aquí puedes activar el sonido global, elegir qué eventos se muestran y cuáles suenan, y ajustar el volumen.
- **Colores y forma**: cambia el color de fondo, bordes, color principal (acento) y el redondeo de esquinas.

**Todos los cambios se guardan automáticamente** en tu navegador. Si cierras el panel y vuelves a abrirlo, tus preferencias seguirán ahí.

### 5. Genera el enlace para OBS

Una vez que hayas configurado todo a tu gusto, haz clic en el botón grande verde **"📋 Copiar enlace del widget"** (está justo debajo del título). Se copiará un enlace largo similar a:

Ese enlace contiene **toda tu configuración** (colores, imágenes, eventos, etc.). ¡Guárdalo o pégalo directamente en OBS!

### 6. Añade el widget a OBS

1. Abre **OBS Studio**.
2. En la escena donde quieras mostrar el widget, crea una nueva fuente → **Browser Source**.
3. En **URL**, pega el enlace que copiaste.
4. Configura el ancho (width) y alto (height) según el diseño que hayas elegido:

| Diseño                      | Ancho | Alto  |
|-----------------------------|-------|-------|
| Compacto (con patrocinadores y redes) | 1200  | 204   |
| Compacto (sin patrocinadores ni redes) | 800   | 204   |
| Horizontal (una fila ancha) | 1920  | 116   |

5. Marca la opción **"Refresh browser when scene becomes active"** (para que se reconecte al WebSocket al cambiar de escena).
6. Haz clic en **Aceptar**.

### 7. Verifica la conexión con Streamer.bot

- Asegúrate de que Streamer.bot esté ejecutándose y que el **WebSocket Server** esté activado (General → WebSocket Server, puerto 8080).
- En el widget, deberías ver el mensaje **"Bienvenido ✓ — Sistema en línea"**.
- Prueba un evento (por ejemplo, un follow de prueba desde Streamer.bot). El ticker debe mostrar el evento y, si activaste el sonido, escucharás la notificación.

## 🎨 Personalización avanzada

Si deseas cambiar fuentes, tamaños, animaciones o cualquier detalle visual más allá de lo que permite el panel, puedes editar directamente el archivo `widget.html`. Los estilos están dentro de la etiqueta `<style>`. No olvides guardar los cambios y volver a generar el enlace.

## ❓ Solución de problemas comunes

| Problema | Posible solución |
|----------|------------------|
| El widget no se conecta (muestra "⚠ Señal perdida") | Verifica que Streamer.bot esté abierto, el WebSocket Server activo y el puerto coincida (8080). |
| Las imágenes no se ven | Asegúrate de que los archivos `logo.png`, `corazon.gif`, etc., estén en la carpeta `assets` y que las rutas sean correctas. Si usas URLs externas, comprueba que sean públicas. |
| El sonido no suena | Revisa que el archivo `notification.mp3` esté en `assets`. Ajusta el volumen en el admin (no al 0%). En algunos navegadores puede requerir una interacción; en OBS funciona siempre. |
| El ticker corta el texto | El tamaño del texto se ajusta automáticamente. Si aún así se corta, aumenta el ancho del Browser Source en OBS. |
| Los eventos de YouTube no aparecen | Agrega los triggers manualmente en la acción de Streamer.bot (New Member, Member Milestone, Super Chat). |
| El panel no guarda mis cambios | El panel usa `localStorage` del navegador. Si borras los datos o usas modo incógnito, se perderán. No hay problema, puedes volver a configurarlo. |

## 📝 Créditos y licencia

Desarrollado por [jsmoctezuma](https://github.com/jsmoctezuma).  
Iconos por [Iconify](https://iconify.design).  
Fuentes: Rajdhani y Barlow Condensed (Google Fonts).  

Puedes usar, modificar y compartir este widget libremente. ¡Disfrútalo en tu stream! 🎥

---

## 📌 Enlaces útiles

- [Streamer.bot oficial](https://streamer.bot/)
- [GitHub Pages – cómo alojar tu widget gratis](https://pages.github.com/)
- [Imgur – sube imágenes gratis para tus patrocinadores y logos](https://imgur.com/)
