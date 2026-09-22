---
name: write-experience-league-markdown
description: |
  Reglas de sintaxis, extensiones personalizadas y obstáculos para escribir contenido de marcado publicado en Adobe Experience League. Utilice esta aptitud siempre que cree o edite cualquier página en ayuda/ en este repositorio (o en cualquier otro repositorio de contenido de Experience League): encabezados, vínculos, imágenes, tablas, bloques de notas/alertas, etiquetas UICONTROL/DNL, incrustaciones de vídeo, anclajes y obstáculos de procesamiento conocidos. Fuente: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
---

# Escribir marcado de Experience League

Experience League procesa el marcado con sabor a GitHub mediante una canalización personalizada
con sus propias extensiones y peculiaridades de procesamiento. GFM estándar funciona principalmente, pero
los elementos siguientes son específicos del Experience League: equivocarse y contenido
falla el CI lint/link-check o se procesa incorrectamente en el sitio activo.

## Títulos

* De `#` a `#####` (niveles 1-5). La materia principal de la página `title` es
efectivamente nivel 0; el primer encabezado Markdown del cuerpo debe ser un
un único encabezado `# Level 1` que coincide (o coincide estrechamente) con el título de la página.
* No omita niveles arbitrariamente; el mini-TOC se genera a partir de encabezados.

## Formato de texto

* `**bold**`, `*italic*`, `***bold and italic***`.
* Aplique escape a caracteres especiales literales con una barra invertida (`\*`, `\_`, etc.).
* **Ampersands** en encabezados/títulos debe escribirse (`and`) o codificarse como
  `&amp;`: un `&` sin formato en un título puede interrumpir el análisis.
* **Los corchetes angulares** que se utilizan como texto literal (no como HTML real) deben estar codificados:
  `<placeholder>` → `&lt;placeholder&gt;`.
* Las **comillas tipográficas** pegadas desde procesadores de texto deben estar codificadas, no dejadas como
caracteres literales de rizo: doble izquierdo `&#8220;`, doble derecho `&#8221;`,
apóstrofe/soltero derecho `&#8217;`.

## Listas

* Listas numeradas: iniciar todos los elementos con `1.` (o `1)`): GitHub/Experience
Los números automáticos de la liga independientemente de los dígitos literales escritos.
* Listas con viñetas: usar `*`, `-` o `+`, pero **no mezclar caracteres de viñeta
en la misma lista o documento**.
* La anidación de listas `TOC.md` utiliza `+` de forma coherente: siga los pasos del archivo existente
estilo bullet en lugar de introducir uno diferente.

## Vínculos

* Las referencias cruzadas internas deben ser vínculos de marcado **relativo** a la
archivo de destino `.md`: `[Overview](../../overview.md)`.
* Las referencias externas deben ser direcciones URL **absolutas**.
* Ancla en los encabezados/grupos de otra página: anexar `#anchor-id`, p. ej.
  `[Mesh](../../glossary/glossary.md#mesh)`.
* Los anclajes de la página se declaran como encabezado (autoslugging) o como
explícito `<span id="anchor-id"></span>` (HTML) / `{: #anchor-id}` (marcado) inmediatamente antes del término —
consulte `help/glossary/glossary.md` para ver el patrón utilizado en este repositorio.
* Los delimitadores de sección `TOC.md` utilizan la sintaxis `{#section-id}` después de un encabezado o lista
etiqueta, p. ej. `Getting started{#getting-started}`.

## Imágenes

Utilice la sintaxis de imágenes de marcado siempre que sea posible:

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* El texto `![...]` es un texto alternativo accesible obligatorio. Hazlo conciso y hazlo
no utilizar guiones bajos; en su lugar, utilice espacios o guiones.
* La ruta de acceso de la imagen puede ser relativa al archivo de marcado o relativa a la raíz, como
como `/help/assets/shared-image.png`. Las imágenes específicas de la página pertenecen al
carpeta del mismo nivel `<page-name>.resources/` (por ejemplo,
  `<page-name>.resources/image.png`). `help/assets/` es una carpeta compartida heredada;
  no agregue allí nuevas imágenes específicas de la página.
