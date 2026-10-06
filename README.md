# manu.dev

Blog personal hecho con [Quarto](https://quarto.org).

## Verlo en tu compu

1. Instala Quarto desde https://quarto.org/docs/get-started/
2. En esta carpeta: `quarto preview`

## Antes de publicar

Busca `TU-USUARIO` y `TU-ID` en el proyecto y cámbialos:

- `_quarto.yml` → `site-url` (necesario para sitemap, RSS y URLs canónicas) y link de GitHub
- `robots.txt` → URL del sitemap
- `index.qmd` → tu LinkedIn y el ID de Formspree del formulario
- Pon tu foto en `img/mifoto.jpeg` (si no existe, la landing muestra tus iniciales)

## Crear un post

1. Crea una carpeta en `posts/`, por ejemplo `posts/mi-nuevo-post/` (ese nombre será la URL: corto, en minúsculas y con guiones).
2. Dentro crea `index.qmd` con este encabezado:

```yaml
---
title: "Título del post (50 a 60 caracteres es lo ideal)"
description: "Resumen de 1 o 2 frases. Es lo que muestra Google y la tarjeta al compartir."
date: 2026-10-05
categories: [Mobile, Kotlin]
image: portada.png          # opcional, guárdala en la misma carpeta
image-alt: "Qué se ve en la portada"
featured: false             # true = aparece como Destacado en el blog
---
```

3. Escribe el contenido en Markdown usando `## Subtítulos` (con ellos se arma el índice "En este post").

El blog, el feed, las categorías, el RSS y el sitemap se actualizan solos.

## Publicar en GitHub Pages

1. Sube el proyecto a un repositorio de GitHub.
2. Una sola vez, desde tu compu: `quarto publish gh-pages`
3. Desde ahí, cada push a `main` publica solo (ver `.github/workflows/publish.yml`).
