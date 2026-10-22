# manu.dev — blog personal de Manuel Herrera

Landing personal hecha con **Quarto** (generador de sitios estáticos). El **blog se separó**: se rehace
aparte con Astro y se despliega en Vercel. Este repo contiene **solo la landing**. Es una tarea de la carrera
(Ingeniería en Tecnologías de la Información e Innovación Digital, Universidad Politécnica de Chiapas).
Aquí se publican experiencias de la carrera y cosas que Manuel va aprendiendo. Todo el contenido va en español.

## Comandos

- `quarto preview` — levanta el sitio y recarga al guardar. Úsalo para verificar cada cambio.
- `quarto render` — genera el sitio en `_site/`.

El sitio todavía **no se ha probado completo**: se armó sin poder ejecutar Quarto. Lo primero es correr
`quarto preview` y corregir cualquier error antes de cambiar otra cosa.

## Estructura

- `_quarto.yml` — configuración, navbar, SEO (site-url, Open Graph, RSS, canonical).
- `index.qmd` — landing: hero, sobre mí, tecnologías, proyectos, certificaciones, contacto. Es HTML dentro de un bloque `{=html}`.
- `_variables.yml` — `blog-url`, la dirección del blog. Todos los links al blog usan `{{< var blog-url >}}`; cambiarla solo ahí.
- `img/proyectos/` — portadas de EduControl y Gym Tracker que usa la landing.
- `styles/theme.scss` — todo el diseño. Los colores están arriba como variables Sass.
- `assets/site.html` — JS: botón para volver arriba (también tiene código de los listados del blog que ya no se usa).
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
- Los bocetos originales definían cuatro pantallas (landing, blog, entrada y feed); aquí solo queda la landing.

## Contenido

- Solo dos proyectos en todo el sitio: **EduControl** y **Gym Tracker**. No agregar otros sin que lo pida.
- Los posts (`kotlin-compose` y `proyecto-integrador`) se respaldaron en `../respaldo-posts/` para pasarlos al blog en Astro.
- Los posts se escriben en primera persona con lo que Manuel hizo de verdad. No inventar datos,
  opiniones ni detalles técnicos; si falta información, preguntarle.
- Certificaciones: solo la lista (nombre, institución, fecha). No publicar los PDF.
- En EduControl no mostrar capturas con nombres de alumnos o docentes ni el nombre de la escuela.

## Pendientes

- ID de Formspree en `index.qmd` (buscar `TU-ID`).
- Poner la URL real del blog en `_variables.yml` cuando esté desplegado en Vercel.

## Cómo trabajar con Manuel

- Avanzar por pasos pequeños y decir qué cambió en cada uno.
- Tiene que poder explicar el proyecto, así que el código debe ser entendible.
