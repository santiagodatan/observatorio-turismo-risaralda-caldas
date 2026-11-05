# Observatorio de Turismo de Proximidad — primera versión

Sitio estático en HTML, JavaScript y Apache ECharts, alimentado por `datos.json`.

## Publicar en GitHub Pages
1. Crear un repositorio público de GitHub.
2. Subir `index.html` y `datos.json` a la raíz del repositorio.
3. Ir a **Settings → Pages → Build and deployment** y elegir **Deploy from a branch**, rama `main`, carpeta `/(root)`.
4. Abrir el enlace publicado. La biblioteca ECharts se carga desde un CDN, por lo que requiere conexión a Internet.

## Ver localmente
No abrir `index.html` con doble clic, porque los navegadores pueden bloquear `fetch` sobre `file://`. En la carpeta ejecutar `python -m http.server 8000` y abrir `http://localhost:8000`.

## Advertencias metodológicas
- El archivo contiene registros analíticos y respuestas categóricas, no nombres, teléfonos ni correos. Antes de publicar, revisar categorías poco frecuentes y cualquier riesgo de reidentificación.
- Noches, personas por grupo y presupuestos excluyen datos faltantes o no numéricos; las cantidades válidas se indican en las tarjetas.
- La suma de presupuestos es exclusivamente muestral, no derrama económica.
- Las respuestas de municipios y alojamientos pueden tener categorías con ortografías distintas; requieren homologación.
- La versión inicial muestra distribuciones y comparaciones de encuestas; no infiere variaciones en flujos totales de visitantes.
