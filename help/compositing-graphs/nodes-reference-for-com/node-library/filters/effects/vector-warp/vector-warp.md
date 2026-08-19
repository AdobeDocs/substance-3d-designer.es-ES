---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Deformación vectorial para deformar texturas mediante campos vectoriales para crear efectos de distorsión fluida y orgánica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación vectorial
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Deformación vectorial

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-warp.png){width="128px"}

![](../../../../../../assets/vector-warp-grayscale.png){width="128px"}

## Deformación vectorial (escala de grises)

**En:** *Filtros/Efectos*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

La deformación vectorial es un efecto de distorsión avanzado, similar a [Deformación](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) y [Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), con la principal diferencia de que se basa en un mapa de bits vectorial (de color) en lugar de un mapa de escala de grises. Esto significa que es más potente y versátil que sus primos nodo atómico.

El mapa vectorial es similar a un mapa normal, pero no es necesario normalizarlo y solo se utilizan los canales R y verde (X e Y). Los canales azules y Alpha pueden dejarse en negro si lo desea. La construcción de un buen Mapa de Vectores puede ser el mayor desafío en el uso de este nodo; puede [convertir mapas en escala de grises a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) o construir el mapa combinando canales con [Combinación RGBA.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) Como alternativa, también se puede usar algo como [&quot;Flow Map&quot;](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting).

Este nodo puede ser útil cuando se desea realizar distorsiones muy específicas con direcciones variables, donde los nodos de deformación estándar no lo cortan.

## Parámetros

### Entradas

* **Entrada**: *Entrada de color*\
  Mapa para distorsionar.
* **Mapa de vectores**: *Entrada de color*\
  Mapa del controlador de distorsión. Se utilizan los canales de color rojo y azul.

### Parámetros

* **Intensidad**: *0.0 - 1.0* Multiplicador de intensidad para el mapa vectorial.
* **Formato de vector**: *DirectX, OpenGL* Cambia el canal verde entre la interpretación hacia arriba y hacia abajo.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/vector-warp-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
