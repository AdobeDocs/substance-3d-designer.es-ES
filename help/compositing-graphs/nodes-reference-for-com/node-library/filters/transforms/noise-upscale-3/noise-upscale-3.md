---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Utilice el nodo Noise Upscale 3 para aumentar la escala de las texturas mediante algoritmos avanzados basados en ruido para conservar los detalles en resoluciones más altas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ampliación de ruido 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Ampliación de ruido 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Ampliación de ruido 3

**En:** *Filtros/Transformaciones*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un procedimiento de ruido de entrada y lo escala a doble resolución, manteniendo el detalle pero sin introducir demasiadas baldosas. Utiliza una máscara definida por el usuario para fusionar el ruido sobre su escala original.

Este nodo está destinado principalmente a optimizar gráficos lentos que utilizan ruidos grandes y pesados. Permite utilizar resoluciones más altas sin introducir demasiado tiempo de cálculo adicional.

Vea también [Noise Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) y [Noise Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), que en la mayoría de los casos tienden a ser ligeramente mejores para ocultar el mosaico.

## Parámetros

### Entradas

* **Escala de grises**: *Entrada en escala de grises*\
  Imagen de ruido de destino.
* **Máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

*No hay parámetros.*

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise3ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
