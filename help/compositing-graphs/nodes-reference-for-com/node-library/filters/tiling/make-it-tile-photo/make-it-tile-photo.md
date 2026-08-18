---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Utilice el nodo Hacer fotografía en mosaico para convertir fotografías en texturas de mosaico perfectas para la creación de materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hacer que la fotografía en mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Hacer que la fotografía en mosaico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## Fotografía en mosaico de la imagen (escala de grises)

**En:** *Filtros/Mosaico*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo proporciona la funcionalidad de reparación de bordes para cualquier imagen que no pueda estar en mosaico debido a bordes no continuos. No afecta a nada que no sean los bordes de la imagen de entrada. Si desea ajustar la escala o el mosaico de diferentes maneras, consulte [Parche del mosaico Make It Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

## Parámetros

* **Deformación de máscara H**: *-100.0 - 100.0* Introduce la deformación en el eje horizontal para evitar transiciones no definidas.
* **Deformación de máscara V**: *-100.0 - 100.0* Introduce la deformación en el eje vertical para evitar transiciones no definidas.
* **Tamaño de máscara H**: *0.0 - 1.0* Establece hasta dónde llega horizontalmente el borde de la transición.
* **Tamaño de máscara V**: *0.0 - 1.0* Establece hasta dónde llega verticalmente el borde de la transición.
* **Precisión de máscara H**: *0.0 - 1.0* Establece la suavidad horizontal de la transición.
* **Precisión de máscara V**: *0.0 - 1.0* Define qué tan suave es verticalmente la transición.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
