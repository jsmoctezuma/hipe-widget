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
U0JBRR+LCAAAAAAABADNWllz4kgSfp+I+Q8dft1Rb6l0T8Q+cMrCbboNRoDW81AXQrauRQKMJ+a/b5YAG3F091zedQQmUFZlZX75ZVaWpF9//OHDh6tElOTq5w+/yh/wMyWJgJ9Xt5sPnec8W5RXP+0kZFnOs4WUPRZJxkrxskzIq3QlFkWUpVKsfkQf0auAi4ItorzcCQ/VZYNl2mA7SbqM470sidIoWSb+q04plLLfqhFXnNRsJpWOAq78e3vlw15UiSMuF2a2yg1HdRRmqJai64alOBamijozKNEJEjPD2BtXTfvPUiwrKNDuTznzb/9XmylSQmMhVy0XS1GTPLN4yUV3kSXXUVFmiw0MmpG4uDTqi0h5lIbnRu0jdR3l4sM44qEoa1aEi2yZywHDciFIUpOReE02BcB/TvGCpDxLXgNzImdZypaLhUjLc9JyEYUhBO4wGkcROYiKTi2kc10ozMJY0blKFXtmMYViy1CRhS1bJ4eWb5fY5NJz1dCPJReRf8O12FPll0Ppbz9921bMTKZqmCuqZhBFp4IolDuOolm2bdqYcUS1y7Ya72RrGSVi4VUGW5rm2Iibiuk4QHlEwWCMZspMMBNhSyOEmCcGb33VHGRr4JVic82GbOG24hiIKEw1GGUmtnT1dOrOVwup7+brlmiqed6LmSbACU5lzlNgF9YUoglHsYQjkGEyjp3ZxYgh7X/uBdRBuK6cwJmQ57PXt14b3BSUWaaCVTpTdMaoQmymKapOuapzagqhXvb6vXLqr/O6WNL7rfXoZEqWlvPCjWZl5YB6koRbxBxhWqZu6grHFgK2U0CMz4RCTQsjjZmEMHwZsffK7D/GBjabUZuqRJlZct+T5YA4qqEg05jNkKpCpeWXfbPetcIiZAOcKlLIjKuKLpih2BhqraNZjCA0swzzcoV9t6qzEGuy4NsSe6F8MsPSMJRQRbMJEMomjuKY2IA8dIT0TcW2ddERFf9fE8rmjg5OqApFM0fRLUdXiKlxxSLUEBQZFPHLvqH39Q1a0UvOnUp2tUA3TUHUmaLajCs6xjPFmem6gi3VdLhlEhtdrp743Ui4j90fcNDQdZ0YAvKL6uCgEIpja7oCzTAjmqMyol5suXSETsr131oRDJM7kPuagihsaPoMWQrRgWw2ojMoyrYBfftXjHXe1VjoixyKYLuFwqUpOhE6UMc2YAtWCRQDy9QuN4g6Uv/Cnfftxy+HvTnslI3Ts9JlhyybGtixYe8QJqS6bUAuCMNQDKEZ3LYpcvTTXFiLKJzLowE6ZeDOWQPZx5KcyANFVVQPToLfCUWUciFJj74/YrvT07m16ifWcyMWYibAXCZOcKzErZ8fHsZgU7YuHh5uI7bIimxWfux37h8eugtYeJ0tnkz94WGlw1FZQ5rqPDwkBcsWcUQ/8jg+xvSP6hxuilIkFzR+fHjoi3UJZJCKekWWVgPr4345dp1uStHKeHXy5JN+ThMWjrT4hbt++XmNbvbX7hNf466zZNhJeMu4ge+llLfv8jUf9woyvg2n+HnOtNvwTm16w7EB14wY5Fb7Lgu9ViNk135E3fjRc3sritfhYDKPp5qPgmGY78cI0Cm/d5/Vp03j+VPU/DJNBzFN/I133Ven6W0YuKMwSJwNHXdChv2UT3pzrzV/Cib9p2DYHHEcoykOQ7pplsFYXbEknt/cHepu5jS9C2H9DUv8Je9u9X4ZNtaf1/VxQdTIppNeyjZGm2IDTcfxkqEyFsMwYpofMdzfkHEvZk/9FR8byIueXv2pPtdFvxU1wgO/Qs+Nl4DjiKXxHeh+CYbzOUv4y3jTewE8X6ZaL5+Cv3fYUcHOaDI0RlTtI/BjGWzC/FOrueKTE/vzI9udmh2uXzA8qtlyhHf1OcWk2R51wuUA+2iAn1fTpFv4SXfzRfrQ1jMvmefM9dsQg00A/o8kJhuv8K4HGz4enbOpZsOnjR0ONB/8H8xZ1FxPZSyvuyrEcQnxA2yaazL2N4HbCaV+lkDsJ0FM08GK1XVXdo6O7Lxp9TIyacZ3db8iwPCxbvM65Nc9WPfJquP2vJI5QBNHu59UeHSmk0Hsu3EZjJwkSPsxxNLnbv8z1djSdx2fJrG+las5dZ9z4OgjcOeJQeyO8Igodgrgw8u9G+Ng2HC8Tv9u2DKA8/0eq2Luz+l4G/fPp/mxgfy4Bt4jMnaW04kXUsDpfuyj6bCRETdeByO+mo6f7yWvzuVAgJ05bb2uC7oG19R1IpgzBn025DH6EoXRsS4vuoRXnEAuphR3C6+9drx24zvyQepdy/zLbty+ytKejO92nZYd3t43cq9VhLfDp/Amajzfts/mVH3dIz1138+tfcyHxsJrd47qwfYja9ynGOLe4QXFvTntBsDd8xht8b2A1TXqt8LzfLjDfhGMexvgWlWDL+bh9a4uvLzlYjB+jqdpb85dyZu3XPTayPFaPcRSP/Ye6xhCzGFs8/Ftrt+lyd1X8r/Ki3+85tebvfFgbDxd5Mfe3k2zmAJv/Uk/ZhHwz+1uAu12CTVvyd0ucLP/KZg8ZV7qvwQTL7oZNv65HdOn+2vHddFrwzpP3SLQ/DwY69HZXLvuw14yOMBoJH1MIGYvwX0dE8l9zzVirg5kfYY8l3ZWfKn71LJXXvt26XVe2gXm+RR3qj1qlPgR+Bh7rVD9PLTxbatRfokauN+ytdvW09Fa0/CE+219v963c+i8X1Wsz3EY9lPNl3hCXIEX4U1rfsz/leQ/4C7zAPIvk3l45PfbHlnX93vy7xjf4/wvLq379Xpfzx+o941oy8dLe9P35DZg7AI2SRcFI38ZtECXa6w4Uvd2rm/bjT+hv147DjGF/aqK5c0RR2f1mh5T4MGuFuYMvdkLXE6P6v9XYrnb66KTepCfmXNGz+/DUtom/fWSYF7Zf6l2HHzIpH9U5yR3tvPP4X6E09k+pN/Sw8FoHfrdnn+HbNPrQL8AvSP0JbB/qyuvk9/fIx1yO4Y86SPoTw77FcSHTc/vqLeyZ4B+C+pYLHNyXs9diUGz2qdGbteAujsPKt5DHqy/GZ/5VAM+Y13ulVG1t3T9deACH4HXZ8a/5rTM8aPe7tx4JHvdYFLV/crGT41v144aT8+Mn57uZS9g09PhnnF2Hbf7wrtVrZdz3vaL+p7pnPZFTZ/hbknleSTtQU4NHuXcYdpf0XqPGdPWLmbXvXiK42i6vQb1JI+5a4MNccnceFXDatsrTcD2F4r7C+iZWiyBOLp9OAMNqvPRTScHWXVmwMGkh2QeyHMI6DOhb4xI4j/yXb/yxoOn4/4Qy54OdEIMu+Wf5curHm0g94foPOa7PnTfk959DettDfaxPAc5jwTif4r3vMKj2tfhTAO98j3gkUOdy0Xif5E4T7W77NTHLRb13OnF/NrfQAzr+5rso1L0r5PbF/lCsCzJo1icebq5uz8Qk82wJItzzz+rEQVZiYEolnF5n/lkEcl7F18bWxt17obD7qGchiyNO6qC7Zmh6AbWFMfGTJk5lOuOZWkY63/kdowj//6WGzLq99yVYlkck7wQ3JVPrOt3s3Zz9uO3D+W3Q/aXIFoJSXn94lrQImNPohyKxWr3NPpU2Ioj8LEurJ6ffuNdgt/7YPXtrQpRkg/DJS0uvC9w+ixe5IKUZ94kiNISPCOxDB9CtSnV43vvTX6idJnnYnEwoDY9jtIKYFQP0VIOP7zFto+M/Nq9lvH2DgjePju9EtUrJILLVxmudq+G7Ch6+pLH9sURhcT5nHxUr3784bf/AnoIByGiIgAA
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
