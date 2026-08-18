---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Utilice el nodo Sobel de curvatura para detectar bordes de curvatura mediante los operadores Sobel para crear máscaras basadas en bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel de curvatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# Sobel de curvatura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## Sobel de curvatura

**En:** *Filtros/Efectos*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza una conversión de curvatura de un solo paso simple y estricta para introducir [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). El mapa resultante tiene matices blancos para áreas convexas y negros para cóncavas. La curvatura siempre produce líneas más gruesas y transiciones nítidas.

Este nodo es útil para resaltar u oscurecer rápidamente determinados bordes. Es ligeramente diferente de [Curvature](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), ya que produce resultados de mejor calidad, pero sigue siendo nítido y duro.

## Parámetros

* **Intensidad**: *0.0 - 1.0* Intensidad del efecto, ajusta el contraste.
* **Tipo normal**: *DirectX, OpenGL*

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
