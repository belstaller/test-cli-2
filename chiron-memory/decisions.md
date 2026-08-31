# decision

A technical decision that was made and WHY (which alternatives were discarded).

## Landing page en HTML + CSS plano, sin build ni dependencias

**What** — La landing (`index.html` + `styles.css` en la raíz del repo) es HTML
y CSS escritos a mano: sin bundler, sin framework, sin framework de CSS, sin
JavaScript y sin `package.json`. La identidad visual sale de variables CSS en
`:root` y el responsive de un único breakpoint en 720px.

**Why** — El pedido era una página puramente informativa, sin input de usuario
ni persistencia. Astro / Vite / Next agregarían `node_modules`, un lockfile y un
paso de build a un repo que todavía no tiene stack elegido, a cambio de nada:
no hay componentes que reutilizar ni contenido que generar. Tailwind por CDN
quedó descartado por una razón extra: el criterio de aceptación exigía cero
llamadas de red, y un CDN es exactamente eso. Consecuencia práctica: lo que está
en el repo es lo que se publica, sirve en cualquier host estático y no se rompe
con el tiempo por dependencias que envejecen.

**Where** — `index.html`, `styles.css`, y el README documenta el flujo de edición.

**Learned** — 2026-08-31, construyendo la landing inicial del proyecto.
