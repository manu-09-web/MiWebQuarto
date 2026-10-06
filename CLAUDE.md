# manu.dev — blog personal de Manuel Herrera

Blog dev personal hecho con **Quarto** (generador de sitios estáticos). Es una tarea de la carrera
(Ingeniería en Tecnologías de la Información e Innovación Digital, Universidad Politécnica de Chiapas).
Aquí se publican experiencias de la carrera y cosas que Manuel va aprendiendo. Todo el contenido va en español.

## Comandos

- `quarto preview` — levanta el sitio y recarga al guardar. Úsalo para verificar cada cambio.
- `quarto render` — genera el sitio en `_site/`.

El sitio todavía **no se ha probado completo**: se armó sin poder ejecutar Quarto. Lo primero es correr
`quarto preview` y corregir cualquier error antes de cambiar otra cosa.

## Estructura

- `_quarto.yml` — configuración, navbar, SEO (site-url, Open Graph, RSS, canonical).
- `index.qmd` — landing: hero, sobre mí, lenguajes, proyectos, certificaciones, contacto. Es HTML dentro de un bloque `{=html}`.
- `blog.qmd` — página del blog. Usa la plantilla `ejs/blog.ejs` (post destacado + lista por año).
- `feed.qmd` — catálogo de entradas. Usa `ejs/feed.ejs` (tarjetas en 2 columnas, paginación).
- `posts/<slug>/index.qmd` — cada entrada con sus imágenes. `posts/_metadata.yml` tiene las opciones comunes.
- `styles/theme.scss` — todo el diseño. Los colores están arriba como variables Sass.
- `assets/site.html` — JS: filtro por categoría, buscador, paginación, tiempo de lectura, barra de progreso.
- `assets/head.html` — fuentes (Geist y Geist Mono) y metas.
- `.github/workflows/publish.yml` — publica en GitHub Pages en cada push a `main`.

## Diseño (decisiones ya tomadas)

- Paleta de Manuel: fondo `#000020`, superficies `#171a4a`, índigo `#2f2c79`, grises `#666666` y `#8c8c8c`.
  El acento `#9d9aff` es el índigo aclarado para que se lea sobre el fondo.
- Estilo "premium", no genérico: bordes finos, un solo resplandor índigo arriba, botones tipo píldora,
  mucho aire. **No** usar cuadrícula de fondo, degradados azul-verde ni los tres puntitos de colores en el código.
- Principio que pidió Manuel: los elementos de una sección (campos, tarjetas, listas) deben medir lo mismo de ancho.
- Las clases CSS propias llevan prefijo `md-`.
- Una versión anterior en gris casi negro con acento naranja **no le gustó**; no volver a eso.
- Los bocetos originales definen cuatro pantallas: landing, blog, entrada y feed. Se puede mejorar el look,
  pero sin perder esa estructura.

## Contenido

- Solo dos proyectos en todo el sitio: **EduControl** y **Gym Tracker**. No agregar otros sin que lo pida.
- Posts publicados: `posts/kotlin-compose` (Gym Tracker) y `posts/proyecto-integrador` (EduControl).
- Los posts se escriben en primera persona con lo que Manuel hizo de verdad. No inventar datos,
  opiniones ni detalles técnicos; si falta información, preguntarle.
- Certificaciones: solo la lista (nombre, institución, fecha). No publicar los PDF.
- En EduControl no mostrar capturas con nombres de alumnos o docentes ni el nombre de la escuela.

## Pendientes

- Poner la URL real en `site-url` (`_quarto.yml`) y en `robots.txt`.
- Usuario de LinkedIn y ID de Formspree en `index.qmd` (buscar `TU-USUARIO` y `TU-ID`).
- Foto de perfil en `img/mifoto.jpeg`.
- Post de Gym Tracker: los fragmentos de código son versiones simplificadas; cambiarlos por el código
  real del repo https://github.com/manu-09-web/GymAppkt.
- Post de EduControl: falta decir qué servicios de AWS se usaron (hay un comentario HTML en "Mi parte").
- Definir cómo publicar posts sin tocar código (el profe lo va a enseñar; opciones: Decap CMS o crear
  el archivo desde GitHub con el workflow ya incluido).

## Cómo trabajar con Manuel

- Avanzar por pasos pequeños y decir qué cambió en cada uno.
- Tiene que poder explicar el proyecto, así que el código debe ser entendible.
