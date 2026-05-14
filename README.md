
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
