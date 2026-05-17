# Hipe Widget - Overlay configurable para Streamer.bot

Widget para OBS que muestra estado del canal, metas, patrocinadores, cronometro, redes sociales y eventos del stream usando Streamer.bot.

[Panel de administracion](https://jsmoctezuma.github.io/hipe-widget/admin.html)

## Que Hace

Hipe Widget es un overlay configurable para streamers. Se configura desde una pagina web, genera un enlace y ese enlace se pega en OBS como Fuente de navegador.

No necesitas programar. Solo necesitas:

- Abrir el panel de administracion.
- Importar la accion en Streamer.bot.
- Configurar colores, metas, eventos y redes.
- Copiar el enlace para OBS.
- Pegar el enlace en una Fuente de navegador.

## Funciones

- Dos disenos: compacto y horizontal.
- Estado del canal: EN VIVO, OFFLINE o SIN SENAL.
- Foto/logo del canal y nombre del streamer.
- Meta de suscriptores de Twitch con avance automatico por rangos.
- Meta de follows de Twitch con avance automatico por rangos.
- Meta de bits por stream.
- Meta de bits mensual con acumulado persistente en Streamer.bot.
- Celebracion de metas.
- Patrocinadores con rotacion, duracion personalizada e indicadores.
- Cronometro del directo basado en el tiempo real de Twitch.
- Tarjeta de categoria actual del directo con portada, nombre y fallback visual si no hay imagen disponible.
- Formato visual de numeros grandes en metas, por ejemplo 11900/12000 se muestra como 11,900/12,000.
- Ajuste automatico de texto para evitar que numeros largos, categorias largas y textos del ticker se salgan del contenedor.
- Redes sociales con rotacion e indicadores por color.
- Codigo de creador con etiqueta, codigo e imagen.
- Ticker de eventos en pantalla.
- Sonido global y sonido por tipo de evento.
- Personalizacion de colores, opacidad, tipografia y bordes.
- Host y puerto configurables para Streamer.bot.
- Prueba de conexion desde el panel.

## Eventos Soportados

Twitch:

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

YouTube:

- Nuevo suscriptor
- Nuevo miembro
- Membership milestone
- Regalo de membresia
- Super Chat

StreamElements:

- Donation / Tip

## Instalacion Rapida

1. Abre el panel de administracion:

```text
https://jsmoctezuma.github.io/hipe-widget/admin.html
```

2. Importa la accion en Streamer.bot.
3. Activa el WebSocket Server de Streamer.bot.
4. Configura el widget en el panel.
5. Pulsa `Copiar enlace para OBS`.
6. Pega el enlace en OBS como Fuente de navegador.

## Importar Accion En Streamer.bot

La accion se llama:

```text
Hipe Widget
```

Pasos:

1. Abre Streamer.bot.
2. Ve a `Actions`.
3. Pulsa `Import`.
4. Usa `Import from Clipboard` si tu version lo permite.
5. Si no, guarda el codigo de importacion en un archivo `.sbaction` e importalo desde archivo.
6. Verifica que la accion `Hipe Widget` quede habilitada.

El codigo de importacion actualizado esta en:

```text
streamerbot-import.txt
```

La accion final incluye estas sub-actions en este orden:

```text
Get Twitch Subscriber Count
Get Twitch Follower Count
Add Twitch Broadcaster Information
Execute C# Code
```

Para que la categoria cambie en vivo cuando actualices el juego/categoria en Twitch, agrega tambien el trigger de Twitch:

```text
Twitch -> General -> Stream Update
```

## Configurar Streamer.bot

Activa el servidor WebSocket:

```text
Streamer.bot -> General -> WebSocket Server
```

Valores recomendados:

```text
Host: 127.0.0.1
Puerto: 8080
```

En el panel del widget puedes cambiar host y puerto si tu configuracion es diferente.

## Configurar El Widget

En el panel encontraras estas secciones:

| Seccion | Para Que Sirve |
|---|---|
| Formato del widget | Elegir compacto u horizontal |
| Conexion con Streamer.bot | Host, puerto y prueba de conexion |
| Identidad del canal | Nombre y foto/logo del streamer |
| Metas y progreso | Meta de subs, meta de follows, meta de bits y celebracion |
| Patrocinadores y directo | Logos/videos, cronometro y categoria actual |
| Redes sociales y codigo de creador | Cuentas sociales y codigo promocional |
| Eventos y sonidos | Eventos visibles, sonidos y duracion del ticker |
| Apariencia | Colores, opacidad, tipografia y bordes |

Los cambios se guardan automaticamente en el navegador.

## Disenos Y Medidas Para OBS

| Diseno | Medida Recomendada |
|---|---|
| Compacto con patrocinadores y redes | 1200 x 204 |
| Compacto sin patrocinadores ni redes | 800 x 204 |
| Horizontal | 1920 x 116 |

En OBS:

1. Agrega una Fuente de navegador.
2. Pega el enlace generado por el panel.
3. Ajusta ancho y alto segun el diseno.
4. Activa `Refresh browser when scene becomes active`.

## Metas De Suscriptores

La meta de suscriptores usa los datos reales de Twitch obtenidos por Streamer.bot.

La meta se calcula por rangos:

- De 0 a 99: saltos de 10.
- De 100 a 999: saltos de 50.
- De 1000 en adelante: saltos de 100.

Ejemplos:

- 21 subs -> meta 30.
- 134 subs -> meta 150.
- 1340 subs -> meta 1400.

Al llegar a la meta, el widget espera unos segundos, muestra celebracion y luego actualiza a la siguiente meta.

## Meta De Follows

La meta de follows usa una logica similar a la meta de suscriptores.

- De 0 a 99: saltos de 10.
- De 100 a 999: saltos de 50.
- De 1000 en adelante: saltos de 100.

Si Streamer.bot envia el total de followers, el widget usa ese numero. Si solo llega un evento de follow, Streamer.bot suma 1 al acumulado guardado.

## Meta De Bits

La meta de bits tiene dos modos.

### Por Stream

- Empieza desde los bits actuales configurados en el admin.
- Suma cheers/bits recibidos durante el directo.
- Al llegar a la meta, se congela visualmente en objetivo/objetivo.
- Se reinicia al terminar el directo.
- Tambien suma al acumulado mensual interno.

### Mensual

- Usa la variable mensual persistente de Streamer.bot.
- Al llegar a la meta, el widget se congela visualmente en objetivo/objetivo.
- Streamer.bot sigue acumulando bits reales internamente.
- Si quieres una meta mas grande, vuelve al admin, sube el objetivo y copia un nuevo enlace.
- Los bits mensuales solo se reinician al cambiar de mes.

El admin no permite bajar los bits mensuales guardados en Streamer.bot.

## Cronometro

El cronometro usa el tiempo real del directo de Twitch.

Esto permite que si recargas OBS o cambias el enlace durante un directo, el cronometro no empiece desde cero, sino desde el tiempo real que lleva el stream.

## Estados Del Canal

- `EN VIVO`: Twitch esta online.
- `OFFLINE`: Twitch esta offline.
- `SIN SENAL`: el widget perdio conexion con Streamer.bot.

Si aparece `SIN SENAL`, revisa que Streamer.bot este abierto y que el WebSocket Server este activo.

## Solucion De Problemas

| Problema | Solucion |
|---|---|
| El widget muestra SIN SENAL | Abre Streamer.bot y revisa el WebSocket Server |
| No conecta con Streamer.bot | Verifica host `127.0.0.1` y puerto `8080` |
| No aparecen eventos | Revisa que la accion `Hipe Widget` este habilitada |
| No suenan eventos | Revisa sonido global, sonido por evento y volumen |
| No se ven imagenes | Usa enlaces publicos directos a imagen/video |
| El cronometro no coincide | Verifica triggers Twitch Stream Online/Offline |
| Bits mensuales no bajan | Es intencional; Streamer.bot protege el acumulado real |

## Archivos Principales

```text
admin.html              Panel de configuracion
widget.html             Overlay para OBS
codigosb.txt            Codigo C# de Streamer.bot para referencia
streamerbot-import.txt  Codigo de importacion de la accion
TESTING.md              Checklist de pruebas
assets/                 Imagenes, audio y favicon
```

## Notas

- La celebracion de metas actualmente es visual. Los sonidos pertenecen a los eventos del ticker, no a la celebracion como sonido independiente.
- El enlace generado contiene la configuracion del widget.
- Si cambias metas, colores, redes o eventos, copia de nuevo el enlace y actualizalo en OBS.
- Streamer.bot debe estar abierto para recibir eventos en tiempo real.
- El panel guarda tus preferencias en el navegador usando `localStorage`.

## Creditos

Desarrollado por [jsmoctezuma](https://github.com/jsmoctezuma).

Iconos por [Iconify](https://iconify.design). Fuentes por Google Fonts.
