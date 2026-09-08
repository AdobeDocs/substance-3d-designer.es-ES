---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: 9f19a0232c1f355ba2450995b4a6d23b7ed846d1
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 6%

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
explícito `<span id="anchor-id"></span>` inmediatamente antes del término —
consulte `help/glossary/glossary.md` para ver el patrón utilizado en este repositorio.
* Los delimitadores de sección `TOC.md` utilizan la sintaxis `{#section-id}` después de un encabezado o lista
etiqueta, p. ej. `Getting started{#getting-started}`.

## Imágenes

* `![Alt text](path/to/image.png "Optional hover title")`.
* Se admiten parámetros de consulta de tamaño y optimización opcionales:
  `![Adobe logo](my-page.resources/logo.png?width=750&format=png&optimize=medium)`.
* **El texto alternativo no debe contener guiones bajos**; no se representan correctamente;
en su lugar, utilice guiones o espacios.
* Las imágenes específicas de la página se encuentran en una carpeta del mismo nivel `<page-name>.resources/`
junto a `.md`, referenciado relativamente (p. ej.
  `<page-name>.resources/image.png`). `help/assets/` es un legado compartido
  carpeta — no agregue imágenes nuevas allí (vea CLAUDE.md).

## Tablas

* Delimitado por canalizaciones, con una fila de separación de encabezados de guion:

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* Una línea en blanco debe preceder a la tabla o no se representará como tabla.
* Las tablas no pueden contener de forma limpia contenido de bloques complejos o de varios párrafos en un
celda — donde este repositorio necesita imágenes/listas dentro de una celda de tabla (p.ej.
tablas de comparación en `overview.md`), vuelve al HTML en línea
(`<div>`, `<b>`, `<ul>`/`<li>`) con `data-preserve-html="true"` en cada uno
para que la canalización no la retire. Seguir ese patrón existente más bien
que inventar un nuevo HTML en línea a menos que sea necesario.

## Código

* Código en línea: un solo tic.
* Bloques cercados: triplicar las marcas, con un lenguaje opcional para la sintaxis
resaltando (` `&#x200B;``python `, ` ``&#x200B;`javascript `, etc.).

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

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

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

Consulte la sección &quot;Page front matter&quot; de CLAUDE.md para ver el bloque exacto utilizado por
páginas de contenido normal en este repositorio y `metadata.md` para el nivel de repositorio
campos heredados.