---
name: generate-node-documentation
description: ""
source-git-commit: 69f546a26d2e09127b1c79ef4003e235536289da
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---


# Generando documentación del nodo

Cada página de referencia de nodo de hoja de este repositorio sigue una estructura coherente. Esto
la habilidad es la especificación de esa estructura. El ejemplo canónico, totalmente trabajado es
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
en caso de duda, ábrelo y refleja el resultado.

Esta aptitud solo cubre la página de nodo *structure*. Para el marcado de Experience League base
(bloques de nota/alerta, enlaces relativos-vs-absolutos, UICONTROL/DNL, parámetros de consulta de imágenes,
pelusa gotchas) sigue la habilidad `write-experience-league-markdown`.

## Dónde reside una página de nodo (carpeta / convención de índice)

* Una carpeta por nodo, bajo la ruta de categoría/subcategoría coincidente, p. ej.
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* La carpeta se denomina como el título del nodo kebab-case; contiene **un** archivo `.md`
con el mismo nombre.
* Todos los medios incrustados de la página (icono, imágenes de ejemplo, GIF) viven en un hermano **  `<node-name>.resources/` carpeta **junto a `.md` y se hace referencia a ella con una
  ruta relativa (p. ej. `<node-name>.resources/<file>.png`). No señalar páginas de nodo en
  la carpeta `help/assets/` compartida, es decir, un modelo heredado que se está eliminando gradualmente; nuevo y
  las páginas editadas utilizan su propia carpeta `.resources`.
* Cada página tiene una entrada correspondiente en `help/guide/TOC.md`. Al añadir o mover un
página, actualice `TOC.md` y el diseño de carpeta juntos (consulte la carpeta/índice de CLAUDE.md)
convención).

## Materia prima

Las páginas de nodos usan el bloque **minimal**, solo `title` y un estilo de ruta de exploración
`description`. (Esto es distinto de los documentos de 11 campos heredados de bloque CLAUDE.md para
páginas de contenido normal).

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## Estructura corporal

De arriba abajo, todo lo que está debajo de la materia frontal:

### &#x200B;1. Título H1

Un solo `# <Node title>`: exactamente un H1 por página.

### &#x200B;2. Icono / tabla de descripción

Una tabla de HTML, una fila, dos celdas. La celda izquierda (`33.33%`) contiene el icono y luego el
`In:` ruta de exploración; la celda derecha (`100.00%`) contiene `## Description` y la prosa.

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

Convenciones de prosa de celda de descripción:
* Separe los párrafos con `<br><br>` (las líneas en blanco dentro de la celda no son fiables).
* El énfasis en línea es `<b>…</b>` / `<i>…</i>`.
* Los asistentes de introducción usan `<i>Note:</i>` / `<i>Tip:</i>` al comienzo de la oración.
* Use `&gt;` para `>` en la línea `In:` (está dentro de HTML). Tome la categoría /
nombres de subcategoría del propio nodo; no los inventes.

### &#x200B;3. Llamadas opcionales

`>[!INFO]`, `>[!TIP]`, `>[!NOTE]`, etc. ir **después de** la tabla de icono/descripción (no
dentro de la celda). Sintaxis según la aptitud `write-experience-league-markdown`.

### &#x200B;4. Entradas

Incluir sólo si el nodo tiene pin de entrada. Precede el encabezado con un anclaje.

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* Dos columnas, fila de encabezado vacía, alineación de `|:---|:---|`.
* Una fila por entrada: celda izquierda `<b>Name</b> <i>Type</i>`, celda derecha de la descripción.
* El marcador de tipo es cursiva de HTML — `<i>Type</i>` — no marcado `*Type*`.

### &#x200B;5. Salidas

Misma forma que Entradas, con `<a name="outputs"></a>` + `## Outputs`. Incluir sólo si el
node documenta distintos resultados (muchos nodos tienen un único resultado implícito y omiten este
sección — no inventes una).

Para salidas multicanal empaquetadas, divida los canales con `<br>` y aplique sangría
subpuntos con `&nbsp;` (consulte las filas &quot;Splatter UVW&quot; / &quot;Datos de salpicaduras&quot; en el
referencia):

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. Parámetros

La misma forma de tabla, con `<a name="parameters"></a>` + `## Parameters`. Omitir el todo
si el nodo no tiene parámetros (nunca emitir una tabla vacía o un &quot;Sin parámetros&quot;).
línea).

* **Parámetros agrupados**: emitir una fila de etiqueta de expansión con una celda derecha vacía antes de la
filas del grupo:

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **Valores de enumeración / opción múltiple**: enumerar las opciones dentro de la celda de descripción como
  Lista de guiones separados por `<br>`:

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. Ejemplos

Incluir sólo si hay imágenes/GIF de ejemplo. Utilizar una tabla de galería de HTML; uno `<td>`
por imagen con un pie de ilustración opcional; ajustar a un nuevo `<tr>` después de 3 imágenes. Rutas de medios
apunte a la carpeta `.resources` de la página.

```html
## Examples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file>.gif" /><br><i>Caption</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file2>.jpg" /><br><i>Another caption</i>
        </td>
    </tr>
</table>
```

Dejar las celdas finales en una fila final parcialmente llena vacía (`<td …></td>`) en lugar de
reflujo. Omitir subtítulos si el origen no tiene ninguno.

## Valores de tipo canónico

Reutilizar el propio texto de tipo del nodo; valores típicos: `Grayscale`, `Color`, `Integer`,
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. No invente ni &quot;normalice&quot; un tipo
el nodo en realidad no usa.

## Reglas de celdas de tabla

* No hay líneas nuevas sin formato dentro de una celda de tabla: unir líneas con `<br>` (y `<br><br>` entre
párrafos).
* El énfasis dentro de las celdas es `<b>`/`<i>` y el marcador de tipo siempre es `<i>Type</i>`.
* Aplicar sangría a subpuntos anidados con `&nbsp;` secuencias.

## Reglas / no hacer

* **No fabricar** entradas, salidas o parámetros que el nodo no tiene; omita el
en su lugar. No reformules, resumes ni elimines contenido técnico existente, solo
reformatéalo.
* **Mantener vínculos relativos** a otras `.md` páginas; enlaces externos absolutos.
* **Eliminar la trama heredada** al editar una página antigua con este formato: etiquetas de dificultad
(`**Simple**` / `**Intermediate**` / `**Complex**`), el `## <Title>`
dentro de la celda de icono, frases de código auxiliar como &quot;No hay imágenes adjuntas a
esta página.&quot;, y cualquier tabla de navegación/envoltura vacía sobrante de migraciones anteriores.
* **Un H1** por página; las secciones utilizan `##` y los anclajes Entradas/Salidas/Parámetros
(`inputs` / `outputs` / `parameters`) deben preceder a sus encabezados para que se puedan cruzar las páginas
  `#inputs` vínculos resueltos.
* **Mantén `TOC.md` sincronizado** al agregar, cambiar el nombre o mover una página.
