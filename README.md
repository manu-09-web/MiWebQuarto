# manu.dev

Landing personal hecha con [Quarto](https://quarto.org).
El blog vive aparte (Astro + Vercel); su dirección está en `_variables.yml`.

## Verlo en tu compu

1. Instala Quarto desde https://quarto.org/docs/get-started/
2. En esta carpeta: `quarto preview`

## Cambiar la dirección del blog

Edita `blog-url` en `_variables.yml`. Todos los links al blog de la landing
(`{{< var blog-url >}}` en `index.qmd`) toman ese valor.

## Pendiente

- `index.qmd` → ID de Formspree del formulario (busca `TU-ID`)

## Publicar en GitHub Pages

Cada push a `main` publica solo (ver `.github/workflows/publish.yml`).
