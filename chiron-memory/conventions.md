# convention

A rule, pattern or convention this project follows (naming, formats, repeated approach).

## styles.css usa variables de color en :root, soporte de modo oscuro vía prefers-color-sche…

What: styles.css usa variables de color en :root, soporte de modo oscuro vía prefers-color-scheme, tipografía fluida con clamp(), y un único breakpoint en ~720px con enfoque mobile-first · Why: — · Where: styles.css <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-4 -->

## Aunque no lo pedían los criterios de aceptación, se incluyó una base de accesibilidad en…

What: Aunque no lo pedían los criterios de aceptación, se incluyó una base de accesibilidad en la landing: skip link, jerarquía de headings semántica, estilos :focus-visible visibles y respeto de prefers-reduced-motion en las animaciones/scroll · Why: — · Where: index.html, styles.css <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-7 -->

## Para verificar el requisito de "sin inputs/formularios/backend" se usa grep sobre los arc…

What: Para verificar el requisito de "sin inputs/formularios/backend" se usa grep sobre los archivos buscando ausencia de <form>, <input>, <button>, <script>, fetch, onclick, y ausencia de URLs externas en href/src/url(), en vez de un test automatizado · Why: es un sitio estático sin build ni test runner, así que la validación de "contenido puramente estático" se hace por inspección de texto plano <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-8 -->

## El copy pendiente de definir (nombre del producto, propuesta de valor, etc.) se marca ent…

What: El copy pendiente de definir (nombre del producto, propuesta de valor, etc.) se marca entre corchetes como placeholder explícito (ej. [Nombre del producto]) en vez de inventar contenido definitivo · Why: el repo no tenía ninguna descripción del producto real, así que se optó por dejar el hueco visible en un solo lugar para completar después, en vez de rellenar con copy inventado · Where: index.html, chiron-memory/conventions.md <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-2 -->