* Los parámetros opcionales de consulta de imágenes pueden controlar el procesamiento de CDN:
  `?width=750&format=png&optimize=medium`. Mantener estos parámetros en la imagen
  URL, antes de cualquier bloque de propiedad.
* Agregar propiedades de imagen inmediatamente después del cierre `)`:
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width` es un valor de píxel o porcentaje del área de vista; escala de imágenes
proporcionalmente. Los valores de alineación admitidos son `center` y `right`.
  `valign` no es compatible.
* Use `modal="regular"` o `zoomable="yes"` para hacer clic para hacer zoom en una imagen:
  `![Alt text](image.png){width="100" zoomable="yes"}`. No combinar
  hacer clic para hacer zoom con un vínculo de imagen; el hipervínculo tiene prioridad.
* Para crear un vínculo de imagen a otra página, ajuste la imagen en un vínculo de marca:
  `[![Alt text](image.png)](../target/target.md)`.
* Para imágenes grandes, proporcione al menos 640 píxeles de anchura de origen cuando sea práctico,
no utilice más de 2000 píxeles a menos que sea necesario y mantenga los archivos de imagen bajo
5 MB cuando sea posible. La canalización acepta archivos de hasta 100 MB, pero los archivos de más
Validación de error de 20 MB y los artículos no deben contener más de
100 imágenes (algunas guías antiguas dicen 200; utilizar el límite más estricto).

Utilice HTML sólo cuando Markdown no pueda expresar el diseño requerido, como un
una tabla especial o una presentación en línea personalizada. El formulario de imagen de HTML compatible
es:

```html
<img src="image.png" alt="Alt text" />
```

* Proporcione siempre un atributo `alt` significativo y use un atributo relativo o
`src` relativo a la raíz coherente con las imágenes de marcado.
* Para imágenes de HTML dentro del HTML en línea conservado, agregue
  `data-preserve-html="true"` a las etiquetas contenedoras cuando lo requiera el
  marcas de alrededor. Por ejemplo:

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* Para activar la función de hacer clic para hacer zoom en una imagen de HTML, utilice
  `class="modal-image"` en la etiqueta `<img>`.
* No utilice atributos de HTML no compatibles ni confíe en `valign`; prefiera Markdown
propiedades de anchura y alineación.

## Tablas

Prefiera tablas de marcado nativas para contenido tabular ordinario:

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* Coloque una línea en blanco antes de la tabla. Las tablas de marcado requieren al menos una
fila de encabezado y fila de un cuerpo; utilizar una tabla de HTML para una fila o sin encabezado
tabla.
* Utilice al menos tres guiones en cada celda de separador de encabezados y mantenga el mismo
número de caracteres de canalización en cada fila. Escapar de una canalización literal como `\|` o
  `&vert;`.
* Utilice marcadores de alineación en la fila de separación cuando sea necesario:
  `|---|:---:|---:|` para la alineación izquierda, central y derecha.
* El HTML en línea es compatible con las celdas de la tabla de marcado para saltos de párrafo y
listas básicas. Usar `<p>` para párrafos separados, `<br>` para saltos de línea y
  `<ul>`/`<ol>` con `<li>` elementos para listas. Añadir
  `data-preserve-html="true"` para incluir elementos de HTML cuando lo requiera el
  marcas de repositorio circundantes.

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* Evite mesas muy anchas y muy altas; son difíciles de navegar.
Tenga cuidado con el código en línea en las tablas, ya que el código largo puede forzar
anchos de columna desproporcionados.
* Para elegir el diseño de tabla para una tabla de Markdown, agregue la propiedad después del
, separados por una línea en blanco:

  ```markdown
  {style="table-layout:fixed"}
  ```

  Usar `table-layout:auto` (el valor predeterminado) cuando el texto o el código largos necesiten flexibilidad
  anchos de columna. Usar `fixed` para columnas equilibradas, como tablas que contienen
  imágenes de tamaño similar.

Utilice una tabla de HTML cuando Markdown no pueda expresar la estructura requerida, como
omitir encabezados, combinar celdas con grupos, equilibrar columnas o alinear
contenido dentro de las celdas:

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* Los elementos de tabla admitidos son `<table>`, `<tbody>`, `<thead>`, `<tfoot>`,
  `<tr>`, `<th>`, `<td>`, `<col>` y `<colgroup>`, junto con los archivos compatibles
elementos en línea como `<p>`, `<br>`, `<b>`, `<i>`, `<ul>`, `<ol>` y
  `<li>`.
* No utilice la sintaxis Markdown dentro de una tabla de HTML. Por ejemplo, Markdown
las notas, imágenes y vínculos pueden representarse literalmente; en su lugar, utilice la sintaxis del HTML.
  Las etiquetas de localización `UICONTROL` y `DNL` son excepciones.
* Usar `align="left"`, `align="center"` o `align="right"` en una celda cuando
necesario. Las tablas de HTML no pueden contener tablas anidadas.
* Establezca el diseño de la tabla HTML en la etiqueta de apertura:
  `<table style="table-layout:auto">` o
  `<table style="table-layout:fixed">`.
* Para una tabla de HTML de una fila sin bordes, utilice
  `<tr style="border: 0;">`.

## Código

* Código en línea: un solo tic.
* Bloques cercados: triplicar las marcas, con un lenguaje opcional para la sintaxis
resaltando (` ```python `, ` ```javascript `, etc.).

## Nota / bloques de alerta

Sintaxis de blockquote personalizada, un tipo por bloque, línea de blockquote en blanco entre
la etiqueta y el cuerpo:

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

Tipos admitidos: `NOTE`, `TIP`, `IMPORTANT`, `CAUTION`, `WARNING`,
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## Incrustaciones de vídeo

Experience League no admite incrustaciones directas de vídeo MP4 o YouTube en `[!VIDEO]` bloques. Si necesita una vista previa animada, use un GIF en la carpeta del mismo nivel `.resources` de la página y céntrela con un HTML en línea si es necesario.

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

No use `[!VIDEO]` para archivos MP4 locales, remotos o URL de YouTube: la canalización de publicación los rechaza y falla CI.

## Etiqueta UICONTROL

Ajusta los nombres de los elementos de la interfaz de usuario (etiquetas de botón, elementos de menú, nombres de campo) en línea, de modo que
la canalización de localización sabe que debe comprobar si hay una cadena traducida y cae
volver a la etiqueta inglesa si no existe:

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

Utilícelo para cada etiqueta de IU literal a la que se hace referencia en el texto de instrucciones (menú
elementos, nombres de botones, títulos de cuadros de diálogo, nombres de paneles).

## Etiqueta DNL (&quot;No localizar&quot;)

Contiene nombres de productos, nombres de funciones de terceros o cualquier frase que deba
nunca se traduzca a máquina:

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

En este repositorio, utilícelo para nombres de productos como `[!DNL Substance 3D Designer]`,
`[!DNL Substance 3D Sampler]`, etc., en las menciones primero/prominentes por página,
coherente con las páginas existentes.

## HTML en línea

Se permite el HTML sin procesar (el repositorio `markdownlint_custom.json` deshabilita MD033)
específicamente por este motivo), pero solo se conserva de forma fiable a través del
canalización cuando las etiquetas llevan `data-preserve-html="true"`. Reservar HTML en línea
para los casos sin formato Markdown no puede expresar (imágenes/listas dentro de las celdas de tabla,
`<span id="...">` delimitadores) en lugar de como sustituto general de Markdown.

## Materia prima

Consulte la sección &quot;Page front matter&quot; de AGENTS.md para ver el bloque exacto utilizado por
páginas de contenido normal en este repositorio y `metadata.md` para el nivel de repositorio
campos heredados.