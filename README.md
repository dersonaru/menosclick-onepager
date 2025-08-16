# MenosClick – OnePager (estático)

Este repo contiene una **OnePager HTML** simple (sin frameworks ni build). Sirve para enviar propuestas personalizadas con parámetros en la URL.

## Archivos
- `index.html` → plantilla principal. Se personaliza con parámetros:
  - `name` (nombre del negocio)
  - `logo` (URL del logo)
  - `primary` (color en HEX, ej. `#8B5A2B`)
  - `cta` (URL del botón “Quiero empezar”, ej. WhatsApp)
  - `call` (URL del botón “Agendar llamada”, ej. Calendly)
- `atcm.html`, `restaurante-demo.html`, `cafeteria-demo.html` → páginas de **redirección** que apuntan a `index.html` con parámetros ya listos.

> Todas las páginas tienen `noindex, nofollow` para que no se indexen.

## Ejemplos
- Template directo: `/index.html?name=All%20Things%20Chocolate%20%26%20More&primary=%238B5A2B`
- Atajos: `/atcm.html`, `/restaurante-demo.html`, `/cafeteria-demo.html`

## Deploy en Vercel (sin build)
1. Crea el repo y sube estos archivos a la **raíz**.
2. En Vercel → New Project → Importa el repo.
3. En la configuración deja todo vacío: *Build Command* (vacío) y *Output Directory* `.`
4. Deploy. Listo.

## Subdominio (opcional)
- En Vercel agrega `p.tudominio.com` y copia el **CNAME**.
- En Namecheap → DNS → crea un **CNAME** con Host `p` apuntando al CNAME de Vercel.
- Espera unos minutos y prueba: `https://p.tudominio.com/atcm.html`

— 2025-08-16 21:19
