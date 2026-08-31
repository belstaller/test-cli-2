# decision

A technical decision that was made and WHY (which alternatives were discarded).

## La landing page se construyó como HTML+CSS plano, sin build tool ni dependencias externas

What: La landing page se construyó como HTML+CSS plano, sin build tool ni dependencias externas · Why: se descartaron Astro/Vite/Tailwind por ser sobre-ingeniería para una página estática de una sola sección sin necesidad de build; también evita llamadas a CDN, lo cual choca con el requisito de 'sin llamadas externas/backend' · Where: index.html, styles.css, chiron-memory/decisions.md <!-- id: 5e707f3d-ddd7-4ef1-b49a-fc7a6380710f-0 -->
