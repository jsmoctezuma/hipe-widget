
### 4. Añadir el widget a OBS

- En OBS, crea una nueva fuente **Browser Source**.
- Pega el enlace copiado.
- Configura el ancho y alto según tu diseño:
- **Compacto con patrocinadores y redes**: 1200 × 204
- **Compacto sin patrocinadores** (solo ticker): 800 × 204
- **Horizontal (completo)**: 1920 × 116
- (Opcional) Activa **"Refresh browser when scene becomes active"** para asegurar la conexión WebSocket.

### 5. Verificar la conexión con Streamer.bot

- Asegúrate de que Streamer.bot tenga el **WebSocket Server** activo (puerto 8080 por defecto).
- El widget mostrará "Bienvenido ✓ — Sistema en línea" cuando la conexión sea exitosa.
- Prueba un evento (por ejemplo, un follow falso) para ver si aparece en el ticker y suena la notificación.

## 🎨 Personalización avanzada

Puedes modificar los archivos HTML/CSS directamente si deseas cambiar la apariencia más allá de lo que ofrece el admin. Todos los estilos están en `widget.html` dentro de la etiqueta `<style>`.

## ❓ Solución de problemas

- **El widget no se conecta**: Revisa que Streamer.bot esté abierto, que el WebSocket Server esté activo (pestaña **General** → **WebSocket Server**) y que el puerto coincida con el configurado en el admin (8080 por defecto).
- **No se ven las imágenes**: Asegúrate de que la carpeta `assets` contenga los archivos `logo.png`, `corazon.gif`, etc., y que las rutas sean relativas correctas. Si usas enlaces externos (Imigur), verifica que sean públicos.
- **El sonido no se reproduce**: Comprueba que el archivo `notification.mp3` esté en `assets` y que el volumen no esté al 0%. Además, algunos navegadores requieren una interacción previa; en OBS no hay ese problema.
- **El ticker corta el texto**: El widget ajusta automáticamente el tamaño de la fuente. Si aún así se corta, revisa que el ancho del Browser Source sea el adecuado.

## 📝 Créditos

Desarrollado por [jsmoctezuma](https://github.com/jsmoctezuma)  
Iconos por [Iconify](https://iconify.design/)  
Fuentes: Rajdhani y Barlow Condensed (Google Fonts)

## 📄 Licencia

Puedes usar, modificar y distribuir este widget libremente. No se requiere atribución, pero se agradece.
