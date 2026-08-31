# gotcha

Something non-obvious that failed or must be kept in mind to avoid repeating (bugs, surprises, lessons).

## El favicon inline hace que un grep de "http" dé falso positivo

**What** — `index.html` tiene el favicon como data-URI con un SVG inline, y ese
SVG incluye `xmlns='http://www.w3.org/2000/svg'`. Un `grep http index.html`
devuelve ese match aunque la página no haga ni una sola request externa.

**Why** — `xmlns` es un identificador de namespace XML, no una URL que el
navegador vaya a buscar. Vale la pena saberlo porque el criterio de aceptación
de la landing es "cero llamadas externas": al auditarlo, ese match parece una
violación y no lo es. El favicon está inline justamente para evitar la request
a `/favicon.ico`.

**Where** — `index.html`, atributo `<link rel="icon">`.

**Learned** — 2026-08-31, verificando la landing contra el criterio de red.
