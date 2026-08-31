# convention

A rule, pattern or convention this project follows (naming, formats, repeated approach).

## El copy pendiente se marca [entre corchetes]

**What** — En el HTML del sitio, todo texto que es placeholder y espera copy
real va [entre corchetes], y arriba del `<body>` hay un comentario que los
lista en orden de aparición.

**Why** — Hace que reemplazar contenido sea un find-and-replace de `[` en vez de
una lectura completa del archivo, y hace obvio en un diff o en la página
renderizada qué quedó sin escribir. Un placeholder que parece copy real (texto
lorem ipsum, o nombres plausibles inventados) se publica sin que nadie lo note.

**Where** — `index.html`.

**Learned** — 2026-08-31, al entregar la landing sin tener definido el producto.
