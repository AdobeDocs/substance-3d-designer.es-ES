---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Utilice el nodo Paso alto de luminancia para extraer detalles de luminancia de alta frecuencia de texturas para mejorar los detalles de la superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paso alto de luminancia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# Paso alto de luminancia

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## Paso alto de luminancia

**En:** *Filtros/Ajustes*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Cancela la información de iluminación realizando un [paso alto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) en el valor de luminancia de la entrada. Útil para corregir texturas fotografiadas con información de iluminación. Se puede combinar en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) con varias pasadas para eliminar distintas frecuencias de detalles de iluminación.

Hace un trabajo ligeramente mejor en la conservación de colores que [Iluminación Cancelar bajas frecuencias.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

## Parámetros

* **Radio**: *0.0 - 64.0* Radio del efecto paso alto. Un radio más pequeño cancela una iluminación más pequeña, ajústela para que coincida con las imágenes de entrada.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
