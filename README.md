# Portfolio — Leandro Romero Morel

Sitio de una sola página: `index.html` + carpetas `img/` y `cv/`. HTML5, Tailwind CSS por CDN y JavaScript, sin build.

## Estructura
```
portfolio/
├── index.html   → página completa (textos, estilos y lógica)
├── img/         → foto y capturas de los proyectos (.webp)
└── cv/          → CV en PDF (botón "Descargar CV")
```

## Probarlo
Abrí `index.html` con doble clic, o en VS Code con la extensión Live Server.

## Editar
Todo lo que cambia seguido está al final de `index.html`, en el bloque `CONFIGURACIÓN`:
- `PROFILE`: email, GitHub, LinkedIn, ruta del CV.
- `PROJECTS`: los proyectos, en el orden en que aparecen.
- `SKILLS`: el stack tecnológico.

Los textos del inicio y de "Cómo trabajo" están en el HTML, marcados con ✏️.

## Agregar un proyecto
1. Sacá dos capturas de página completa (en Chrome: F12 → Ctrl+Shift+P → "Capture full size screenshot"):
   - compu: ventana de 1440 px de ancho
   - celular: activá el modo dispositivo (Ctrl+Shift+M) en 390 px de ancho
2. Pasalas a .webp (por ejemplo en squoosh.app) y guardalas en `img/`.
3. Copiá un bloque dentro de `PROJECTS` y completalo:
```js
{
  title: 'Nombre del proyecto',
  client: 'Cliente',                 // o 'Emprendimiento propio'
  problem: 'Qué es y qué problema resuelve.',
  highlights: ['Punto 1', 'Punto 2', 'Punto 3'],
  category: 'frontend',              // 'frontend' o 'fullstack'
  tags: ['HTML5', 'CSS3', 'JavaScript'],
  demo: 'https://mi-sitio.vercel.app/',   // '' muestra "Publicación próximamente"
  repo: 'https://github.com/leanromorel/mi-repo',
  screens: [{ label: 'Sitio', desktop: 'img/mi-sitio-desktop-full.webp', mobile: 'img/mi-sitio-mobile-full.webp' }]
}
```
Para mostrar más de una pantalla (como Tienda / Panel admin en Mola), agregá más objetos en `screens`.

## Publicar en Vercel
1. Creá un repo `portfolio` en GitHub y subí esta carpeta.
2. En vercel.com → Add New → Project → importá el repo → Deploy (no hay comando de build).
