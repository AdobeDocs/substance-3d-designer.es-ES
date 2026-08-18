---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Utilice el nodo Reemplazar rango de color para reemplazar los colores de un rango especificado por colores nuevos para la corrección de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Reemplazar rango de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# Reemplazar rango de color

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## Reemplazar rango de color

**En:** *Filtros/Ajustes*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Reemplaza Color de origen por Color de destino, con controles adicionales. Por ejemplo, se puede utilizar para cambiar el color de partes de un mapa de ID de material (hornear).

Para obtener una versión más avanzada, vea [Coincidencia de color.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## Parámetros

* **Color de origen**: *(Valor de color)*Color que se va a reemplazar.
* **Color de destino**: *(Valor de color)*Color que se va a sustituir.
* **Intervalo de origen**: *0.0 -* 1.0\
  Rango o tolerancia del origen seleccionado. Se puede aumentar para que los colores contiguos también cambien de tono.
* **Umbral**: *0,0 - 1,0* Difuminación/contraste para el rango. Establezca bajo para reemplazar solo el color de origen, o más alto para reemplazar también los colores que se fusionan en origen.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
