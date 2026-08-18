---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: Utilice el nodo Iluminación > Cancelar altas frecuencias para eliminar los detalles de iluminación de alta frecuencia de las texturas para el análisis de materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iluminación Cancelar altas frecuencias
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# Iluminación Cancelar altas frecuencias

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/lighting-cancel-high-frequencies.png){width="128px"}

## Iluminación Cancelar altas frecuencias

**En:** *Filtros/Ajustes*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Similar a [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), pero más adecuado para imágenes a todo color (no desatura tanto el resultado), este nodo intenta cancelar los detalles de iluminación pequeños y alta frecuencia.

Consulte también [Cancelación de iluminación con frecuencias bajas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) y la opción más avanzada recomendada: [Paso alto de luminancia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md).

## Parámetros

* **Intensidad**: *0.0 -* 1.0\
  Intensidad del efecto de cancelación de iluminación.
* **Radio**: *0.0 - 10.0* Radio o tamaño de los detalles de iluminación que se van a cancelar.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/lighting-cancel-highfrequencies-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
