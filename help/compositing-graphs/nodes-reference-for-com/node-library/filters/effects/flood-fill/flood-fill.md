---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill para rellenar regiones conectadas de color similar para crear máscaras y efectos de procesamiento de textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill.png){width="128px"}

## Flood Fill

**En:** *Filtros/Efectos*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Flood Fill forma parte de un conjunto avanzado de efectos que le permiten añadir mucha más variación a una textura básica de azulejos binarios. No está destinado a ser utilizado por sí mismo: en su lugar, es más bien un punto de partida para los efectos de Otros Flood Fill. Estos datos separados y divididos permiten un flujo de trabajo más dinámico, optimizado y menos destructivo.

Los otros efectos de Flood Fill son [Flood Fill a degradado](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [Flood Fill a color/escala de grises](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [Flood Fill a escala de grises aleatoria](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [Flood Fill a color aleatorio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [Flood Fill a tamaño de cuadro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [Flood Fill a posición](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Asignador de Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) y [Flood Fill a índice](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> El mapa de entrada debe ser adecuado para que el Flood Fill funcione. Idealmente es un mapa binario (solo blanco/negro, sin escala de grises) donde cada mosaico está separado de las otras líneas por un borde que es negro completo (0,0,0) por cada píxel. Un ejemplo de candidato perfecto para esto es [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).
> 
> Se producen problemas si los mosaicos no están separados por píxeles totalmente negros, normalmente cuando se utilizan valores inclinados de escala de grises. Esto se puede identificar por una falta general de valores rojos en el resultado y, posiblemente, líneas de artefactos extraños. En tales casos, ajuste el contraste en el mapa de entrada o cambie el mapa de entrada hacia fuera. Asegúrese de cambiar el ajuste de compensación Seguridad/Velocidad para ver si hay alguna mejora.

## Parámetros

* **Compensación de seguridad/velocidad**: *Formas simples o pequeñas, formas complejas o grandes, modo sin errores.*Establezca el modo de cálculo para que se adapte mejor a las formas de entrada. Permite obtener resultados mucho más precisos si se elige el modo correcto.
* **Opciones avanzadas**: *Mostrar parámetros avanzados y Generar/Ocultar parámetros y resultados avanzados*
* **Anular intercambio de seguridad/velocidad**: *-1 - 100* Solo visible con Opciones avanzadas activadas. Permite la modificación de funciones internas. Muy avanzado, sirve para crear sus propios efectos o depurar.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/flood-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/flood-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

Buenos y malos ejemplos de resultados de Flood Fill.

</td>
</tr>
</table>
