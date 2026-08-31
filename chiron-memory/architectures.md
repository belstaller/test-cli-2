# architecture

A structural/design choice: layers, module boundaries, where things live.

## La landing page es un sitio estático de un solo archivo HTML más una hoja de estilos, sin…

What: La landing page es un sitio estático de un solo archivo HTML más una hoja de estilos, sin JavaScript, sin bundler y sin backend · Why: — · Where: index.html, styles.css en la raíz del repo <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-3 -->

## index.html y styles.css se colocan en la raíz del repo, no en /src o /public

What: index.html y styles.css se colocan en la raíz del repo, no en /src o /public · Why: así cualquier host estático o GitHub Pages puede servir el sitio sin configuración adicional · Where: index.html, styles.css <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-1 -->

## El favicon se implementa como SVG inline en formato data-URI dentro del <head> de index.h…

What: El favicon se implementa como SVG inline en formato data-URI dentro del <head> de index.html, no como archivo aparte · Why: mantiene el sitio a exactamente dos archivos (index.html, styles.css) sin ninguna petición de red adicional, coherente con el requisito de cero llamadas externas · Where: index.html <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-6 -->
