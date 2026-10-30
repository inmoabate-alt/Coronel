# Coronel Alegre · Abate Propiedades

Landing estática basada en la estructura de Delta Rodó para la propiedad AHO12365728. Datos e imágenes de la ficha proporcionada: USD 335.000, 2 dormitorios, 113 m² construidos, 100 m² cubiertos y garaje. WhatsApp de consultas: +598 96 329 700.

## Desarrollo

Desde el checkout existente `/workspace/Coronel`, ejecutar:

```sh
python3 -m http.server 3000 --bind 0.0.0.0
```

No requiere instalar dependencias ni compilar. Cada tarea ya está aislada; no crear worktrees salvo solicitud explícita.

## Contenido y comprobaciones

Editar `index.html` para los textos y `app.js` para las fotos y sus etiquetas. Las imágenes WebP están en `assets/`. Se incluye Meta Pixel 1905629136345100: PageView al cargar y Contact al pulsar WhatsApp. No hay formularios. El contacto abre WhatsApp al +598 96 329 700 con el mensaje «quiero más información sobre coronel alegre».

Validar con `node --check app.js` y revisar escritorio y móvil: portada, galería con flechas y Escape, detalles expandibles y destino del botón fijo de WhatsApp. Confirmar precio, disponibilidad y contacto antes de publicar. El workflow `.github/workflows/pages.yml` publica `main` mediante GitHub Pages. En Settings → Pages, seleccionar GitHub Actions como origen. La URL esperada es https://inmoabate-alt.github.io/Coronel/; verificar el despliegue antes de anunciarla como activa.

## Meta

En Administrador de eventos → Probar eventos, abrir la URL publicada y pulsar WhatsApp. Deben recibirse PageView y Contact. Contact mide el clic, no el envío del mensaje. Para separar esta propiedad de Delta Rodó, crear una conversión personalizada con evento Contact y URL que contiene `inmoabate-alt.github.io/Coronel/`. La validación local con el SDK simulado no demuestra recepción en Meta.
