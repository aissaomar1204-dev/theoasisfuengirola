# 🌴 The Oasis — Fuengirola

Web oficial de **The Oasis** (`theoasisfuengirola.com`), takeaway premium de comida saludable (açaí bowls, smoothies, zumos fríos y crepes) en Av. Ramón y Cajal 30, Fuengirola.

## Estructura del sitio

| Ruta | Uso |
|---|---|
| `index.html` | Home bilingüe ES/EN (mobile-first, pensada para QR y Google Maps) |
| `acai-bowls-fuengirola/` | Landing SEO — keyword "açaí bowl Fuengirola" |
| `smoothies-zumos-fuengirola/` | Landing SEO — keyword "smoothies / zumos naturales Fuengirola" |
| `crepes-gofres-fuengirola/` | Landing SEO — keyword "crepes / gofres Fuengirola" |
| `en/` | Landing en inglés para turistas (con hreflang) |
| `carta.html` | Carta 3 columnas para el **televisor de 50"** del local (noindex) |
| `sitemap.xml` / `robots.txt` | Infraestructura de rastreo |
| `404.html` | Página de error personalizada |
| `CNAME` | Dominio personalizado para GitHub Pages |
| `logo.png` | Logo de la marca |
| `lista-compra.md` / `costes-margenes.md` | Documentos internos del negocio (no se enlazan desde la web) |

## 🚀 Publicar con el dominio propio

1. Sube todo el proyecto a un repositorio de GitHub.
2. **Settings → Pages → Source: Deploy from a branch → `main` / root**.
3. En **Settings → Pages → Custom domain** escribe `theoasisfuengirola.com` (el archivo `CNAME` ya lo deja fijado) y activa **Enforce HTTPS** cuando esté disponible.
4. En el panel DNS de tu registrador de dominio crea:
   - 4 registros **A** para `@` (apex): `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - 1 registro **CNAME** para `www` → `TU-USUARIO.github.io`
5. La propagación tarda de minutos a unas horas. Verifica en `https://theoasisfuengirola.com`.

## 🔍 Después de publicar (SEO — hazlo la primera semana)

1. **Google Search Console**: da de alta la propiedad `theoasisfuengirola.com`, verifica por DNS y envía `sitemap.xml`.
2. **Google Business Profile** (lo más importante para salir en el mapa): crea/reclama la ficha con el MISMO nombre, dirección y teléfono que la web, categoría "Tienda de zumos" o "Restaurante de comida saludable", añade fotos reales y el enlace a la web.
3. **Reseñas**: pon un QR en el mostrador que lleve a la ficha de Google — las reseñas son el factor nº 1 del ranking local.
4. **Bing Places** y **Apple Maps** (Apple Business Connect): 10 minutos cada uno, tráfico extra gratis.

## 📺 Poner la carta en el televisor

1. Abre `https://theoasisfuengirola.com/carta.html` en el navegador del televisor.
2. Pulsa **F11** (pantalla completa). Reloj en directo, fondo de oasis animado y auto-refresco cada 6 h.

## 🌐 Idiomas

- **Home**: botón **ES · EN** en la navbar (elección guardada en localStorage).
- **`/en/`**: landing indexable en inglés con `hreflang` (la que posiciona en búsquedas en inglés).
- **Carta TV**: bilingüe permanente (traducción en cursiva bajo cada línea).

## 💶 Precios y tamaños

- Bowls en 4 tamaños (**S/M/L/XL**), bebidas en 3 (**S/M/L**), ordenados de más barato a más caro.
- Los precios están en el HTML (mejor para SEO). Si cambias uno, actualízalo en: `index.html`, `carta.html` y la landing de su categoría.

## ✏️ Pendiente de personalizar

- **Redes sociales**: busca `theoasisfuengirola` y pon los usuarios reales de Instagram/TikTok.
- **Fotos reales**: sustituye el visual del hero por una foto del açaí bowl (bloque comentado en `index.html`). Las fotos reales también mejoran el CTR en Google.

## 🛠️ Stack

- HTML5 semántico + Tailwind CSS por CDN + JavaScript vanilla (sin build).
- Iconografía SVG propia inline (sin emojis ni librerías).
- SEO: canonical + hreflang ES/EN, Open Graph, sitemap, robots, migas de pan y JSON-LD (`Restaurant`, `BreadcrumbList`, `FAQPage` en cada landing).
- Accesibilidad: ARIA en tabs y FAQs, contraste alto, `prefers-reduced-motion`.
