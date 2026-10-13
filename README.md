# riablo-web

Sitio oficial de Riablo Studio — https://riablostudio.com

Sitio estático (HTML + CSS + JS sin dependencias). Hostinger lo publica automáticamente desde la rama `main`.

## Estructura

```
index.html            Página completa (estilos y script incluidos)
assets/
  riablo-logo-*.png   Logotipo original (positivo y negativo), recortado del manual de marca
  riablo-r*.png       Isotipo R (rojo, blanco, tinta)
  hero.webm / .mp4    Video del hero en blanco y negro (WebM VP9 + MP4 H.264)
  hero-poster.jpg     Cuadro fijo del video (carga inicial y movimiento reducido)
  og-image.png        Imagen para compartir en redes
  favicon.png, apple-touch-icon.png
robots.txt, sitemap.xml
```

## Reglas de marca aplicadas

- Paleta: blanco papel #FFFFFF domina, negro tinta #0E0E0E sostiene, gris piedra #5C5C5C para secundarios, niebla #F2F2F2 para superficies, rojo sello #F50808 solo como acento gráfico (nunca en texto pequeño: 4.3:1 no pasa AA).
- Tipografía: Outfit (texto), Michroma (titulares cortos y cifras, nunca < 18 px), Instrument Serif itálica (una palabra de acento por bloque).
- El logotipo no se redibuja: se usa el archivo extraído del manual.
- Todo texto cumple contraste WCAG AA.

## WhatsApp

Todos los botones abren `https://wa.me/525586353618` con un mensaje prellenado según el botón (diagnóstico o el caso que la persona eligió en "Lo que te pasa").

## Google Analytics y Google Ads

- **Google Analytics 4:** instalado con la etiqueta oficial de Google (`G-DNKM7EBHP7`), justo después de `<head>` en `index.html`.
- **Google Ads:** en ese mismo bloque está `window.RIABLO_TAGS`. Escribe ahí el ID de Google Ads (`AW-…`) y la etiqueta de la conversión "Clic a WhatsApp". Mientras estén vacíos, solo se mide con Analytics.

Eventos que se envían:

| Evento | Cuándo | Datos |
|---|---|---|
| `generate_lead` | Clic en cualquier botón de WhatsApp | `method`, `link_location` (dónde estaba el botón), `link_text` |
| `conversion` (Google Ads) | El mismo clic, si hay `ads` y `adsLeadLabel` | `send_to` |
| `contact` | Clic en el correo | `method: email` |
| `click_instagram` | Clic en Instagram | `link_location` |
| `select_content` | Alguien abre un caso de "Lo que te pasa" | `item_id` (el caso) |

En GA4 marca `generate_lead` como **evento clave**.

## Probar en local

```
python3 -m http.server 8000
```

y abrir http://localhost:8000
