# Mr. Brasa — Sitio web

Sitio web de una sola página para **Mr. Brasa** (HR Desarrollo Empresarial S.A.C.), pollería en Av. Giraldez 786, Huancayo.

## Estructura del proyecto

```
/assets
  /images       → fotos del local, hero, menú y galería
  /icons        → favicon y apple-touch-icon
/css
  styles.css    → todos los estilos del sitio
/js
  main.js       → loader, menú móvil, tabs de menú, countdown, contador de stats, acordeón FAQ, lightbox
index.html
robots.txt
sitemap.xml
README.md
```

## Cómo personalizar

### 1. Fotografías (lo más importante)
Ahora mismo el sitio usa **imágenes de marcador de posición** generadas automáticamente (fondo oscuro con el nombre del plato) para que puedas ver el diseño completo funcionando. Reemplázalas por tus fotos reales, manteniendo el mismo nombre de archivo, en:
- `assets/images/menu/` — una foto por producto del menú
- `assets/images/gallery/` — fotos del local y platos para la galería
- `assets/images/og-cover.jpg` — imagen que se muestra al compartir el link en WhatsApp/Facebook (1200x630px)
- `assets/icons/favicon.png` y `apple-touch-icon.png` — ícono de pestaña del navegador (idealmente tu logo real)

También puedes reemplazar el fondo del Hero: busca `.hero__bg` en `css/styles.css` y agrega `background-image: url('../assets/images/hero.jpg');` con tu foto de fachada.

### 2. Redes sociales
Busca `href="#"` junto a los íconos de Instagram, Facebook y TikTok (aparecen dos veces: en Contacto y en el Footer) y coloca tus enlaces reales.

### 3. Estadísticas
La sección de estadísticas (contador animado) usa cifras de referencia marcadas con `data-count` en `index.html`. Reemplázalas por tus datos reales cuando los tengas (años de experiencia, pedidos atendidos, calificación de Google, etc.).

### 4. Testimonios
Los tres testimonios son de ejemplo. Reemplázalos por reseñas reales de clientes (puedes copiarlas de tu perfil de Google Maps).

### 5. Promoción y cuenta regresiva
La promoción destacada y el temporizador están en la sección `#promociones`. El contador se reinicia automáticamente cada domingo a las 23:59 — puedes cambiar la oferta editando el texto y el enlace de WhatsApp.

### 6. PedidosYa
El sitio ya incluye tu enlace de PedidosYa (botón en el Hero, en Contacto y en el Footer). Si el link de tu tienda cambia, búscalo y reemplázalo en `index.html` — aparece 3 veces.

### 7. Precios y productos del menú
Todo el menú (Pollo a la Brasa, Acompañamientos, Bebidas) ya tiene tus productos y precios reales tomados de tu ficha de Google. Si cambian los precios, edítalos directamente en las tarjetas `.menu-card` dentro de `index.html`.

### 8. Dominio
Este proyecto usa `https://www.mrbrasa.pe/` como URL de referencia en el SEO (meta tags, Schema.org, sitemap.xml, robots.txt). Cuando tengas tu dominio definitivo, reemplaza esa URL en:
- `index.html` (meta `og:url`, `canonical`, JSON-LD)
- `sitemap.xml`
- `robots.txt`

## Funcionalidades incluidas

- Diseño responsive (móvil, tablet, escritorio)
- Menú de navegación con efecto sticky y versión hamburguesa en móvil
- Botón flotante de WhatsApp y botón "volver arriba"
- Loader de entrada
- Animaciones al hacer scroll (AOS)
- Tabs de categorías en el menú
- Cuenta regresiva de promoción
- Contador animado de estadísticas
- Acordeón de preguntas frecuentes
- Galería con lightbox
- Mapa de Google Maps integrado
- SEO: metaetiquetas, Open Graph, Twitter Cards, datos estructurados Schema.org (Restaurant), sitemap.xml y robots.txt
- Accesibilidad: etiquetas ARIA, navegación por teclado, textos alternativos en imágenes, buen contraste

## Cómo publicarlo

Puedes subir esta carpeta tal cual a cualquier hosting estático (Hostinger, Netlify, Vercel, GitHub Pages, etc.). No requiere backend ni build: es HTML, CSS y JS puro.
