---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro de curvatura para generar mapas de curvatura a partir de mapas de height para detectar superficies convexas y cóncavas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# Curvatura (nodo de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## Curvatura

**En:** *Filtros/Efectos*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza una conversión de curvatura de un solo paso simple y estricta para introducir [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). El mapa resultante tiene matices blancos para áreas convexas y negros para cóncavas. La curvatura siempre producirá líneas delgadas como píxeles y transiciones nítidas.

Este nodo es útil para realzar u oscurecer rápidamente determinados bordes. Está limitado en comparación con [Curvature Smooth](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (que produce resultados de mayor calidad) y [Curvature Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (que tiene más opciones).

## Parámetros

* **Intensidad**: *0.0 - 10.0* Intensidad del efecto. Aumenta el contraste del resultado.
* **Formato normal**: *DirectX, OpenGL*\
  Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
