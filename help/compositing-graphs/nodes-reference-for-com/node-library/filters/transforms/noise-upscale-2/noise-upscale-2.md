---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: Utilice el nodo Noise Upscale 2 para aumentar la escala de las texturas mediante la interpolación basada en ruido para mantener la calidad de la textura en tamaños mayores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ampliación de ruido 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# Ampliación de ruido 2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Ampliación de ruido 2

**En:** *Filtros/Transformaciones*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un procedimiento de ruido de entrada y lo escala a doble resolución, manteniendo el detalle pero sin introducir demasiadas baldosas. Utiliza un tipo de máscara &quot;X&quot; y se fusiona con menos contraste que la entrada original (los modos de fusión internos son Máx y Mín).

Este nodo está destinado principalmente a optimizar gráficos lentos que utilizan ruidos grandes y pesados. Permite utilizar resoluciones más altas sin introducir demasiado tiempo de cálculo adicional.

Consulta [Noise Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) y [Noise Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) para obtener diferentes variaciones de este proceso.

## Parámetros

* **Desplazamiento1X**: *0.0 - 1.0* Desliza las partes superior e inferior sobre el eje X.
* **Desplazamiento1Y**: *0.0 - 1.0*\
  Desliza las partes superior e inferior sobre el eje Y.
* **Desplazamiento2X**: *0.0 - 1.0* Desliza las partes izquierda y derecha sobre el eje X.
* **Desplazamiento2Y**: *0.0 - 1.0* Desliza las partes izquierda y derecha sobre el eje Y.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise2ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
