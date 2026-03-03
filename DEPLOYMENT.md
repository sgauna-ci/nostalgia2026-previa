# Landing 2026 en `/2026`

## Objetivo

Publicar esta landing en:

- `https://lafiestadelanostalgia.com/2026`

sin tocar todavía:

- `https://lafiestadelanostalgia.com/`

## Estado del proyecto

Esta landing es estática:

- `index.html`
- `assets/css/styles.css`
- `assets/js/main.js`

Usa rutas relativas para CSS, JS e imágenes, por lo que se adapta bien a vivir debajo de `/2026` siempre que el servidor preserve esa estructura.

## Publicación recomendada

### Origen AWS

Subir el contenido de esta carpeta a un origen estático:

- S3
- servido por CloudFront

## Estructura esperada del origen

En el origen que responda a `/2026`, debería existir:

- `/2026/index.html`
- `/2026/assets/...`

## CloudFront

En la distribución principal del dominio:

- behavior `/2026*` -> origen estático de esta landing
- behavior `/ticketing*` -> origen del sistema de venta
- behavior `*` -> sitio principal actual

## Nota

No conviene depender de GitHub Pages para el dominio final bajo `/2026`. GitHub puede seguir como repositorio de código, pero el hosting final debería resolverse desde AWS para poder enrutar por path bajo el mismo dominio principal.
