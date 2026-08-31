# test-cli-2

Landing page estática de una sola página. Puramente informativa: no tiene
formularios, ni JavaScript, ni backend, ni dependencias.

## Ver la página

Doble clic en `index.html` — se abre en el navegador y funciona.

Si preferís servirla por HTTP (más parecido a producción, y necesario si
después agregás rutas):

```sh
python3 -m http.server 8000
# http://localhost:8000
```

No hay `npm install` ni paso de build: lo que está en el repo es lo que se
publica. Sirve tal cual en GitHub Pages, Netlify, S3 o cualquier host estático.

## Editar el contenido

Todo el texto a reemplazar está **[entre corchetes]** en `index.html`. Buscá
`[` y los encontrás todos; arriba del `<body>` hay un comentario que los lista
en orden. Los principales:

| Placeholder | Qué va |
| --- | --- |
| `[Nombre del producto]` | El nombre real (título, marca del header, footer) |
| `[Tagline corto]` | 3 a 6 palabras, aparece en la pestaña del navegador |
| `[Titular ...]` | El headline del hero |
| `[Beneficio 1..3]` | Los tres puntos de valor |
| `[hola@ejemplo.com]` | Datos de contacto |

Los datos de contacto son texto plano a propósito (el criterio era "contacto
como texto estático"). Si querés que el email sea clicable, envolvelo en
`<a href="mailto:...">` — sigue sin haber backend de por medio.

## Cambiar el diseño

Los colores, el radio de los bordes y el ancho máximo son variables CSS al
principio de `styles.css`, en `:root`. Cambiándolas ahí se actualiza toda la
página. El modo oscuro se resuelve solo con `prefers-color-scheme` y usa las
mismas variables.

El layout es mobile-first con un único breakpoint en `720px`, al final del
archivo: arriba de esa medida el nav pasa a horizontal y las grillas de 1 a 3
columnas.

## Estructura

```
index.html    # header + hero + producto + contacto + footer
styles.css    # estilos, mobile-first, un breakpoint
```
