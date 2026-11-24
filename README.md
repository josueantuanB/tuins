# Tuins — Landing page

Sitio estático (HTML + CSS, sin JavaScript ni frameworks) de la app **Tuins**, con la identidad de la Ruta 3 (Diéresis) v2.

## Estructura

```
index.html              Página principal
sobre-nosotros.html     Qué es Tuins y quién está detrás
contacto.html           Canal de contacto
aviso-legal.html        Aviso legal del sitio
privacidad.html         Política de privacidad del sitio
css/styles.css          Estilos (responsive, móvil incluido)
assets/fonts/           Fredoka y Nunito en woff2 (subconjunto latino) + licencias OFL
assets/img/             Logo y símbolo en SVG
assets/icons/           Favicon SVG, ícono de iPhone y de Android
assets/og/tuins-og.jpg  Imagen para compartir en redes (1200 × 630)
favicon.ico             Favicon clásico
site.webmanifest        Datos para instalar la web en el teléfono
robots.txt              Permite a los buscadores rastrear el sitio (ver "Raíz del dominio")
sitemap.xml             Lista de páginas para Google
```

## Raíz del dominio

Los buscadores y los asistentes de IA solo leen `robots.txt` y `llms.txt` en la raíz del dominio (`josueantuanb.github.io/`), y este sitio vive en `/tuins/`. Por eso los que cuentan hoy están en otro repositorio, [`josueantuanB.github.io`](https://github.com/josueantuanB/josueantuanB.github.io), cuyo `robots.txt` declara el `sitemap.xml` de aquí. Si agregas o quitas páginas, actualiza `sitemap.xml` en este repo y `llms.txt` en el otro.

El `robots.txt` de este repo solo surtirá efecto si el sitio pasa a un dominio propio.

## Seguridad

GitHub Pages no permite configurar cabeceras HTTP, así que la política de seguridad de contenido (CSP) va en un `<meta>` al inicio de cada página. Solo permite recursos de este mismo sitio: si agregas scripts, fuentes, imágenes o analítica de otro dominio, hay que permitirlos ahí o el navegador los bloqueará. Las cabeceras `X-Content-Type-Options` y `X-Frame-Options` no se pueden definir en GitHub Pages.

## Cómo verla

- Rápido: abre `index.html` en el navegador.
- Como en un servidor real (recomendado): en esta carpeta ejecuta `python3 -m http.server 8000` y entra a http://localhost:8000

## Antes de publicar: reemplaza esto

| Qué | Dónde |
|---|---|
| `https://josueantuanb.github.io/tuins` → tu dominio propio (cuando lo tengas) | Todas las páginas `.html` (canonical, Open Graph, datos estructurados), `robots.txt`, `sitemap.xml` y el repo de la raíz del dominio |
| Enlaces de App Store y Google Play (`href="#"`) | `index.html` (hero y llamado final, marcados con `TODO`) |
| Precio y próximas ciudades | `index.html`, preguntas frecuentes |
| Instagram y TikTok | `index.html`, pie de página |
| Correo o redes de contacto (hoy, el perfil de GitHub del fundador) | `contacto.html` |

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
