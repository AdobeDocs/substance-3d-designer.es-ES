---
source-git-commit: 9f19a0232c1f355ba2450995b4a6d23b7ed846d1
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---
# CLAUDE.md

Este archivo proporciona orientación a Claude Code (claude.ai/code) cuando se trabaja con código en este repositorio.

# Documentación de Substance 3D Designer

Este repositorio contiene la documentación de Substance 3D Designer. No hay código de aplicación, paso de compilación ni conjunto de pruebas: el repositorio *es* el contenido, escrito en Markdown y publicado en [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en).

# Estructura del repositorio

* `help/`: todo el contenido de la documentación, organizado para reflejar la tabla de contenido.
* `help/guide/TOC.md`: la tabla de contenido. Cada entrada es un vínculo relativo (con raíz en `/help/...`) al archivo de marcado de una página. `TOC.md` también lleva metadatos de árbol de páginas (`user-guide-title`, `breadcrumb-title`, `nudge`, anclajes de sección como `{#section-id}`).
* `help/assets/`: carpeta heredada de imágenes compartidas. Los medios específicos de la página ahora se encuentran en una carpeta del mismo nivel `<md-file-name>.resources/` por página (consulte la convención Carpeta/TDC a continuación); solo un puñado de imágenes sobrantes no referenciadas por ninguna página aún se encuentran aquí. Coloque las nuevas imágenes en la carpeta `.resources` de la página using, no aquí.
* `help/glossary/glossary.md`: una sola página de glosario grande, organizada alfabéticamente con intervalos de anclaje (`<span id="term"></span>`) utilizados para el entrecruzamiento mediante `#term` fragmentos.
* `metadata.md`: materia frontal de nivel de repositorio (nube/solución/ID de producto, `git-repo`, etc.) heredado por cada `TOC.md`. Editar esto solo para cambios de metadatos en todo el repositorio; los metadatos específicos de la página pertenecen a la propia materia principal de la página.
* `redirects.csv`, `linkcheckexclude.json`, `markdownlint_custom.json`, `pipeline.opts`: configuración de canalización de publicación (redirecciones, excepciones de comprobación de vínculos, anulaciones de reglas de lint, opciones de canalización).
* `fix-image-names.py`: utilidad única que cambia el nombre de `help/assets` imágenes con sufijos entre paréntesis (p. ej. `foo(1).png` → `foo_1.png`) y reescribe cada referencia de Markdown para que coincida. No forma parte de ningún flujo de trabajo normal; ejecutar manualmente sólo cuando vuelvan a aparecer esos nombres de archivo.

## Convención de carpeta/índice

Para cada entrada de `help/guide/TOC.md`:
* Hay una carpeta correspondiente en `help/`, que sigue el mismo anidamiento que el índice.
* Esa carpeta contiene un archivo Markdown, denominado como la versión kebab-case del título de la página.
* Si la página tiene medios a medida (imágenes, GIF, vídeos), vive en una subcarpeta del mismo nivel denominada `<md-file-name>.resources`.

Al agregar o mover una página, actualiza `TOC.md` y el diseño de la carpeta a la vez: deben permanecer sincronizados.

## Páginas de referencia de nodos

Los árboles de la biblioteca de nodos (p.ej. `help/compositing-graphs/nodes-reference-for-com/node-library/<category>/<node>/<node>.md`) son un tipo de página distinto con su propio diseño coherente: una tabla de HTML de iconos/descripciones, seguida de `## Inputs` / `## Outputs` / `## Parameters` tablas ancladas (`#inputs`/`#outputs`/`#parameters`) y una galería de `## Examples`. Utilizan la **materia frontal mínima** (solo `title` + `description`), no el bloque de página de contenido normal que aparece a continuación (modelado en `.../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md`). Los medios incrustados (icono, imágenes de ejemplo/GIF) se encuentran en una carpeta del mismo nivel `<node-name>.resources/` junto a la página, a la que se hace referencia relativamente. Utilice la aptitud `generate-node-documentation` (si existe) para la plantilla de creación completa.

## Page front matter

Las páginas de contenido normal utilizan un bloque de contenido frontal como:

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

Mantén `description` preciso y conciso: se usa para fragmentos de SEO y búsqueda.

# Reglas de creación de contenido

* El inglés es la fuente de la verdad; todos los demás idiomas se traducen desde él.
* Todos los vínculos a otras páginas de documentación deben ser vínculos **relativos**; todos los vínculos a recursos externos deben ser vínculos **absolutos**.
* El contenido se escribe en el marcado con sabor a GitHub con las extensiones/gotchas personalizadas de Experience League, documentadas [aquí](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown). Utilice la aptitud `write-experience-league-markdown` (si existe) para los detalles específicos.
* Cada cambio enviado pasa por comprobaciones automatizadas de pelusa y validación de vínculos en CI (véase a continuación): compruebe `markdownlint_custom.json` y `linkcheckexclude.json` antes de asumir que se aplica una regla o que es necesario corregir un vínculo.

# Validación / IC

* `.github/workflows/validate-articles.yml` se ejecuta en relaciones públicas y se inserta en `main` (y a través de un comentario de relaciones públicas de `retest`), llamando al flujo de trabajo reutilizable compartido de `Adobe-Enterprise-Docs/workflows` para depurar marcas y validar vínculos. No hay un script equivalente local en este repositorio: CI es la fuente de confianza para la acción de aprobado/suspenso.
* `.github/workflows/mirror.yml` duplica `main` en el repositorio público al insertarlo; se trata de infraestructura, no de algo que los cambios de contenido deban tocar.
* `markdownlint_custom.json` extiende el conjunto de reglas de `markdownlint.json` compartidas y deshabilita varias reglas (MD005, MD007, MD018, MD032, MD033, MD034, MD037, MD040) que entran en conflicto con las extensiones de marcado personalizadas de Experience League (por ejemplo, HTML en línea, énfasis no estándar). No &quot;arregle&quot; el contenido para cumplir estas reglas deshabilitadas.
* `linkcheckexclude.json` listas blancas con patrones de vínculos (actualmente `example.com`/`example-end.com`) que el verificador de vínculos debe omitir.

# Convenciones de trabajo

* Esta es una documentación con muchas notas de la versión: las notas de la versión están activas en `help/release-notes/`, una carpeta por versión (p. ej. `version-16-0`), más `all-changes` y `old-versions` páginas de agregación. Siga la carpeta de la versión existente como plantilla al añadir una nueva versión.
