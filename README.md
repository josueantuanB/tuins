# Tuins — Landing page

Sitio estático (HTML + CSS, sin JavaScript ni frameworks) de la app **Tuins**, con la identidad de la Ruta 3 (Diéresis) v2.

## Estructura

```
index.html              Página principal
css/styles.css          Estilos (responsive, móvil incluido)
assets/fonts/           Fredoka y Nunito en woff2 (subconjunto latino) + licencias OFL
assets/img/             Logo y símbolo en SVG
assets/icons/           Favicon SVG, ícono de iPhone y de Android
assets/og/tuins-og.jpg  Imagen para compartir en redes (1200 × 630)
favicon.ico             Favicon clásico
site.webmanifest        Datos para instalar la web en el teléfono
robots.txt              Permite a los buscadores rastrear el sitio
sitemap.xml             Lista de páginas para Google
```

## Cómo verla

- Rápido: abre `index.html` en el navegador.
- Como en un servidor real (recomendado): en esta carpeta ejecuta `python3 -m http.server 8000` y entra a http://localhost:8000

## Antes de publicar: reemplaza esto

| Qué | Dónde |
|---|---|
| `https://josueantuanb.github.io/tuins` → tu dominio propio (cuando lo tengas) | `index.html` (canonical, Open Graph, datos estructurados), `robots.txt`, `sitemap.xml` |
| Enlaces de App Store y Google Play (`href="#"`) | `index.html` (hero y llamado final, marcados con `TODO`) |
| Precio y próximas ciudades | `index.html`, preguntas frecuentes |
| Términos, Privacidad, Contacto, Instagram, TikTok | `index.html`, pie de página |

Busca `TODO` y `josueantuanb.github.io/tuins` en los archivos para encontrarlos todos.

## SEO incluido

- `<title>` y meta description pensados para búsquedas como "encontrar con quién ir", "planes en Quito" y "app para hacer amigos".
- HTML semántico: un solo `<h1>`, secciones con `<h2>`/`<h3>`, `<nav>`, `<main>`, `<footer>`, lista ordenada para los pasos.
- URL canónica, `meta robots`, `lang="es"` y `og:locale` es_EC.
- Open Graph y tarjeta de X/Twitter con imagen propia de 1200 × 630.
- Datos estructurados JSON-LD (schema.org): Organization, WebSite, WebPage, MobileApplication y FAQPage.
- `robots.txt` y `sitemap.xml`.
- Rendimiento: sin JavaScript, fuentes propias en woff2 con `preload` y `font-display: swap`, imágenes con `width`/`height` (evita saltos de diseño) y carga diferida debajo del pliegue.
- Accesibilidad (también cuenta para SEO): enlace "Saltar al contenido", textos alternativos, contraste AA, foco visible y soporte para "reducir movimiento".
- Favicons, ícono de iPhone y manifest.

## Después de publicar

1. Da de alta el dominio en Google Search Console y envía `sitemap.xml`.
2. Revisa los datos estructurados con la Prueba de resultados enriquecidos de Google.
3. Pasa Lighthouse (Chrome → DevTools → Lighthouse) en la versión publicada.
4. Comprueba cómo se ve al compartir el enlace (por ejemplo, pegándolo en WhatsApp).

## Fuentes

Fredoka y Nunito son de Google Fonts, con licencia SIL Open Font License 1.1 (uso comercial permitido). Las licencias están en `assets/fonts/`.
