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

Todos los botones abren `https://wa.me/525586353618` con un mensaje prellenado según el botón (diagnóstico, paquete Presencia, paquete Operación o consulta general).

## Probar en local

```
python3 -m http.server 8000
```

y abrir http://localhost:8000
